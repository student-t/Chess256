# This file is part of Chess 256.
# 
# Copyright © 2018 Alexander Kernozhitsky <sh200105@mail.ru>
# 
# Chess 256 is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
# 
# Chess 256 is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
# 
# You should have received a copy of the GNU General Public License
# along with Chess 256.  If not, see <http://www.gnu.org/licenses/>.

.PHONY: build clean install

PREFIX = $(DESTDIR)/usr/local

DIRS := Design Glyphs Icons
DIRS_BUILD := $(DIRS:%=%-build)
DIRS_CLEAN := $(DIRS:%=%-clean)

build: $(DIRS_BUILD)
clean: $(DIRS_CLEAN)

install:
	+cd Icons && make install PREFIX=$(PREFIX)

.PHONY: $(DIRS_BUILD) $(DIRS_CLEAN)

$(DIRS_BUILD):
	+cd $(@:%-build=%) && make build

$(DIRS_CLEAN):
	+cd $(@:%-clean=%) && make clean
