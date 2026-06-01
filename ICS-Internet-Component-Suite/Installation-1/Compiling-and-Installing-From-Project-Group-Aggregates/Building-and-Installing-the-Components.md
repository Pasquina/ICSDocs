1. Do a `File/Open Project`, navigate to the `Install` directory that was determined based on your intentions and compiler level. Select the correct project file and open it. The project manager view should now display various package projects, some run-time and some design-time package. The run-time package name contains the `Run` suffix. The design-time package name contains the `Design` suffix. There are two ways you can build the necessary packages:
    * **`Select` and `Build` each package for each platform and build configuration required, usually four times:**  Note the Common package must always be built and installed, in addition to VCL or FMX, or both.
    * **Alternate Build Method:** `Click the Show Build Groups` Pane button, select an `Active Group` and click `Build the current project` group which builds all packages for all platforms and configurations together.

1. Select and Install the design-time packages one at a time. After a few seconds, you should have a dialog box telling you the package has been installed with a bunch of new components registered in the Tool Palette under **Overbyte ICS** and **Overbyte ICS SSL**. 
2. Then do a `Save All` and a `Close All`.

:::tip
Two or three packages should now appear in the Delphi Packages list, called **Overbyte ICS Common/|  FMX/VCL Design-Time Package for Delphi**.
:::

:::note
The packages all have `Post-build events` to copy install files around, and sometimes these may give errors during building, if these files can not be found or certain directories are missing.  This does not means the packages are not built correctly, just that some things may not work as expected.  Specifically, the Common packages copies all files from `.\ICS-OpenSSL` to `c:\ProgramData\ICS-OpenSSL\` and may fail if running applications are using OpenSSL files in that directory.  The VCL and FMX packages copy two `.DFM` files from the `.\Source directory` to `.\Lib` so they can be found later.
:::