OpenSSL changes the DLL file names for major releases and ICS also has an internal version check when loading the DLLs to try to ensure that unknown versions are not loaded.  Generally, ICS applications are built for either OpenSSL 3 or 4 according to `{$DEFINE}`s shown below.

Distribution of the ICS OpenSSL files changed with V9.1 and later.  Earlier ICS versions required the OpenSSL DLLs to be distributed with applications, and required a root CA bundle file to verify SSL/TLS connections. These needed to be loaded using code.  

There was little standardization over where the OpenSSL DLLs were located. Applications tended to keep their own copies alongside other executables,
leading to multiple DLL copies. This in turn require changing the public variable `GSSL_DLL_DIR`, setting it to a specific directory before OpenSSL was loaded.  Likewise, the root CA bundle directories had to be distributed with applications and loaded with code.

ICS V9.1 and later allows five different ways of loading OpenSSL:

1. `.dll`s linked into application as resource files
2. `.dll`s loaded from common directory C:\ProgramData\ICS-OpenSSL\
3. OpenSSL `.dcu` linked into application using commercial YuOpenSSL
4. `.dll`s loaded from location specified in public variable `GSSL_DLL_DIR`
5. `.dll`s loaded according to path, may be found anywhere on PC

The method used to load OpenSSL `.dll`s is determined by several `{$DEFINE}`s located in the `.\Source\Include\OverbyteIcsDefs.inc` file. These are discussed in the sections that follow.