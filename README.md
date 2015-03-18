----------------------------------------------
# mc_LJ
----------------------------------------------

C program for MC simulations applied to Lennard Jones clusters only.

[![Build Status](https://travis-ci.org/FHedin/mc_LJ.svg)](https://travis-ci.org/FHedin/mc_LJ)

<a href="https://scan.coverity.com/projects/4563">
  <img alt="Coverity Scan Build Status"
         src="https://scan.coverity.com/projects/4563/badge.svg"/>
</a>

----------------------------------------------
## COMPILE & INSTALL
----------------------------------------------
A C compiler compatible with the C99 standard or newer is required.

Be sure to have CMAKE installed (http://www.cmake.org/), available on most repositories.

Create a build directory and move to that directory: 
  * mkdir build && cd build

For buildind a debug or release (default) version : 
  * cmake -DCMAKE_BUILD_TYPE=Debug ..
  * cmake -DCMAKE_BUILD_TYPE=Release ..

Debug builds are slower but useful when debugging with gdb or valgrind.

Then, once cmake built a Makefile, just execute :
  * make

For a verbose make, use : 
  * make VERBOSE=1

Please never edit this autogenerated Makefile, edit the CMakeLists.txt instead.

For specifying another compiler on linux (for example clang or Intel icc): 
  * CC=clang cmake ..
  * CC=icc cmake ..
    
It is possible for the user to define custom energy functions using the Lua scripting language (http://www.lua.org/).
See input_file.inp and the ./plugins directory for more details.

For enabling Lua plugins files use when compiling: 
  * cmake -DUSE_LUA=1 ..

You will most probably have to edit the CMakeLists.txt file for adding paths to the Lua include and library directories.
For best performances you can use the LuaJIT implementation : http://luajit.org/

----------------------------------------------
## DOCUMENTATION
----------------------------------------------
Check the doc directory that contains programming documentation.

For updating the documentation, run doxygen in the current directory (http://www.doxygen.org)

----------------------------------------------
## LICENSING (all files excepted subdirectory dSFMT)
----------------------------------------------
Copyright (c) 2011-2015, Florent Hedin, Markus Meuwly, and the University of Basel.
All rights reserved.

The 3-clause BSD license is applied to this software.

See LICENSE.txt

----------------------------------------------
## NOTE CONCERNING dSFMT
----------------------------------------------
This project uses as random numbers generator the dSFMT code : 
http://www.math.sci.hiroshima-u.ac.jp/~m-mat/MT/SFMT/

All files in the subdirectory dSFMT are licensed with a 3-clause BSD license and copyrighted as following :
Copyright (C) 2007,2008 Mutsuo Saito, Makoto Matsumoto and Hiroshima
University. All rights reserved.

See dSFMT/LICENSE_dSFMT.txt

