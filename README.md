# visualization.waveform addon for Kodi

This is a [Kodi](http://kodi.tv) visualization addon.

[![Build Status](https://travis-ci.org/notspiff/visualization.waveform.svg?branch=master)](https://travis-ci.org/notspiff/visualization.waveform)
[![Build Status](https://ci.appveyor.com/api/projects/status/github/notspiff/visualization.waveform?svg=true)](https://ci.appveyor.com/project/notspiff/visualization-waveform)

## Build instructions

When building the addon you have to use the correct branch depending on which version of Kodi you're building against. 
For example, if you're building the `master` branch of Kodi you should checkout the `master` branch of this repository. 
Also make sure you follow this README from the branch in question.

### Linux

The following instructions assume you will have built Kodi already in the `kodi-build` directory 
suggested by the README.

1. `git clone https://github.com/xbmc/xbmc.git`
2. `git clone https://github.com/notspiff/visualization.waveform.git`
3. `cd visualization.waveform && mkdir build && cd build`
4. `cmake -DADDONS_TO_BUILD=visualization.waveform -DADDON_SRC_PREFIX=../.. -DCMAKE_BUILD_TYPE=Debug -DCMAKE_INSTALL_PREFIX=../../xbmc/kodi-build/addons -DPACKAGE_ZIP=1 ../../xbmc/cmake/addons`
5. `make`

The addon files will be placed in `../../xbmc/kodi-build/addons` so if you build Kodi from source and run it directly 
the addon will be available as a system addon.