<img align="right" width="250" height="47" src="graphics/Gematik_Logo_Flag_With_Background.png"/><br/>

# Introduction

This repository contains data to be imported into an [eHC-Hash-Database][] of a
[PoPP-Service][].
Among other ways it is possible to import data into that [eHC-Hash-Database][]
as described in [clause 6.1.1.9.4][].

## Installation

Currently, this project contains information to be used by implementors or
testers of PoPP-Service.
Thus, this project needs no installation.

## Usage

Signed messages from this repository can be delivered to PoPP-Service as
described in [A_27045][].
For this purpose this repository contains the following directories:
1. **import**: This directory contains signed _eContent_ where all _egkInfo_
   structures (described in [A_27045][]) have _status = 0 = import_.
2. **remove**: This directory contains signed _eContent_ where all _egkInfo_
   structures (described in [A_27045][]) have _status = 1 = remove_.

Typically, the data from a test-eHC (Test-eGK) is available four times, i.e.
the data from a test-eHC is present in four _egkInfo_ according to [A_27045][]:
1. **single import**: Folder "import" contains a file for the eHC, where the
   ICCSN of the eHC is the name prefix.
2. **single remove**: Folder "remove" contains a file for the eHC, where the
   ICCSN of the eHC is the name prefix.
3. **bulk import**: File "import/_all.eContent-signed" contains the _egkInfo_
   for that eHC together with _egkInfo_ from a lot of other eHC.
4. **bulk remove**: File "remove/_all.eContent-signed" contains the _egkInfo_
   for that eHC together with _egkInfo_ from a lot of other eHC.

## Support

For support contact
[software-development@gematik.de](mailto:software-development@gematik.de).

## Roadmap

Currently, there are just a few signed messages available.
On request and over time more signed messages may be added.

## Contributing

See the [CONTRIBUTING](./CONTRIBUTING.md) file.

## License

Copyright 2025 gematik GmbH

Apache License, Version 2.0

See the [LICENSE](./LICENSE) for the specific language governing permissions and
limitations under the License.

## Additional Notes and Disclaimer from gematik GmbH

1. Copyright notice: Each published work result is accompanied by an explicit
   statement of the license conditions for use. These are regularly typical
   conditions in connection with open source or free software. Programs
   described/provided/linked here are free software, unless otherwise stated.
2. Permission notice: Permission is hereby granted, free of charge, to any
   person obtaining a copy of this software and associated documentation files
   (the "Software"), to deal in the Software without restriction, including
   without limitation the rights to use, copy, modify, merge, publish,
   distribute, sublicense, and/or sell copies of the Software, and to permit
   persons to whom the Software is furnished to do so, subject to the following
   conditions:
   1. The copyright notice (Item 1) and the permission notice (Item 2) shall be
      included in all copies or substantial portions of the Software.
   2. The software is provided "as is" without warranty of any kind, either
      express or implied, including, but not limited to, the warranties of
      fitness for a particular purpose, merchantability, and/or non-infringement.
      The authors or copyright holders shall not be liable in any manner
      whatsoever for any damages or other claims arising from, out of or in
      connection with the software or the use or other dealings with the
      software, whether in an action of contract, tort, or otherwise.
   3. The software is the result of research and development activities,
      therefore not necessarily quality assured and without the character of a
      liable product. For this reason, gematik does not provide any support or
      other user assistance (unless otherwise stated in individual cases and
      without justification of a legal obligation). Furthermore, there is no
      claim to further development and adaptation of the results to a more
      current state of the art.
3. Gematik may remove published results temporarily or permanently from the
   place of publication at any time without prior notice or justification.
4. Please note: Parts of this code may have been generated using AI-supported
   technology. Please take this into account, especially when troubleshooting,
   for security analyses and possible adjustments.

## Changelog

See the [CHANGELOG](./CHANGELOG.md) file.

## Project status

This project is active.


[A_27045]:https://gemspec.gematik.de/prereleases/Draft_PoPP_25_2/gemSpec_PoPP_Service_V1.0.0_CC3/#A_27045
[PoPP-Service]:https://gemspec.gematik.de/prereleases/Draft_PoPP_25_2/gemSpec_PoPP_Service_V1.0.0_CC3/
[clause 6.1.1.9.4]:https://gemspec.gematik.de/prereleases/Draft_PoPP_25_2/gemSpec_PoPP_Service_V1.0.0_CC3/#6.1.1.9.4
[eHC-Hash-Database]:https://gemspec.gematik.de/prereleases/Draft_PoPP_25_2/gemSpec_PoPP_Service_V1.0.0_CC3/#6.1.1.9
