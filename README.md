# UnknownAnimeGamePS
- Contributors are always welcome
- Updated to 4.7

## Current features

* Logging in
* Combat (-)
* Friends list
* Teleportation
* Gacha system (-)
* Co-op *partially* works (-)
* Spawning monsters via console
* Inventory features (receiving items/characters, upgrading items/characters, etc) (-)

# Setup Guide

## Main Requirements

- Get [Java 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
- Get [MongoDB Community Server](https://www.mongodb.com/try/download/community)
- Get game version REL4.7.0 (If you don't have a 4.7.0 client, you can find it here and download it) :


| Download link | Package size | MD5 checksum |
| :---: | :---: | :---: |
| [GenshinImpact_4.7.0.zip.001](https://autopatchhk.yuanshen.com/client_app/download/pc_zip/20240524181522_P7n5afVhY8WeoVZb/GenshinImpact_4.7.0.zip.001) | 10.0 GB | 0790ed842a1732fb9e5530a826828440 |
| [GenshinImpact_4.7.0.zip.002](https://autopatchhk.yuanshen.com/client_app/download/pc_zip/20240524181522_P7n5afVhY8WeoVZb/GenshinImpact_4.7.0.zip.002) | 10.0 GB | 6ac391b6a3a185bc8ab1e431f67ecd25 |
| [GenshinImpact_4.7.0.zip.003](https://autopatchhk.yuanshen.com/client_app/download/pc_zip/20240524181522_P7n5afVhY8WeoVZb/GenshinImpact_4.7.0.zip.003) | 10.0 GB | 36460a467de4901f517f8ed9be6b877c |
| [GenshinImpact_4.7.0.zip.004](https://autopatchhk.yuanshen.com/client_app/download/pc_zip/20240524181522_P7n5afVhY8WeoVZb/GenshinImpact_4.7.0.zip.004) | 10.0 GB | d1c0d81ab7aff5d5fb490cff20b9b87f |
| [GenshinImpact_4.7.0.zip.005](https://autopatchhk.yuanshen.com/client_app/download/pc_zip/20240524181522_P7n5afVhY8WeoVZb/GenshinImpact_4.7.0.zip.005) | 10.0 GB | fec57d6f7f78c04309f16dfc2207cd6f |
| [GenshinImpact_4.7.0.zip.006](https://autopatchhk.yuanshen.com/client_app/download/pc_zip/20240524181522_P7n5afVhY8WeoVZb/GenshinImpact_4.7.0.zip.006) | 7.15 GB | 84135fa7008156965514a6ec99c55c66 |


- Download the patch from [here](https://watchandy.me/version.dll).
- Put the `version.dll` in to the folder of your game client.
- Download the old version of [mihoyonet.dll](https://autopatchhk.yuanshen.com/client_app/download/pc_zip/20231030132335_iOEfPMcbrXpiA8Ca/ScatteredFiles/GenshinImpact_Data/Plugins/mihoyonet.dll) (4.2.0).
- Put the old version of `mihoyonet.dll` in `GenshinImpact_Data/Plugins` folder.

### Notice

In the 4.7 version of UnknownAnimeGamePS Grasscutter fork, I've added an option called "useXorEncryption" in config.json, which is disabled by default. If the option is enabled, you won't be able to enter the game using the patch provided above, you will have to use a patch which patches the client's RSA key. Due to my skill issue, I am not able to provide a better patch for PC environment. If you have a better patch, please in contact with me on Discord (@watchandytw), thanks.

## Let's build the server

### 1. Clone the repository

```shell
git clone --recurse-submodules https://github.com/XeonSucksLAB/UnknownAnimeGamePS.git
cd UnknownAnimeGamePS
```

**Curiosity**: Grasscutter uses Gradle to handle dependencies and building.

### 2. Compile the actual Server

**Sidenote**: Make sure to append the right prefix and suffix based on your operating system (./ for linux | .\ for windows | add .bat for windows systems when compiling server JAR/handbook).

**Requirements**:

[Java Development Kit 17 | JDK](https://oracle.com/java/technologies/javase/jdk17-archive-downloads.html) or higher

[Git](https://git-scm.com/downloads)

- **Sidenote**: Handbook generation may fail on some systems. To disable handbook generation, append `-PskipHandbook=1` to the `gradlew jar` command.

- **For Windows**:
```shell
.\gradlew.bat
.\gradlew.bat jar
```
*If you are wondering, the first command is to set up the environment while the 2nd one is for building the server JAR file.*

- **For Linux**:
```bash
chmod +x gradlew
./gradlew jar
```
*If you are wondering, the first command is to make the file executeable and for the rest refer to the windows explanation.*

### You can find the output JAR in the project root folder.

### Manually compile the handbook
```shell
./gradlew generateHandbook
```


## You're done with the building part!

- Launch the server.
- Launch the client and login.

- Enjoy!

### Troubleshooting
- Fiddler or any proxy is required.
