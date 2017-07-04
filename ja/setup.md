# セットアップ

## 1. Platoで使用するソフトウェアのセットアップ

### 1.1. Visual Studio Code
Visual Studio Code(以下VSCode)は、Microsoftが提供するOSSのテキストエディタです。  
[こちら](https://code.visualstudio.com/Download)から、ご使用のOS用のVSCodeをダウンロードして、解凍・セットアップを行ってください。

### 1.2. Ruby
Platoの動作には、(本家)Ruby(バージョン1.9.3以降)が必要となります。  
- Windows環境の場合  
[こちら](https://rubyinstaller.org/downloads/)から、RubyInstallerをダウンロードして、セットアップを行って下さい。
- Mac環境の場合  
Mac環境の場合には、初期インストールされているRubyが利用可能です。

参考: コマンドラインから **ruby --version** を実行することで、インストールされているRubyのバージョンが確認できます。
```bash
$ ruby --version
ruby 2.3.0p0 (2015-12-25 revision 53290) [x86_64-darwin15]
```

### 1.3. CoolTerm {#setup-coolterm}

PCとマイコンボードでシリアル通信を行う際に使用するターミナルアプリケーションをインストールします。  
他のターミナルソフト(WindowsのTeraTerm、Macのscreenなど)も利用できますが、ここではCoolTermを使用する前提で説明していきます。

CoolTermは[こちら](http://freeware.the-meiers.org/)からダウンロードできます。  
セットアップは、ダウンロードしたCoolTerm_Win.zip (Macの場合はCoolTerm_Mac.zip) を任意のディレクトリに解凍するだけで完了です。  
解凍したディレクトリ内の**CoolTerm.exe**(Macの場合は**CoolTerm.app**)を実行するとCoolTermが起動します。


## 2. enziボードを使用する場合に必要なソフトウェアのセットアップ {#setup-enzi}

### 2.1. VCP(仮想COMポート)ドライバ {#setup-vcp}

Platoでenziボードを使用する場合には、PCとenziボードでシリアル通信を行うために必要な、VCP(仮想COMポート)ドライバをインストールする必要があります。

#### Windows環境の場合  

1. [こちら](http://www.st.com/ja/development-tools/stsw-stm32102.html)からVCPドライバ(stsw-stm32102.zip)をダウンロードします。
2. 解凍して、VCP_V1.4.0_Setup.exe を実行します。
3. インストール先(例: C:¥Program Files (x86)\STMicroelectronics\Software\Virtual comport driver)のフォルダを開きます。
4. OSのバージョンに応じたフォルダを開きます。  
 - Win7フォルダ: Windows 7, 10 の場合
 - Win8フォルダ: Windows 8.x の場合
5. OSに応じたインストーラを実行します。
 - 32bit版OSの場合: dpinst_x86.exe
 - 64bit版OSの場合: dpinst_amd64.exe

#### Mac環境の場合

[こちら](http://www.ftdichip.com/Drivers/VCP.htm)からFTDIドライバをダウンロードしてインストールします。
※ **Mac OS X 10.9 and above** の **x64 (64-bit)** をダウンロードして下さい


## 3. Platoのセットアップ

1. [こちら](http://plato.click/downloads)からPlatoインストーラをダウンロードします。

### Windows環境の場合

2. plato-windows-X.X.X.zipを任意のフォルダに解凍します。
3. コマンドプロンプトを開き、以下のコマンドを実行します。

```bash
> cd <zipを解凍したフォルダ>
> ruby install.rb
```

### Mac環境の場合

2. 以下のコマンドを実行します。

```bash
$ cd <zipをダウンロードしたディレクトリ>
$ unzip plato-mac-X.X.X.zip
$ cd plato-setup
$ ruby install.rb
```
