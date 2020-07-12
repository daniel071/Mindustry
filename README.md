![Logo](core/assets-raw/sprites/ui/logo.png)

[![Build Status](https://travis-ci.org/daniel071/Mindustry.svg?branch=master)](https://travis-ci.org/Anuken/Mindustry) 
[![Discord](https://img.shields.io/discord/391020510269669376.svg)](https://discord.gg/mindustry)  

This is a custom client of a sandbox tower defense game written in Java. It is based of https://github.com/hellomouse/Mindustry/tree/antigrief and has several extra customisations such as colourful shields and toggleable rendering of ambient light.

_[Trello Board](https://trello.com/b/aE2tcUwF/mindustry-40-plans)_  
_[Wiki](https://mindustrygame.github.io/wiki)_ 

## Downloads
You can find pre-compiled binaries in the [releases page](https://github.com/daniel071/Mindustry/releases). You can also download the source code and compile on your own (see instructions below). 

## Building
If you'd rather compile on your own, follow these instructions.
First, make sure you have [JDK 8](https://adoptopenjdk.net/) installed. Open a terminal in the root directory, `cd` to the Mindustry folder and run the following commands:

#### Windows

_Running:_ `gradlew.bat desktop:run`  
_Building:_ `gradlew.bat desktop:dist`  
_Sprite Packing:_ `gradlew.bat tools:pack`

#### Linux/Mac OS

_Running:_ `./gradlew desktop:run`  
_Building:_ `./gradlew desktop:dist`  
_Sprite Packing:_ `./gradlew tools:pack`

#### Server

Server builds are bundled with each released build (in Releases). If you'd rather compile on your own, replace 'desktop' with 'server', e.g. `gradlew server:dist`.

#### Android

1. Install the Android SDK [here.](https://developer.android.com/studio#downloads) Make sure you're downloading the "Command line tools only", as Android Studio is not required.
2. Create a file named `local.properties` inside the Mindustry directory, with its contents looking like this: `sdk.dir=<Path to Android SDK you just downloaded, without these bracket>`. For example, if you're on Windows and installed the tools to C:\\tools, your local.properties would contain `sdk.dir=C:\\tools` (*note the double backslashes are required instead of single ones!*).
3. Run `gradlew android:assembleDebug` (or `./gradlew` if on linux/mac). This will create an unsigned APK in `android/build/outputs/apk`.
4. (Optional) To debug the application on a connected phone, do `gradlew android:installDebug android:run`. It is **highly recommended** to use IntelliJ for this instead, however.

##### Troubleshooting

If the terminal returns `Permission denied` or `Command not found` on Mac/Linux, run `chmod +x ./gradlew` before running `./gradlew`. *This is a one-time procedure.*

---

Gradle may take up to several minutes to download files. Be patient. <br>
After building, the output .JAR file should be in `/desktop/build/libs/Mindustry.jar` for desktop builds, and in `/server/build/libs/server-release.jar` for server builds.

### Feature Requests

Post feature requests and feedback [here](https://github.com/daniel071/Mindustry/issues/new/choose).
