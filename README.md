encrypt
=======

Script to reduce directory encryption to a simple, single-step
process.

The executable Bash scripts 'encrypt' and 'decrypt' can be run
as-is. The most convenient way to do so is to place both 'encrypt' and
'decrypt' into /usr/local/bin, or any other directory on your path. If
necessary, chmod +x both of them.

Step by step:
chmod +x encrypt decrypt
sudo cp encrypt decrypt /usr/local/bin

Copyright (C) 2014 Ivo Vegter
Licensed under GNU GPL v3.0

=======================================================================

Encrypts a directory, or decrypts a previously encrypted directory.
Wraps the underlying works into two simple commands:

encrypt <directory> 
- encrypt the contents of <directory>. This is slow the first time it
  is done. 
encrypt -d <directory> OR decrypt <directory>
- decrypt the contents of a previously encrypted <directory>, and make
  it available as clear-text in <directory>.clear

By default, the initial encryption will securely wipe the original
unencrypted contents. This is extra slow, so there is an -f option to
skip this step.

It will pause to ask for the encyption passphrase, when required. It
handles most real-world situations gracefully, to make its use as
intuitive as possible.

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or (at
your option) any later version.

This program is distributed in the hope that it will be useful, but
WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
General Public License for more details.

A copy of the full GNU General Public Licence can be found at:
http://www.gnu.org/licenses/
