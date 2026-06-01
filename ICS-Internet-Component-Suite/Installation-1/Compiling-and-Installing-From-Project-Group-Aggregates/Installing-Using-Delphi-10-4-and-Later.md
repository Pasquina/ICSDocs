For Delphi 10.4, 11, 12, 13 and later, the same install groups and packages are used for all Delphi and C++ versions since these the support `$(Auto)` library suffix which causes packages to be built with the compiler version instead of the manually entered Delphi version needed for earlier compilers, thus requiring compiler specific packages.

| Delphi Version            | Project Group                      | Installation Type                                    |
|---------------------------|------------------------------------|------------------------------------------------------|
| Delphi 10.4/11/12/13      | IcsInstallVcl.groupproj            | VCL components for Windows                           |
| Delphi 10.4/11/12/13      | IcsInstallFmx.groupproj            | FMX components for Windows                           |
| Delphi 10.4/11/12/13      | IcsInstallVclFmx.groupproj         | VCL and FMX components for Windows                   |
| Delphi 10.4/11/12/13      | IcsInstallTestPosix.groupproj      | FMX test components for Android/Linux                |
| C++ Builder 10.4/11/12/13 | CBIcsInstallVclFmx.groupproj       | VCL and FMX components for Windows, Win32 and Win64  |
| C++ Builder 12.3/13       | CBIcsInstallVclFmxModern.groupproj | VCL and FMX components for Windows, Win32 and Win64x |

:::note
ICS includes design packages for Win32 and Win64, so may be used in the Delphi 64-bit IDE with Delphi 12.2, 12.3 and 13.   However `Win64x (Modern)` packages will not build in C++, so the C++ 64-bit IDE can not be used at the moment, pending a compiler improvement.
:::
:::warning
Delphi 10.41 and 10.42 (10.4 with updates 1 or 2) will install correctly with the above packages, the original RTM version does not support the package LIB suffix: `$(Auto)` so you must change it manually for each package to 21.0.
:::
:::warning
C++ Builder Win32 and Win64 packages should install correctly, but at the time of writing, the C++ Win64 Modern appears unable to require other C++ packages, so the design, VCL and FMX give link error due to not being able to find Common.
:::