
# houdini-rop-cop-gif

[Houdini](http://www.sidefx.com/index.php) HDK ROP node which creates a gif file from a given COP2 node.

## Binaries, Houdini 16.0
* [Windows, Houdini 16.0.557](https://github.com/ttvd/houdini-rop-cop-gif/releases/download/1.1/houdini.rop.cop.gif.16.0.557.rar) 

## Building

* Tested on Windows and Houdini 16.0.
  * You would have to patch CMake file to get this building on Linux.
* Define HOUDINI_VERSION env variable to be the version of Houdini 16.0 you wish to build against (for example "16.0.557").
* Alternatively, you can have HFS env variable defined (set when you source houdini_setup).
* Generate build files from CMake for your favorite build system. For Windows builds use MSVC 2015.
* Build the ROP Houdini dso (ROP_CopGif.dylib or ROP_CopGif.dll).
* Place the dso in the appropriate Houdini dso folder.
  * On OS X this would be /Users/your_username/Library/Preferences/houdini/16.0/dso/
  * On Windows this would be C:\Users\your_username\Documents\houdini16.0\dso
  * Or $HOUDINI_PATH/dso

## Usage

* Place the ROP into your ROP network.
* Select COP2 node to process.
* Optionally, select image plane (default is C).
* Optionally, select frames for rendering.
* Optionally, select dithering option.

## Limitations

* Only fp16 and fp32 [0..1] color formats are supported.

## Other

* This plugin uses [gif-h library](https://github.com/ginsweater/gif-h-mit) for gif generation.

## License for the plugin

* Copyright Mykola Konyk, 2016
* Distributed under the [MS-RL License.](http://opensource.org/licenses/MS-RL)
* **To further explain the license:**
  * **You cannot re-license any files in this project.**
  * **That is, they must remain under the [MS-RL license.](http://opensource.org/licenses/MS-RL)**
  * **Any other files you add to this project can be under any license you want.**
  * **You cannot use any of this code in a GPL project.**
  * Otherwise you are free to do pretty much anything you want with this code.
  
## License for gif-h
* Copyright Charlie Tangora, MIT license.
