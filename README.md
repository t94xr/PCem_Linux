# PCem v17 for Linux

There is very little to basically no documentation on how to install/compile PCem 17 for Linux.

<pre>
sudo apt-add-repository 'deb http://repos.codelite.org/wx3.0.5/ubuntu/ focal universe'
sudo apt-get install libwxbase3.0-0-unofficial libwxbase3.1* wx3.0-headers wx3.1-headers wx-common libwxbase3.0-dbg libwxgtk3.0-dbg wx3.0-i18n
sudo apt update
sudo apt-get install libwxbase3.0-0-unofficial libwxbase3.0-* wx3.0-headers wx-common libwxbase3.0-dbg libwxgtk3.0-dbg wx3.0-i18n
sudo apt install mesa-utils
cd PCemV17Linux/
sudo apt install openal-dev
sudo apt install libopenal-dev
./configure --enable-release-build
make
</pre>

