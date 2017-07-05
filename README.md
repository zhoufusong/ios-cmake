A CMake tool file for iOS

ios-cmake
=========

Tested with the following combinations:

* XCode 8.2.x, iOS SDK 10.2
* XCode 8.3.2, iOS SDK 10.3

# Example usage 
**NOTE: Change the `-DIOS_PLATFORM` to applicable value if targeting other platform. **

```bash
cmake .. -DCMAKE_TOOLCHAIN_FILE=../../ios.toolchain.cmake -DIOS_PLATFORM=SIMULATOR64 -DCMAKE_BUILD_TYPE=Release
cmake --build .
```

## Options

* Set `-DIOS_PLATFORM` to "SIMULATOR" (example above) to build for iOS simulator 32 bit (i386)
* Set `-DIOS_PLATFORM` to "SIMULATOR64" to build for iOS simulator 64 bit (x86_64)
* Set `-DIOS_PLATFORM` to "OS" to build for Device (armv7, armv7s, arm64)

__* To combine all platforms into the same, use the LIPO tool. lipo -create ".a path" -output ".a name"; also you can use lipo -info to analysis it.*__
