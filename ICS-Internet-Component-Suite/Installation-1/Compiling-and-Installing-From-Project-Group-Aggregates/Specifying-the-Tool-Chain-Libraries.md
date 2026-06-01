After building the packages and installing them on the Tool Pallet they must be made available for use by software that employs them. To do this, the libraries specified in the tool chains must be updated to include the newliy installed packages and other code.

##### Delphi XE and Earlier
Use `Tools`→`Options`→`Delphi Options`→`Library`→`Win32`→`Library Path`, and add the `.\Lib` subdirectory according to version, i.e. `.\Lib\Debug\Win32\D2007` for Delphi 2007, replacing the first `.` with the install directory, if not done previously.  If you modify the ICS source files, also add `.\Source`.

##### Delphi XE2 and Later
Separate Win32 and Win64 paths must be specified. Use `Tools`→`Options`→`Language`→`Delphi`→`Library`→`32-bit` or `64-bit`, then add the `.\Lib` directory according to version,  i.e. `.\Lib\Debug\Win64\D103` for Delphi 10.3 64-bit, or `.\Lib\Debug\Win32\23.0` for Delphi12 32-bit. 

:::note
Note Delphi 10.4 and later use release studio version, so 21.0 for 10.4, 22.0 for Delphi 11, 11.1, 11.2 and 11.3, and 23.0 for Delphi 12, 12.1, 12.2, 12.3 etc.
:::

##### RAD Studio 12 Update 3
This is also known as RAD Studio 12.3. RAD Studio 12 Update 3 adds a new 64-bit IDE. The design packages have Windows 64-bit as a target, allowing them to be installed into the 64-bit IDE.  The 32-bit IDE allows design packages to be built with target Windows 64-bit, but not installed.