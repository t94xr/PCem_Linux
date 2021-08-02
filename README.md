# PCem v17 for Linux

There is very little to basically no documentation on how to install/compile PCem 17 for Linux.

<pre>
mkdir PCemV17Linux/
wget -c https://pcem-emulator.co.uk/files/PCemV17Linux.tar.gz
tar -xvzf PCemV17Linux.tar.gz --directory PCemV17Linux

./configure --enable-alsa --enable-release-build --enable-networking --prefix=/usr
make
</pre>

