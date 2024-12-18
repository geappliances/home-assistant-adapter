# home-assistant-adapter
Example firmware for the ESP32C3-based Home Assistant Adapter.

## Hardware
The Home Assistant Adapter consists of a [Xiao ESP32C3](https://wiki.seeedstudio.com/XIAO_ESP32C3_Getting_Started/) and [carrier board](doc/schematic-v1.0.pdf) that breaks out the serial interface of the Xiao to an RJ45 jack.

## Setup
- Install [PlatformIO](https://platformio.org/)
- Copy `config/Certificate.h.sample` to `config/Certificate.h` and add your certificate (if any)
- Copy `config/Config.h.sample` to `config/Config.h` and add your WiFi credentials, MQTT configuration, and your device ID

In-depth instructions can be found in the [Getting Started](doc/getting-started.md) guide.

## Usage
### Build
Builds the firmware into `.pio/build/xiao_c3/firmware.bin`.

```shell
make
```

### Clean
Deletes all build artifacts.

```shell
make clean
```

### Upload
Uploads/flashes the firmware to the ESP32-C3. Note that the board may need to be reset into boot loader mode by holding the B (boot) button and pressing the R (reset) button.

```shell
make upload
```

### (Serial) Monitor
Opens the PlatformIO serial monitor to view a connected ESP32-C3's serial output.

```shell
make monitor
```

## Example Home Assistant configuration

Sample yaml can be found in https://github.com/geappliances/home-assistant-examples
