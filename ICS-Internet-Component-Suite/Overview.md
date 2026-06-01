### Colophon:
* Revised: May 16, 2026
* Release: V9.7
* https://www.overbyte.eu/
* https://wiki.overbyte.eu/
* https://svn.overbyte.be/svn/


ICS is a free internet component library for all Delphi, C++Builder, BDS and RAD Studio versions.
It includes TCP, UDP, raw sockets, clients, servers, as well as all the main high level protocols
such as FTP, SMTP, POP3, NNTP, HTTP and more. ICS also supports SSL/TLS with the help of OpenSSL.

Includes OpenSSL 3.5.6, 3.6.2 and 4.0.0 for Win32 and Win64. Defaults to 3.6.2.


### UPGRADE TO V9.1 AND LATER WARNINGS

https://wiki.overbyte.eu/wiki/index.php/Updating_projects_to_V9.1

There are a lot of changes between ICS V8/V9.0, and ICS V9.1 and later, and some
less major changes with ICS V9.3 that will require OverbyteIcsTypes being added to
most applications.

Opening project forms with the IDE should automatically add any new units required,
but OverbyteIcsTypes and OverbyteIcsSslBase may need adding manually if ICS components
are created in code.

Installation for Delphi 10.4 and later all now use the same install groups and projects,
and may need the library path updating for versions, you must uninstall earlier packages
before installing new packages, due to the package names having changed.

The default location for the OpenSSL DLLs has moved.

There are several new DEFINES relating to building SSL/TLS applications that need adding to
the OverbyteIcsDefs.inc file, if it is not replaced during installation.

All the samples are in new directories, many old samples have been archived.

More details below.


### Table of contents:

- Legal issues
- Donate
- Register
- Contributions
- Support
- Latest Versions
- Version Control repository
- Platforms and Targets
- Installation
- SSL/TLS Optional DEFINES
- 'ICS Root CA' Certificate
- SSL/TLS Updating to V9.1 and later
- SSL/TLS Downloads
- Available VCL Components
- Delphi Windows sample applications:
- Getting Started with ICS
- Release notes
- Midware


### Legal issues:
```text
              Copyright (C) 1997-2026 by François PIETTE
              Rue de Grady 24, 4053 Embourg, Belgium
              <francois.piette@overbyte.be>

              SSL implementation includes code written by Arno Garrels,
              Berlin, Germany

              ICS is freeware.

              This software is provided 'as-is', without any express or
              implied warranty. In no event will the author be held liable
              for any damages arising from the use of this software.

              Permission is granted to anyone to use this software for any
              purpose, including commercial applications, and to alter it
              and redistribute it freely, subject to the following
              restrictions:

              1. The origin of this software must not be misrepresented,
                 you must not claim that you wrote the original software.
                 If you use this software in a product, an acknowledgment
                 in the product documentation would be appreciated but is
                 not required.

              1. Altered source versions must be plainly marked as such, and
                 must not be misrepresented as being the original software.

              1. This notice may not be removed or altered from any source
                 distribution.

              1. You must register this software by sending a picture postcard
                 to the author. Use a nice stamp and mention your name, street
                 address, EMail address and any comment you like to say.

              1. As this code make use of OpenSSL, your rights are restricted
                 by OpenSSL license as soon as you use any SSL feature.
                 See http://www.openssl.org for details.
```                 


### Donate

ICS is freeware. You can use it without paying anything except the registration
postcard (see "register" below). But of course donations are welcome. You can
send cash (Euro currency or US Dollars) in an envelop to my street address or
buy a gift certificate at Amazon in the UK. I will then use it to buy books.
Here is the direct URL at Amazon UK (nearest to my home, please don't use another):
http://www.amazon.co.uk/exec/obidos/gc-email-order1/ref=g_gc_email/202-6198323-6681414
For more generous amount, contact me by email.


###  Register

ICS is freeware. If you use the components, you must register by sending a
picture postcard showing the area you live in and some beautiful stamps for
my kids who are stamp collectors. Do not use an envelop, I collect USED
postcards sent to me. Write on the postcard that it is your ICS registration.

Address your card to: Francois PIETTE, rue de Grady 24, 4053 Embourg, Belgium.
Don't forget to mention your name, street address, EMail and web site.


### Contributions:

ICS has been designed by François PIETTE but many other peoples are working on the
components and sample programs. The history of changes in each source file list
all developers having contributed (When no name is given, the change is by F. Piette).
I can't list all contributors here but I want to specially thanks two specially active
contributors:

- Arno Garrels
- Angus Robertson <angus@magsys.co.uk>


### Support:

A new web support forum was created for ICS in February 2019:

https://en.delphipraxis.net/forum/37-ics-internet-component-suite/

Once registered, it is possible to follow a forum with email messages for new
posts, or a daily summary like the old mailing list.


### Latest versions:

The latest versions of ICS can be downloaded from the ICS Wiki web site:

https://wiki.overbyte.eu/wiki/index.php/ICS_Download

ICS V5, V6, V7 and V8 are archive releases no longer updated or supported.

ICS V9 is the long term support release which is held in a public Version Control
repository that is zipped each night for easy download.  The download page above
also includes the OpenSSL binaries needed to support SSL. ICS V9 supports Delphi
64-bit and Mac OS-X projects.  Note that C++ Builder versions supported are 10.4
and later.  Beware Mac OS-X and C++ have not been tested recently due to lack of
support from such users.

The latest released version is V9.4 which will be reported by the CopyRight constant
in OverbyteIcsWSocket.pas and the integer WSocketVersion as 904.

ICS V10 is in early development and is planned to support Android and Linux Server.
There are no current plans for ICS for iOS or MacOS.


### Version Control repository:

svn://svn.overbyte.be/ or https://svn.overbyte.be/svn/

There are several repositores, icsv9 is the latest release, icsdev contains some
older samples and other ICS tools, ddservice is needed for two ICS Windows service
samples.

:::info
(Usercode = ics, password = ics)
:::


### Platforms and Targets

The latest version of ICS supports Windows 32-bit and 64-bit targets using VCL and FMX
components.  Note MacOS is no longer supported due to lack ot testing and support.
Some users have reported problems with Delphi 2009, unfortunately we can not test and
fix compiler specific problems with some out of support compilers, although Delphi 2007 is still regularly tested for backward compatibility, Delphi 7 less often.

Testing of ICS is primarily with Windows 11 and Server 2022 and 2025, also Windows 10.
Note that Windows XP is not supported and SSL will not work. Windows 7, 8 and Server
2008 R2 and Server 2012 and 2019 are still be supported but testing is minimal.