# PCem v17 for Linux

There is very little to basically no documentation on how to install/compile PCem 17 for Linux.

# Ubuntu 21.04/Mint 21.2
### Notes
- Update system, so systemd gets upgraded to latest version. libsdl2-dev will not install if it hasn't been upgraded.
- ***Required:*** You will need the Universe Repo enabled, for libsdl2-dev, libwxgtk3.0-gtk3-dev and libopenal-dev
<pre>
sudo apt update && sudo apt upgrade -y

sudo apt-get install libsdl2-dev libwxgtk3.0-gtk3-dev libopenal-dev gcc make g++

mkdir PCemV17Linux/
wget -c https://pcem-emulator.co.uk/files/PCemV17Linux.tar.gz
tar -xvzf PCemV17Linux.tar.gz --directory PCemV17Linux
cd PCemV17Linux

./configure --enable-alsa --enable-release-build --enable-networking --prefix=/opt/pcem17
make -j5
sudo make install

</pre>

Once the 'make install' command has been completed, try running the following terminal command to ensure it is now working on your machine:
<pre>
  /opt/pcem17/bin/pcem
</pre>

If build has completed successfully, running the <code>/opt/pcem17/bin/pcem</code> terminal command will complain about missing BIOS ROM files.

# PCem ROMS 
<pre>
cd ~
cd .pcem
mv roms roms-bak
git clone https://github.com/BaRRaKudaRain/PCem-ROMs.git 
mv PCem-ROMs roms
</pre>

Running <code>/opt/pcem17/bin/pcem</code> should appear with the PCem dialog.
Create a  Shortcut to it by right clicking on the PCEM on the first lunch and then you will see it added among your programs.
