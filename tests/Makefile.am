#
# Copyright 2014 Red Hat, Inc.
#
# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 2 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301  USA
#
# Refer to the README and COPYING files for full details of the license
#

test_modules = \
	test_glustercli.py \
	test_storage.py \
	utilsTests.py \
	$(NULL)

dist_glusternagioscommontests_DATA = \
	xml2dictSuccess.xml \
	$(NULL)

dist_glusternagioscommontests_PYTHON = \
	$(test_modules) \
	testrunner.py \
	testValidation.py \
	$(NULL)

dist_glusternagioscommontests_SCRIPTS = \
	run_tests.sh \
	$(NULL)

dist_noinst_DATA = \
	run_tests_local.sh \
	$(NULL)

CLEANFILES = \
	$(NULL)

all-local: \
	$(nodist_glusternagioscommontests_PYTHON)

check-local:
	@echo '*** Running tests.  To skip this step place NOSE_EXCLUDE=.* ***'
	@echo '*** into your environment.  Do not submit untested code!    ***'
	$(top_srcdir)/tests/run_tests_local.sh $(test_modules)
