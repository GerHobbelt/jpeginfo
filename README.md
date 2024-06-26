
Jpeginfo v1.7.1  Copyright (c) 1995-2023, Timo Kokkonen.

SYNOPSIS
    Prints information and tests integrity of JPEG/JFIF files.


REQUIREMENTS
	Independent JPEG Group's jpeg library (libjpeg) version 6b or later.
	(Alternatively should also work with libjpeg-turbo or mozjpeg)

TESTED PLATFORMS
	Linux
	MacOS
	Solaris *
        IRIX *
	HP-UX *

	*) No longer actively tested on these operating systems.

INSTALLATION
	Installation should be very straightforward, just unpack the
	tar file, run configure script, and then compile the program.
	You may want to do something like this:

		gunzip -c jpeginfo-1.7.1.tar.gz | tar xf -
		cd jpeginfo-1.7.1
		./configure
		make
		make strip
		make install

	NOTE! if 'configure' cannot find libjpeg.a or jpeglib.h, then
	you must use the --with-jpeglib option when running configure,
	see 'configure --help'.


HISTORY
	v1.7.1 - Add --files-from and --files-stdin options,
	         fix -j option,
		 lot of code cleanup by Kurt Schwehr,
	         other minor fixes.
        v1.7.0 - support for CSV output (--csv),
	         support for JSON output (--json),
	         add support for reading input file from stdin (--stdin),
		 add support for displaying column names (--header),
		 add SHA-512 sigest support (--sha512),
	         other minor fixes.
	v1.6.2 - add SHA-256 digest support (--sha256 or -2),
	         improved Win32 support thanks to tumagonx,
		 other minor fixes.
	v1.6.1 - support for new libjpeg v7 thanks to Guido Vollbeding,
		 fix to display of 8bit characters by Pierre Jarillon
	v1.6.0 - added support for printing out Comments (from COM
	         markers), Exif format images are now also recognized
	         (no Exif marker decoding functionality, though).
	v1.5   - configuration is now done with GNU autoconf,
		 program now uses free MD5 algorithm,
		 added file size as new field on reports,
		 program now returns exit code 1 if one or more of the jpegs
		 had any errors, useful for testing if particular jpeg is
	         ok from shell scripts,
	         also if you specify -q (--quiet) option twice on
		 command line, then program won't produce any output.
	v1.4   - added support for calculating MD5 checksums.
	v1.3   - alternative listing format (-l switch) added.
	         new column on reports displaying whether jpeg is
		 progressive or normal (P/N).
		 new switch -i for printing out even more information
	         about pictures: coding, density, CCIR601 sampling.
	         new switch -f for passing filenames to program from
	         file or stdin.
	v1.2   - improved support for other platforms, minor fixes
        v1.1.2 - small fixes, improvements to Makefile
	v1.1   - modified to use Independent JPEG Group's new v.6a library,
		 minor fixes.
	v1.0   - first public release


LATEST VERSION

	Latest version is always available from:
		http://www.iki.fi/tjko/projects.html


ACKNOWLEDGEMENT

	- MD5 message-digest allgorithm used is public domain implementation
	  written by Colin Plumb.
	- SHA-2 message-digest algorithm used is public domain implementation
	  by D. J. Bernstein (from NaCl library).



Timo <tjko@iki.fi>
29-Oct-2023
