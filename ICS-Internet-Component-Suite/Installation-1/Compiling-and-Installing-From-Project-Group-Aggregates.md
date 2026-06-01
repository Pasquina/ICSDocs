Project Group Aggregates are projects that contain a set of projects which, taken together, provide for a complete installation of the related ICS version. They generally include
- Two run time .bpl projects
    - Common
    - Component
- Two design time .bpl projects
    - Common
    - Component

Hence, installation generally consists of building two run-time .bpl files and building and installing two design-time .bpl files.

In general, ICS provides three different install groups for compilers supporting both VCL and FMX, to allow individual installation, or both together. Howeever, there are specific differences depending on whether you're installing ICS and are using Delphi 10.4 or later, or version prior to Delphi 10.4. Those are explained in the sections that follow.

:::warning
    Uninstall an existing ICS package (`Menu→Component→Install Packages`, select the component package and click Remove).  If you skip uninstall for Delphi 10.4 and later updating from ICS V9.0 or earlier, you may get errors due to the package names having changed.
:::

1. Rename the old ICS directory and unzip to a new or empty directory.
2. Remove the old path from the library path. 
3. Add either the new .\Source directory to the library path under `Tools→Options...` or the appropriate .\Lib subdirectory according to version, ie .\Lib\Debug\Win32\D2007 for Delphi 2007. The latter has the advantage that the ICS source code won't be recompiled whenever your project is built.
4. Also under `Tools→Option...` add the new .\Source directory to the Browsing path.

#### Installing Using Delphi 10.4 and Later

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

#### Installing Using Installers Prior to Delphi 10.4:
If you are installing using compiler versions prior to Delphi 10.4, you must choose a project group that corresponds to your compiler version. The following options are provided:

| Delphi Version | Project Group               | Installation Type                  |
|----------------|-----------------------------|------------------------------------|
| Delphi 7       | D7Instdall.bpg              | VCL components for Windows         |
| Delphi 7       | D7Install.bpg               | VCL components for Windows         |
| Delphi 2006    | D2006Install.bdsgroup       | VCL components for Windows         |
| Delphi 2007    | D2007Install.groupproj      | VCL components for Windows         |
| Delphi 2009    | D2009Install.groupproj      | VCL components for Windows         |
| Delphi 2010    | D2010Install.groupproj      | VCL components for Windows         |
| Delphi XE      | DXeInstall.groupproj        | VCL components for Windows         |
| Delphi XE2     | DXe2InstallVcl.groupproj    | VCL components for Windows         |
| Delphi XE2     | DXe2InstallFmx.groupproj    | FMX components for Windows         |
| Delphi XE2     | DXe2InstallVclFmx.groupproj | VCL and FMX components for Windows |
| Delphi XE3     | DXe3InstallVcl.groupproj    | VCL components for Windows         |
| Delphi XE3     | DXe3InstallVclFmx.groupproj | FMX components for Windows         |
| Delphi XE3     | DXe3InstallVclFmx.groupproj | VCL and FMX components for Windows |
| Delphi XE4     | DXe4InstallVcl.groupproj    | VCL components for Windows         |
| Delphi XE4     | DXe4InstallFmx.groupproj    | FMX components for Windows         |
| Delphi XE4     | DXe4InstallVclFmx.groupproj | VCL and FMX components for Windows |
| Delphi XE5     | DXe5InstallVcl.groupproj    | VCL components for Windows         |
| Delphi XE5     | DXe5InstallFmx.groupproj    | FMX components for Windows         |
| Delphi XE5     | DXe5InstallVclFmx.groupproj | VCL and FMX components for Windows |
| Delphi XE6     | DXe6InstallVcl.groupproj    | VCL components for Windows         |
| Delphi XE6     | DXe6InstallFmx.groupproj    | FMX components for Windows         |
| Delphi XE6     | DXe6InstallVclFmx.groupproj | VCL and FMX components for Windows |
| Delphi XE7     | DXe7InstallVcl.groupproj    | VCL components for Windows         |
| Delphi XE7     | DXe7InstallFmx.groupproj    | FMX components for Windows         |
| Delphi XE7     | DXe7InstallVclFmx.groupproj | VCL and FMX components for Windows |
| Delphi XE8     | DXe8InstallVcl.groupproj    | VCL components for Windows         |
| Delphi XE8     | DXe8InstallFmx.groupproj    | FMX components for Windows         |
| Delphi XE8     | DXe8InstallVclFmx.groupproj | VCL and FMX components for Windows |
| Delphi 10      | D10SInstallVcl.groupproj    | VCL components for Windows         |
| Delphi 10      | D10SInstallFmx.groupproj    | FMX components for Windows         |
| Delphi 10      | D10SInstallVclFmx.groupproj | VCL and FMX components for Windows |
| Delphi 10.1    | D101InstallVcl.groupproj    | VCL components for Windows         |
| Delphi 10.1    | D101InstallFmx.groupproj    | FMX components for Windows         |
| Delphi 10.1    | D101InstallVclFmx.groupproj | VCL and FMX components for Windows |
| Delphi 10.2    | D102InstallVcl.groupproj    | VCL components for Windows         |
| Delphi 10.2    | D102InstallFmx.groupproj    | FMX components for Windows         |
| Delphi 10.2    | D102InstallVclFmx.groupproj | VCL and FMX components for Windows |
| Delphi 10.3    | D103InstallVcl.groupproj    | VCL components for Windows         |
| Delphi 10.3    | D103InstallFmx.groupproj    | FMX components for Windows         |
| Delphi 10.3    | D103InstallVclFmx.groupproj | VCL and FMX components for Windows |

:::note
Sorry, no C++ Builder install groups are available with V9.1 and later for older
compIlers than 10.4, you will need to use ICS V9.0 instead or create them yourself.
:::