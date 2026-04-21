[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![cctv-viewer](https://img.shields.io/badge/Launchpad_PPA-daily/latest+git-0e8420?logo=launchpad)](https://launchpad.net/~ievgeny/+archive/ubuntu/cctv-viewer)
[![cctv-viewer](https://snapcraft.io/cctv-viewer/badge.svg)](https://snapcraft.io/cctv-viewer)
[![cctv-viewer](https://snapcraft.io/cctv-viewer/trending.svg?name=0)](https://snapcraft.io/cctv-viewer)

# CCTV Viewer

CCTV Viewer - a simple application for simultaneously viewing multiple video streams. Designed for high performance and low latency.
Based on ffmpeg.

To clone this repository use the following command:

	git clone --recurse-submodules https://github.com/sviktor75/cctv-viewer.git

The original repository:

	git clone --recurse-submodules https://github.com/iEvgeny/cctv-viewer.git

# Install requirements for Linux Mint 22.3 Mate

	sudo apt update
	sudo apt install git build-essential cmake qtbase5-dev qtdeclarative5-dev \
	qtmultimedia5-dev qml-module-qtquick-controls2 qml-module-qtquick-layouts \
	libavformat-dev libavcodec-dev libavutil-dev libswscale-dev libavdevice-dev
	
	sudo apt install qttools5-dev-tools
	sudo apt install qttools5-dev
	sudo apt install libgtest-dev
	sudo apt install libva-dev libx11-dev
	sudo apt install qml-module-qtmultimedia
	sudo apt install qml-module-qtquick-dialogs qml-module-qt-labs-settings

# Compile and install cctv-viewer
	
	cd ~
	mkdir opt && cd opt
	git clone --recurse-submodules https://github.com/sviktor75/cctv-viewer.git
	cd cctv-viewer
	mkdir build && cd build
	
	cmake ..
	or
	cmake -DENABLE_TESTS=OFF ..
	
	make -j$(nproc)

# Copy the binary to be accessible from "anywhere"
	sudo cp cctv-viewer /usr/bin/
	

# Start the program
CLI:

	cctv-viewer
Desktop:
	
	cp cctv-viewer.desktop ~/Desktop
	# Start by the new ikon from desktop
	


	
