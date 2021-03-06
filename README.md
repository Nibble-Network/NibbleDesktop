

# Nibble Desktop (GUI Wallet)

<p align="center">
<img width="600" height="342" src="https://i.imgur.com/mhh1gL8.gif">
</p>
Maintained by The Nibble Developers.

## Information
Nibble is a decentralized reward platform with encrypted messages and own privacy protected cryptocurrency.

All your NBXC transactions and messages are anonymous. The Nibble Network provides an instant secure, untraceable and unlinkable way of encrypted communication - crypto messages.

Nibble is open-source, always has been and always will be. 
This latest edition of Nibble, has been created from a merger of projects - Nibble Classic & Crumbs
Giving our users the best from both worlds, a simple to use platform, messaging ability, deposits & rewards.

Get your nibble on!

## Resources
- Web: https://nibble-nibble.com
- GitHub: https://github.com/Nibble-Network
- Discord: https://discordapp.com/invite/rqYhADW
- Twitter: @NibbleNetwork


## Compiling Nibble from source

### Linux / Ubuntu

##### Prerequisites

Dependencies: GCC 4.7.3 or later, CMake 2.8.6 or later, Boost 1.55 or later, and Qt 5.9 or later.
You may download them from:

- http://gcc.gnu.org/
- http://www.cmake.org/
- http://www.boost.org/
- https://www.qt.io

Alternatively, it may be possible to install them using a package manager.

#### Building

To acquire the source via git and build the release version, run the following commands:

- `cd ~`
- `git clone https://github.com/Nibble-Network/NibbleDesktop`
- `cd nibble-wallet`
- `git clone https://github.com/Nibble-Network/nibble.git cryptonote`
- `make build-release`
- `mkdir bin && mv build/release/NIBBLE-GUI bin/`
- `make clean`

If the build is successful the binaries will be in the bin folder.

### Windows 10

##### Prerequisites

- Install [Visual Studio 2017 Community Edition](https://www.visualstudio.com/thank-you-downloading-visual-studio/?sku=Community&rel=15&page=inlineinstall)
- When installing Visual Studio, you need to install **Desktop development with C++** and the **VC++ v140 toolchain** components. The option to install the v140 toolchain can be found by expanding the "Desktop development with C++" node on the right. You will need this for the project to build correctly.
- Install [CMake](https://cmake.org/download/)
- Install [Boost 1.67.0](https://boost.teeks99.com/bin/1.67.0/), ensuring you download the installer for MSVC 14.1.
- Install [Qt 5.11.0](https://www.qt.io/download)

##### Building

- From the start menu, open 'x64 Native Tools Command Prompt for vs2017' or run "C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\Common7\Tools\VsMSBuildCmd.bat" from any command prompt.
- Edit the CMakeLists.txt file and set the path to QT cmake folder. For example: set(CMAKE_PREFIX_PATH "C:\\Qt\\5.11.0\\msvc2017_64\\lib\\cmake\\").
- `git clone https://github.com/Nibble-Network/nibble`
- `git clone https://github.com/Nibble-Network/NibbleDesktop`
- Copy the contents of the nibble-core folder into nibble-wallet\cryptonote
- `cd nibble-wallet`
- `mkdir build`
- `cd build`
- `cmake -G "Visual Studio 15 2017 Win64" -DBOOST_LIBRARYDIR:PATH=c:/local/boost_1_67_0 ..` (Or your boost installed dir.)
- `msbuild NIBBLE-GUI.sln /p:Configuration=Release`

If the build is successful the binaries will be in the Release folder.

#### Special Thanks
Special thanks goes out to the developers from Cryptonote, Bytecoin, Monero, Forknote, TurtleCoin, Masari & Conceal Network.
