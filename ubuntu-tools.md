#ubuntu-tools.md
## clock-override
https://extensions.gnome.org/extension/1206/clock-override/
### params 
Bienvienue M. COUNDIA, Aujourhd'hui c'est   :   [ %A %d %B %Y ]      et il est  :  [ %H:%M ]  à DAKAR

## scrcpy
https://github.com/Genymobile/scrcpy
Debian/Ubuntu

# runtime dependencies
sudo apt install ffmpeg libsdl2-2.0-0

# client build dependencies
sudo apt install make gcc git pkg-config meson ninja-build \
                 libavcodec-dev libavformat-dev libavutil-dev \
                 libsdl2-dev

# server build dependencies
sudo apt install openjdk-8-jdk

On old versions (like Ubuntu 16.04), meson is too old. In that case, install it from pip3:

sudo apt install python3-pip
pip3 install meson

export ANDROID_HOME=/outils/Android/sdk

git clone https://github.com/Genymobile/scrcpy
cd scrcpy

meson x --buildtype release --strip -Db_lto=true
cd x
ninja
