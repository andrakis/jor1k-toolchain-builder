jor1k-toolchain-builder
=======================

These scripts should help to build the experimental toolchain, programs and libraries for the openrisc or1k processor.
The final goal is to build an bootable image with a number of tools available for further development.

Parts are based on the book "Linux from Scratch"

TOOLCHAIN
---------

1. Edit the top lines of the Makefile
2. Execute
	make info (check and change in Makefile)
	make init
	make fetchtoolchain
	make checktoolchain
	make toolchain
	make or1ksim (installed in /usr/local)

To work with this toolchain execute
	make env
and execute the commands printed

KERNEL
------
Execute following commands
	make kernel

Progs and Libs
--------------

To get a list of available programs and libraries look at scripts/progs.make
	make fetchprogs (unfortunately this does not work at the moment. You have to download the programs by yourself in the downloads folder)
	make progs


Native Building Tools
---------------------
	make buildtools


DirectFB
--------
	make progs (if not already done so)
	make buildtools (if not already done so)
	make DirectFB 
	make DirectFB_Examples

X11
---
	make progs (if not already done so)
	make buildtools (if not already done so)
	make xpre
	make xproto
	make xlibs
	make xlibs2
	make xfonts
	make Mesa
	make xorg-server
	make xapps


Image
-----

Execute following commands
	make buildimage
	