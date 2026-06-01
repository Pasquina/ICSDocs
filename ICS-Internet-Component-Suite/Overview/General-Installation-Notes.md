ICS V9 has been designed for Embarcadero Delphi 2009 and up, and C++ Builder
2009 and up, but is mostly compatible with Borland Delphi 7 and CodeGear 2006 and 2007. Delphi 7 does not have TWebBrowser so the TOAuthLoginForm unit is missing
and samples needing it will fail..

:::warning
While ICS still includes packages for Delphi 7 and it should still work, we can no
longer regularly test changes against Delphi 7 so you may find incompatibilities
with ICS due to it's old syntax and libraries, please submit any corrections that
are needed for future releases. Many samples may fail to built without changes with
older compilers, too many changes over the years.
:::

Embarcadero RAD Studio includes Delphi and C++ Builder.

https://www.embarcadero.com/

With Delphi XE2 and later, VCL 64-bit Windows targets are supported for Delphi only.
Currently FireMonkey is partly supported for Delphi only (there are still a few
non-ported components). ICS for Mac OSX is currently experimental.

When extracting ICS from the zip file, the directory structure MUST be maintained,
otherwise you will be unable to use the install groups and library package projects
to correctly build ICS.

This is the V9.1 and later sub-directory layout:

| Directory Path                                | Content                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| .\                                            | Info directory                                                                                                                                                                                                                                                                             |
| .\Install                                     | Component packages project groups for all versions                                                                                                                                                                                                                                         |
| .\Packages                                    | Delphi (7 and up) and C++ builder (2006 and up)                                                                                                                                                                                                                                            |
| .\Source                                      | ICS Delphi source code built into packages                                                                                                                                                                                                                                                 |
| .\Source\Include                              |  .inc files (including OverbyteIcsDefs.inc)                                                                                                                                                                                                                                                |
| .\Source\zobj1212                             | ZLIB C OBJ include files                                                                                                                                                                                                                                                                   |
| .\ICS-OpenSSL                                 | OpenSSL DLLs, copied to c:\ProgramData\ICS-OpenSSL\ when building packages, including sub-directories.                                                                                                                                                                                     |
| .\ICS-OpenSSL\ICS-Certs                       | ICS SSL/TLS test certificates                                                                                                                                                                                                                                                              |
| .\ICS-OpenSSL\ICS-RootCAs                     | ICS SSL/TLS root certificate authority bundles                                                                                                                                                                                                                                             |
| .\Lib\$(Config)\$(Platform)\$(ProductVersion) | Unit output directories for all package builds, subdirectories created on building the packages, Release/  Debug, Win32/Win64/OSX64, D2007/D110//etc/21.0/22.0/23.0,                                       includes .dcu and .dfm files for Delphi and .obj and .hpp files for C++ Builder |
| .\demos-delphi-vcl                            |  VCL samples for Windows                                                                                                                                                                                                                                                                   |
| .\demos-delphi-extra                          | VCL samples that need third party components to build                                                                                                                                                                                                                                      |
| .\demos-delphi-fmx                            |  FMX samples for Windows                                                                                                                                                                                                                                                                   |
| .\demos-delphi-mobile                         | Empty, for the future                                                                                                                                                                                                                                                                      |
| .\demos-cpp-vcl                               | Old C++ samples that have not been tested for 10 years                                                                                                                                                                                                                                     |
| .\demos-data                                  | Data files for samples, such as web pages                                                                                                                                                                                                                                                  |

:::information
The .\ indicates the directory into which you extracted the ICS archive, your choice,
but avoid c:\program files due to file permissions.
Example directories could be c:\icsv9, c:\delpicomp\icsv9, etc.

Note the main change from ICS V9.0 and earlier is the Samples directory has been re-arranged
to make it easier to find useful samples in more sensibly named directories.
:::

:::tip
There are major directory and file changes between ICS V9.0 and earlier, and ICS V9.1
and later, hundreds of old files have been removed, and many files are in new directories.
It is strongly recommended the old install directory is renamed old or something, and
V9.1 or later is extracted to a clean directory, to avoid having a mix of old and new files.
:::