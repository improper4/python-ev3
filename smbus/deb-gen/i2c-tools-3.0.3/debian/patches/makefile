Description: <short summary of the patch>
 TODO: Put a short summary on the line above and replace this paragraph
 with a longer explanation of this change. Complete the meta-information
 with other relevant fields (see below for details). To make it easier, the
 information below has been extracted from the changelog. Adjust it or drop
 it.
 .
 i2c-tools (3.0.3-5build1) precise; urgency=low
 .
   * Rebuild to drop python2.6 dependencies.
Author: Matthias Klose <doko@ubuntu.com>

---
The information above should follow the Patch Tagging Guidelines, please
checkout http://dep.debian.net/deps/dep3/ to learn about the format. Here
are templates for supplementary fields that you might want to add:

Origin: <vendor|upstream|other>, <url of original patch>
Bug: <url in upstream bugtracker>
Bug-Debian: http://bugs.debian.org/<bugnumber>
Bug-Ubuntu: https://launchpad.net/bugs/<bugnumber>
Forwarded: <no|not-needed|url proving that it has been forwarded>
Reviewed-By: <name and email of someone who approved the patch>
Last-Update: <YYYY-MM-DD>

--- /dev/null
+++ i2c-tools-3.0.3/Makefile
@@ -0,0 +1,40 @@
+# I2C tools for Linux
+#
+# Copyright (C) 2007  Jean Delvare <khali@linux-fr.org>
+#
+# This program is free software; you can redistribute it and/or modify
+# it under the terms of the GNU General Public License as published by
+# the Free Software Foundation; either version 2 of the License, or
+# (at your option) any later version.
+
+DESTDIR	=
+prefix	= /usr/local
+bindir	= $(prefix)/bin
+sbindir	= $(prefix)/sbin
+mandir	= $(prefix)/share/man
+man8dir	= $(mandir)/man8
+incdir	= $(prefix)/include
+
+INSTALL		:= install
+INSTALL_DATA	:= $(INSTALL) -m 644
+INSTALL_DIR	:= $(INSTALL) -m 755 -d
+INSTALL_PROGRAM	:= $(INSTALL) -m 755
+RM		:= rm -f
+
+CC	?= gcc
+
+CFLAGS	?= -O2
+# When debugging, use the following instead
+#CFLAGS	:= -O -g
+CFLAGS	+= -Wall
+
+KERNELVERSION	:= $(shell uname -r)
+
+.PHONY: all strip clean install uninstall
+
+all:
+
+EXTRA	:=
+#EXTRA	+= py-smbus
+SRCDIRS	:= $(EXTRA)
+include $(SRCDIRS:%=%/Module.mk)
