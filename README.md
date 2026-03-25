# BigTIFF community standard candidate

This GitHub repository contains the content for an OGC Community Standard candidate for BigTIFF (OGC 21-061)

BigTIFF was originated outside the OGC and mainly maintained at https://www.awaresystems.be/imaging/tiff/bigtiff.html and the intention is that it becomes an OGC standard with the support of the community or an OGC community standard.  This repository reproduces the current status of the COG practices collected mainly from https://www.awaresystems.be/imaging/tiff/bigtiff.html and translates it into formal requirements and an OGC standards template.

This repository was originated from the work in Testbed 17 and the original documents are in https://gitlab.ogc.org/ogc/T17-D046-COG-Specification-ER/-/tree/master/standardDrafts/BigTIFF. The work continues in the GeoTIFF.SWG.

The repo is organized as follows:

* index.adoc - nothing in this document
* standard - the main Standard document content
  - organized in multiple sections and directories
  - this is the only part needed to create a Standard

This *candidate* standard is available in [HTML](https://docs.ogc.org/DRAFTS/21-061.html) and [PDF](https://docs.ogc.org/DRAFTS/21-061.pdf) formats.

## The standards

This repository contains a OGC Standard candidate that describes an extended internal structure for a image file that requires more than 4GBytes. The general structure is similar to the TIFF specification version 6 but it replaces two essential data structures called Image File Header and Image File Directory for new ones that support the necessary longer integer numbers that acts as internal offsets of the file. It also adds 3 new data types for very long integers. It is expected that other OGC standards, such as GeoTIFF, can support BigTIFF in the near future.

When the TIFF format was defined back in 1986 the storage capacity of the computers made difficult (or even impossible) for an single file image to be bigger than 4GBytes long. But today capacities makes it viable and if the file can be random accessed in small pieces, could be even useful to have a big remote sensing product in a single file.

The basic BigTIFF design was first proposed in 2004 and refined in (https://www.asmail.be/msg0055453930.html)[this discussion] (now only accessible in the web.archive.org) on the Aware Systems (https://www.awaresystems.be/)[Aware Systems] mailing list (now only available in the web.archive.org). Contributors to the design discussion included Lynn Quam, Frank Warmerdam, Chris Cox, Rob Tillaart, Dan Smith, Bob Freisenhahn, Andrey Kiselev, Phillip Crews, and Gerben Vos. The authors thank all those who came before them for creating libtiff and designing the BigTIFF enhancements.
The BigTIFF format was proposed in https://www.awaresystems.be/imaging/tiff/bigtiff.html maintained by Joris Van Damme and has been stable in recent years (now only accessible in the web.archive.org).

Changes were made by Ole Eichhorn (ole.eichhorn@gmail.com) while at (www.aperio.com)[Aperio] (now only accessible in the web.archive.org) and were donated to the public domain, in gratitude to Sam Leffler, Silicon Graphics, Joris Van Damme, Aware Systems, Frank Warmerdam, Andrey Kisley, Mike Welles, and all who have worked on libtiff over the years to provide this tool. These changes were published on an "as is" basis and neither Ole Eichhorn nor Aperio made any warranty as to their fitness for any intended use.

GeoTIFF 1.1 was brought to the OGC as a community standard but, in the process, was made dependent form the classical TIFF specification. This Standard brings BigTIFF to the OGC as another community standard. It is expected that Next version of GeoTIFF supports both Classical TIFF and  BigTIFF.

This document is an adaptation of the https://www.awaresystems.be/imaging/tiff/bigtiff.html content to an OGC language to bring it to the OGC standards process as a community standard. It was done with the intention of creating a transcription with no practical modifications, so old BigTIFF implementations would be compatible with this document.
