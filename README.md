# PCemV16macOS
MacOS port of PCem low-level PC hardware emulator PCem V16. Experimental OpenGL 3 port. 

**NOTE: Follow the instructions below if you are running macOS Mojave (10.14) or Catalina (10.15). This version of PCem is not fully compatibe with macOS 11 Big Sur. If you are running Big Sur, use PCem version 17 (https://github.com/PCemOnMac/PCemV17macOS).

Step 1: Install Xcode command-line tools

You need Xcode command-line tools from Apple in order to install Home Brew. You can install Xcode from the App Store or, when you run the Home Brew install script (step 2), it will install the command-line tools for you.

Step 2: Install Home Brew

Home Brew is the package manager for macOS that makes it easy to install the required packages needed for PCem to compile successfully. You can get it from https://brew.sh or run the following command from a Terminal shell:

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

Step 3: Install the required packages needed by PCem

In order to compile PCem on macOS you'll need sdl2, wxmac and openal-soft packages (Note: Later versions of macOS already have openal-soft so you may not need to install it using Home Brew). You can install theses with the following commands:

brew install sdl2

brew install wxmac

brew install openal-soft

Step 3: Download the Source Code

Download the source code from this repository and change directory to the PCem install folder.

Example: cd /PCemV16macOS-master

Step 3: Build PCem

Run the configuration script:

./configure --enable-release-build

If you want networking support:

./configure --enable-networking --enable-release-build

Assuming the command completes successfully run:

make

This will take a while. You may see some warning messages during the make process but they do not seem to cause any issues with the compile. Once it completes you'll have the pcem executable file in the install folder. To start the program just run ./pcem from the terminal. You will need to obtain the required ROM files for the machine you want to emulate and need at least one valid ROM for pcem to start. These go in the roms folder located in the folder where PCem is installed.
