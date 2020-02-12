# QFakeGeoPositionSource
Qt/QML plugin and tools to fake on Linux a GPS device to be used by Qt/QML


## Description

As many, I did not own a GPS device and even if I did then I would not ever imagine walking in the streets of Paris to test Qt/QML positioning related apps.
Here comes the reason why I developed this Qt position plugin, so that I would be able to test my apps while staying home !

## Installation and usage

This plugin and these tools were meant to be compiled and used on Linux. Feel free to adapt them for other operating systems.

### Qt position plugin

The Qt plugin generated must be put int the QT_INSTALL_PATH/plugins/position/ folder (basically /usr/lib/qt/plugins/position/).

### fakesource

The fakesource is an executable opening a pseudo-tty (thanks to Linux pseudoterminal multiplexer /dev/ptmx) and writing coordinates updates to it.
Coordinates are generated by the QML GUI interface following a RouteModel at regular speed (start and end coordinates can be changed).

Just run it !

### example

The example is an executable opening a pseudo-tty (by default /dev/pts/2 but it can be changed in the QML file) and listening to incomming coordinates updates to move a POI on the Map from its QML GUI interface.

Just run it after fakesource is perfectly running !

## License

LGPL-3.0
See LICENSE file for more informations.

## Credits

https://stackoverflow.com/questions/49544318/using-linux-pseudoterminal-to-test-qserialport

https://github.com/qt/qtlocation/tree/dev/src/plugins/position/geoclue2

https://doc.qt.io/qt-5/qtlocation-mapviewer-example.html
