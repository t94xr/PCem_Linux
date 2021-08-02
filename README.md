# PCem v17 for Linux

There is very little to basically no documentation on how to install/compile PCem 17 for Linux.

# Ubuntu 21.04
### Notes
- Update system, so systemd gets upgraded to latest version. libsdl2-dev will not install if it hasn't been upgraded.
- ***Required:*** You will need the Universe Repo enabled, for libsdl2-dev, libwxgtk3.0-dev and libopenal-dev
<pre>
sudo apt update && sudo apt upgrade -y

sudo apt-get install libsdl2-dev libwxgtk3.0-dev libopenal-dev

mkdir PCemV17Linux/
wget -c https://pcem-emulator.co.uk/files/PCemV17Linux.tar.gz
tar -xvzf PCemV17Linux.tar.gz --directory PCemV17Linux
cd PCemV17Linux

./configure --enable-alsa --enable-release-build --enable-networking --prefix=/usr
make
</pre>

If build has completed successfully, running <code>./pcem</code> will complain about missing BIOS files.

# PCem ROMS 
<pre>
cd ~
cd .pcem
mv roms roms-bak
git clone https://github.com/BaRRaKudaRain/PCem-ROMs.git 
mv PCem-ROMs roms
</pre>

Running <code>./pcem</code> should appear with the PCem dialog.
