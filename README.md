# CANDLE_DLL
This is a fork of the original repo by HubertD found [here](https://github.com/HubertD/candle_dll).

It also has some, but not all changes from another fork by Andrei-Errapart, mbehensky and others found [here](https://github.com/Andrei-Errapart/candle_dll). From these additional changes, I've dropped support for Visual Studio in favour of MinGW. This also makes it much easier to include in Qt projects.

In addition to the changes above, this repo provides support for High Speed USB devices such as the [CAN Bus Debugger](https://canbusdebugger.com) (full disclosure, I'm the developer of that product).

## Compiling
This repo compiles with no warnings. Ensure you have cmake, Ninja and MinGW compilation tools. If you don't have these, consider using MSYS2 or Chocolatey to install.

```
cmake -G Ninja -DCMAKE_BUILD_TYPE=Release -B ./build .
cmake --build ./build
```

## Future work
* Implement CAN FD support
* Investigate if further performance/reliability improvements can be made

I'd like to change the name of this repo to gs_usb_dll to be more generic as it should support all devices following the gs_usb driver protocol. However, I also don't want to take away from the original authors contribution to this code and so for now will keep the name.