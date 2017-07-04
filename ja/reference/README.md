# Platoクラスライブラリ

## 標準ライブラリ

|クラス||
|:--|:--|
|[Plato::AnalogIO](plato/analogio/README.md)|アナログIOデバイスの制御を行うためのクラスです。|
|[Plato::ButtonSwitch](plato/buttonswitch/README.md)|ボタンスイッチの制御を行うためのクラスです。|
|[Plato::DigitalIO](plato/digitalio/README.md)|ディジタルIOデバイスの制御を行うためのクラスです。|
|[Plato::GPIO](plato/gpio/README.md)|GPIO(汎用IO)デバイスの制御を行うためのクラスです。|
|[Plato::LED](plato/led/README.md)|LEDの制御を行うためのクラスです。|
|[Plato::MRubyApplication](plato/application/README.md)|典型的なmruby組込みアプリケーションに必要なタイマ処理等の機能を提供するクラスです。|
|[Plato::RTC](plato/rtc/README.md)|RTC(Real Time Clock)の制御を行うための抽象クラスです。|
|[Plato::Sensor](plato/sensor/README.md)|各種センサデバイスの制御を行うための抽象クラスです。|
|[Plato::Timer](plato/timer/README.md)|タイマ起動機能を提供するクラスです。|
|[Plato::ZigBee](plato/zigbee/README.md)|ZigBee通信デバイスの制御を行うための抽象クラスです。|

|モジュール||
|:--|:--|
|[Plato::I2C](plato/i2c/README.md)|I<sup>2</sup>CシリアルI/Fへの入出力操作を定義したモジュールです。|
|[Plato::Machine](plato/machine/README.md)|マシン(マイコンボード)に依存する各種制御を定義したモジュールです。|
|[Plato::Serial](plato/serial/README.md)|シリアルI/Fへの入出力操作を定義したモジュールです。|


## デバイスライブラリ

|クラス||
|:--|:--|
|[PlatoDevice::HDC1080](devices/hdc1080/README.md)|温湿度センサ(HDC1080)のデバイスクラスです。|
|[PlatoDevice::MCP7940](devices/mcp7940/README.md)|RTC(MCP7940)のデバイスクラスです。|
|[PlatoDevice::TSL2591](devices/tsl2591/README.md)|照度センサ(TSL2591)のデバイスクラスです。|
|[PlatoDevice::RN4020](devices/rn4020/README.md)|RN4020 BLE通信モジュールのデバイスクラスです。|
|[PlatoDevice::XBeeWiFi](devices/xbeewifi/README.md)|XBee WiFi通信モジュールのデバイスクラスです。|
|[PlatoDevice::XBee](devices/xbee/README.md)|XBee ZigBee通信モジュールのデバイスクラスです。|


## マイコンボード依存ライブラリ

### [enzi](http://enzi.cc/) ライブラリ

|クラス||
|:--|:--|
|[Plato::AnalogIO](boards/enzi/analogio/README.md)|アナログIOデバイスの制御を行うためのクラスです。|
|[Plato::DigitalIO](boards/enzi/digitalio/README.md)|ディジタルIOデバイスの制御を行うためのクラスです。|
|[Plato::GPIO](boards/enzi/gpio/README.md)|GPIO(汎用IO)デバイスの制御を行うためのクラスです。|
|[PlatoEnzi::I2C](boards/enzi/i2c/README.md)|I<sup>2</sup>C I/Fへの入出力を行うためのクラスです。|
|[PlatoEnzi::Machine](boards/enzi/machine/README.md)|enziボードに依存する各種機能を提供するクラスです。|
|[PlatoEnzi::Serial](boards/enzi/serial/README.md)|enziボードのシリアルI/F(UART)への入出力機能を提供するクラスです。|

### [Raspberry Pi](https://www.raspberrypi.org/) ライブラリ

#### 準備中です。

### [GR-PEACH](http://gadget.renesas.com/ja/product/peach.html) ライブラリ

#### 準備中です。

### White-Tiger センサボード ライブラリ

|クラス||
|:--|:--|
|[Plato::GPIO](boards/whitetiger/gpio/README.md)|GPIO(汎用IO)デバイスの制御を行うためのクラスです。|
