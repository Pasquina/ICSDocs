Once ICS is installed, you may open the sample projects. There are about 95 samples, split into several directories, each with a project group.

| Directory             | Sample Content                                         |
|-----------------------|--------------------------------------------------------|
| .\demos-delphi-vcl    | VCL samples for Windows                                |
| .\demos-delphi-extra  |  VCL samples that need third party components to build |
| .\demos-delphi-fmx    | FMX samples for Windows                                |
| .\demos-delphi-mobile | Empty, for the future                                  |
| .\demos-cpp-vcl       | Old C++ samples that have not been tested for 10 years |
| .\demos-data          | Data files for samples, such as web pages              |

Full details of the individual sample projects are shown later in this document.

Each directory has a group project file with the same name as the directory, that
includes all the projects in that directory, so `demos-delphi-vcl.groupproj` contains the main samples directory.  To compile all samples in the group at once, execute `Project→Build all projects`. This may take a few minutes.  For legacy compilers, open the `demos-delphi-vcl-legacy.bpg` project file instead, or `demos-delphi-vcl-legacy.groupproj`.

:::warning
The sample project files (`.dproj`) supplied are built with modern compilers,
and can not be opened by legacy compilers due to new platforms and features.  So
for Delphi XE and earlier (and maybe some other XE versions), before opening a
group or application project, you MUST delete all `.dproj` sample files.  When you
open the project, the `.dproj` file will be automatically recreated from the `.dpr`
project file by Delphi.  If you attempt to open a new `.dproj` file with a legacy
Delphi compiler, it will simply give an XML error and not attempt to rebuild the
project file.
:::
:::note
The C++ Builder packages and samples have not been updated for some years and are untested with V9.1 and later.  They are included here for existing users.
:::