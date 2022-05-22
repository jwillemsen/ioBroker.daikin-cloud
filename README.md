![Logo](admin/daikin-cloud.jpg)
# ioBroker.daikin-cloud

![Number of Installations](http://iobroker.live/badges/daikin-cloud-installed.svg)
![Number of Installations](http://iobroker.live/badges/daikin-cloud-stable.svg)
[![NPM version](http://img.shields.io/npm/v/iobroker.daikin-cloud.svg)](https://www.npmjs.com/package/iobroker.daikin-cloud)

![Test and Release](https://github.com/Apollon77/iobroker.daikin-cloud/workflows/Test%20and%20Release/badge.svg)
[![Translation status](https://weblate.iobroker.net/widgets/adapters/-/daikin-cloud/svg-badge.svg)](https://weblate.iobroker.net/engage/adapters/?utm_source=widget)
[![Downloads](https://img.shields.io/npm/dm/iobroker.daikin-cloud.svg)](https://www.npmjs.com/package/iobroker.daikin-cloud)

## daikin-cloud adapter for ioBroker

Control Daikin Devices that are only connected to the Daikin Cloud / the Onecta App. The adapter connects to the Daikin-Cloud and polls the data from there. 

**This adapter can be installed with the folloowing Node.js versions:**
* 12.19.0+
* 14.15.0+
* 16.13.0+
* Node.js 18 is currently NOT supported because the usen OAuth library do not support it!

## Compatibility

This adapter should be compatible to devices with the Daikin WLAN-Adapters **BRP069C4x** that can be controlled via the Daikin Onecta App. A local connection to these devices is not possible!

Note: For devices with older WLAN-Adapters like **BRP069A4x** which can only be used by the Daikin Controller App please use the [Daikin](https://github.com/Apollon77/ioBroker.daikin) adapter instead.

## Functionality

The newer Daikin devices sold since 2020 contain a newer Wifi Adapter (e.g. BRP069C4x) which only connects to the Daikin Cloud and is no longer reachable locally. These devices are only controllable with the Daikin Onecta App.

This adapter allows to initially (hopefully once) retrieve tokens by using a proxy to login to the Daikin Cloud. After that these tokens can be used and refreshed to interact with teh devices.

**For more information on the Proxy progress for end users - because you need to trust and whitelist them and such - can be found in [PROXY.md](PROXY.md)!**
Info: This project is not grabbing any username or password, just the created tokens after you logged in. This also means that, if Daikin reset tokens or they expire that you need to do this process again!

After connecting to the Daikin Cloud account the adapter will automatically create a new device for each device that is connected to the Daikin Cloud. All available data are displayed and several states allow to control the device.
**Please note that the command speed of the Daikin cloud is not mega fast which means that it can take up to 3 minutes before the command is really executed or states are updated!**

## Changelog

### __WORK IN PROGRESS__
* (Apollon77) initial release

## Disclaimer
**Daikin is a trademark of DAIKIN INDUSTRIES, LTD. I am in no way endorsed by or affiliated with DAIKIN INDUSTRIES, LTD., or any associated subsidiaries, logos or trademarks. This personal project is maintained in spare time.**

## License
MIT License

Copyright (c) 2022 Apollon77 <iobroker@fischer-ka.de>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
