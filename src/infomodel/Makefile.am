##  Copyright 2018-2025 Carnegie Mellon University.
##  See license information in LICENSE.txt.

##  Process this file with automake to produce Makefile.in
##  ------------------------------------------------------------------------
##  Makefile.am (infomodel)
##  autotools build system for libfixbuf
##  ------------------------------------------------------------------------
##  @DISTRIBUTION_STATEMENT_BEGIN@
##  libfixbuf 2.5
##
##  Copyright 2024 Carnegie Mellon University.
##
##  NO WARRANTY. THIS CARNEGIE MELLON UNIVERSITY AND SOFTWARE ENGINEERING
##  INSTITUTE MATERIAL IS FURNISHED ON AN "AS-IS" BASIS. CARNEGIE MELLON
##  UNIVERSITY MAKES NO WARRANTIES OF ANY KIND, EITHER EXPRESSED OR
##  IMPLIED, AS TO ANY MATTER INCLUDING, BUT NOT LIMITED TO, WARRANTY OF
##  FITNESS FOR PURPOSE OR MERCHANTABILITY, EXCLUSIVITY, OR RESULTS
##  OBTAINED FROM USE OF THE MATERIAL. CARNEGIE MELLON UNIVERSITY DOES NOT
##  MAKE ANY WARRANTY OF ANY KIND WITH RESPECT TO FREEDOM FROM PATENT,
##  TRADEMARK, OR COPYRIGHT INFRINGEMENT.
##
##  Licensed under a GNU-Lesser GPL 3.0-style license, please see
##  LICENSE.txt or contact permission@sei.cmu.edu for full terms.
##
##  [DISTRIBUTION STATEMENT A] This material has been approved for public
##  release and unlimited distribution.  Please see Copyright notice for
##  non-US Government use and distribution.
##
##  This Software includes and/or makes use of Third-Party Software each
##  subject to its own license.
##
##  DM24-1020
##  @DISTRIBUTION_STATEMENT_END@
##  ------------------------------------------------------------------------

BUILT_SOURCES = $(INFOMODEL_REGISTRY_INCLUDE_FILES)
EXTRA_DIST = $(INFOMODEL_REGISTRIES) $(INFOMODEL_REGISTRY_INCLUDE_FILES)

$(INFOMODEL_REGISTRY_INCLUDE_FILES): $(srcdir)/../xml2fixbuf.xslt
SUFFIXES = .xml .i
.xml.i:
	$(AM_V_GEN) $(XSLTPROC) --stringparam array-name infomodel_array_static_$* -o $@ $(srcdir)/../xml2fixbuf.xslt $<
