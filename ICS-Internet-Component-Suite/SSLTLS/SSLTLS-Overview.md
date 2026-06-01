ICS is distributed with the versions of OpenSSL that are currently supported and include currrent security fixes. OpenSSL versions 3.5, 3.6 and 4.0 include the latest patch
of each version; e.g.3.5.6, 3.6.2 and 4.0.0.

The resources files are located in `.\Source\LibV35OpenSSL32.res` for 3.5 Win32, and `.\Source\LibV40OpenSSL32.res` for 4.0 Win32. 64-bit versions are similarly handled.

ICS automatically links Win32 or Win64 `.res` files. 

:::note
Note the resource files only have the major OpenSSL version, 3 or 4. not the minor version, to avoid changing the file names for minor releases.
:::

ICS currently supports five different OpenSSL versions. OpenSSL 3.0 TLS is stable and
supported until September 2026, but it is essential to always use the latest sub-version
with security fixes.  OpenSSL 3.5 added Post Quantum (PQ) key negotiation, if that is
required, and the latest long term support release so will remain in ICS until April 2030.
ICS generally stops updating old versions a few months before their support ceases.  The
next planned LTS version is 4.2 in 2027.

:::note
OpenSSL plans two releases a year, each supported with security and bug fixes for 13 months, with one release each two years designated for five year long term support (LTS) security and bug fixes.
:::