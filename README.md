# screensaver.cpblobs addon for Kodi

This is a [Kodi](http://kodi.tv) screensaver addon.

[![Build Status](https://travis-ci.org/xbmc/screensaver.cpblobs.svg?branch=Matrix)](https://travis-ci.org/xbmc/screensaver.cpblobs/branches)
[![Build Status](https://dev.azure.com/teamkodi/binary-addons/_apis/build/status/xbmc.screensaver.cpblobs?branchName=Matrix)](https://dev.azure.com/teamkodi/binary-addons/_build/latest?definitionId=43&branchName=Matrix)
<!--- [![Build Status](https://ci.appveyor.com/api/projects/status/github/xbmc/screensaver.cpblobs?branch=Matrix&svg=true)](https://ci.appveyor.com/project/xbmc/screensaver-cpblobs?branch=Matrix) -->

## Build instructions

When building the addon you have to use the correct branch depending on which version of Kodi you're building against.
If you want to build the addon to be compatible with the latest kodi `master` commit, you need to checkout the branch with the current kodi codename.
Also make sure you follow this README from the branch in question.

### Linux

The following instructions assume you will have built Kodi already in the `kodi-build` directory 
suggested by the README.

1. `git clone --branch master https://github.com/xbmc/xbmc.git`
2. `git clone https://github.com/xbmc/screensaver.cpblobs.git`
3. `cd screensaver.cpblobs && mkdir build && cd build`
4. `cmake -DADDONS_TO_BUILD=screensaver.cpblobs -DADDON_SRC_PREFIX=../.. -DCMAKE_BUILD_TYPE=Debug -DCMAKE_INSTALL_PREFIX=../../xbmc/kodi-build/addons -DPACKAGE_ZIP=1 ../../xbmc/cmake/addons`
5. `make`

The addon files will be placed in `../../xbmc/kodi-build/addons` so if you build Kodi from source and run it directly 
the addon will be available as a system addon.
