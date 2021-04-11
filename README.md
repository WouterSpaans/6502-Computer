
# 6502-Computer
Build a 6502 computer
Based upon teachings by  Ben Eater [link](https://eater.net/6502)
## System Preperation
 [Binaries of vasm for 6502 for x86-64](http://www.ibaug.de/vasm/vasm6502.zip)

    sudo usermod -a -G dialout $USER
    python3 makerom_1.py
    hexdump -C rom.bin
    sudo apt-get install build-essential pkg-config git libusb-1.0-0-dev
    git config --global user.name "Wouter Spaans"
    git config --global user.email wouterspaans@hotmail.com
    git clone https://gitlab.com/DavidGriffith/minipro.git
    cd minipro
    make
    sudo make install
    sudo cp udev/*.rules /etc/udev/rules.d/
    sudo udevadm trigger
    sudo usermod -a -G plugdev $USER
    cd ..
    rm -r minipro/
    minipro -k
    minipro -d AT28C256
    minipro -p AT28C256 -r orig.bin
    hexdump -C orig.bin
    minipro -F updateII.dat
    git clone https://github.com/WouterSpaans/6502-Computer.git


# VS Code Plugins
C/C++
Hex Editor
Markdown Preview?
Python
x64 and x68_64 Assembly