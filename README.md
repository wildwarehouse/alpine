# This file is part of alpine.
#
#    alpine is free software: you can redistribute it and/or modify
#    it under the terms of the GNU General Public License as published by
#    the Free Software Foundation, either version 3 of the License, or
#    (at your option) any later version.
#
#    alpine is distributed in the hope that it will be useful,
#    but WITHOUT ANY WARRANTY; without even the implied warranty of
#    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
#    GNU General Public License for more details.
#
#    You should have received a copy of the GNU General Public License
#    along with alpine .  If not, see <http://www.gnu.org/licenses/>.

alpine is just an extension to the alpine base image.

It has

1. sudo
2. a 'user' user

Usage:

1. Create a 'sbin' directory with a '${NAME}.sh' script that would require sudo.
2. Create a 'sudo' directory with a file '${NAME}' with content like `user ALL=(ALL) NOPASSWD: /usr/local/sbin/${NAME}.sh`
3. Create a 'bin' directory with a file '${NAME}' with content `#!/bin/sh  sudo /usr/local/sbin/${NAME}.sh`