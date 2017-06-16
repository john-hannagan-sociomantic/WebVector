WebVector
=========
An HTML to SVG or PNG convertor
(c) 2009-2015 Radek Burget (burgetr@fit.vutbr.cz)

See the project page for more information and downloads:
[http://cssbox.sourceforge.net/webvector](http://cssbox.sourceforge.net/webvector)

All the source code of the WebVector itself is licensed under the GNU Lesser General
Public License (LGPL), version 3. A copy of the LGPL can be found
in the LICENSE file.

WebVector is based on the
[CSSBox rendering engine](http://cssbox.sourceforge.net/).

Build Instructions
==================

1. Clone this repository into a directory ie. `projects/webvector`
1. Clone the [CSSBox fork](https://github.com/john-hannagan-sociomantic/CSSBox) into a neighbouring directory called `cssbox`, ie. `projects/cssbox`
1. Make sure you've installed your own build version of CSSBoxPDF found at: https://github.com/radkovo/CSSBoxPdf
   - For some reason this isn't on the main maven package repo, so you ahve to build it locally and add the package.
1. Build CSSbox using `mvn install; mvn package`.
1. Build Webvector using `mvn clean; mvn install; mvn package` to build a new jar file with any changes

Modifying the CSSBox lib
========================

When making changes to the CSSBox lib, you must follow these steps to ensure that the new jar is packaged into this project correctly:
1. Build CSSBox: `projects/cssbox > mvn package`
1. Run clean in webvector: `projects/webvector > mvn clean`
1. Run package in webvector: `projects/webvector > mvn package`