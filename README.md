Baidu Maps Download
===================

Download Baidu Maps to one PNG image file.

Usage
-----

### Download map pieces

Download map pieces to ``maps`` directory. The ``maps`` directory will be emptied each time excuting this script.

Start Point (``sp``) is the top-left point of the map while End Point (``ep``) is the bottom-right point.
Level ranges from 1 to 19 and defaults to 12. Higher level means a more detailed map with more image pieces to be downloaded.
Type can be ``web`` (default), ``web-alt`` (bigger font size, good for printing and mobile browsing) or ``sate`` (satellite image).

    bash point2pieces.sh sp_x sp_y ep_x ep_y [level=12 [type=web]]

### Concatenate map pieces

Concatenate map pieces in ``maps`` directory to one PNG image file named ``done.png``. Map pieces and intermediate files will be deleted.

    bash pieces2one.sh

Example
-------

Download (part of) map of Guangzhou in one command:

    bash point2pieces.sh 12550000.00, 2650000.00 12650000.00, 2550000.00 && bash pieces2one.sh

Requirements
------------

* cURL
* ImageMagick
* bc

See Also
--------

* [Baidu Maps Coordinates Utils](https://github.com/caiguanhao/baidu-maps-coord-utils) (includes coordinates to point conversion)
* [BaiduMapsDownloader in Java](https://github.com/java-MagicWang/BaiduMapDownloader/blob/master/MapDownloader.java)

Developer
---------

* caiguanhao
