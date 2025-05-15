# Linux G15 Daemon [Logitech G110 and others keyboards]
G15 Daemon + G15 Macro + Led Control for G110 and other Logitech keyboard on Linux 

#### Video Tutorial:

* ITALIAN https://www.youtube.com/watch?v=AnyfWFa_Ku0

* ENGLISH https://www.youtube.com/watch?v=8gAT-BbyOWw

#### Install:
##### RHEL
```shell
chmod +x */configure
##
cd libusb1-1.4.1
sudo yum install -y python3
sudo python setup.py install
cd ..
##
cd 'libg15-1.2.7 - G110 Patch'
./configure
make
sudo make install
cd ..
##
cd g15daemon-1.9.5.3
./configure
# In case you have this error "libg15render-1.2 not found" see this https://github.com/Leproide/Linux-G15-Daemon-Logitech-G110-/issues/2
make
sudo make install
cd ..
##
cd g15macro-1.0.3
./configure
# In case of errors: sudo yum groupinstall -y "X Software Development"
make
sudo make install
cd ..
##
cd 'G110 Led Control'/logitech-keyboard-change-color-master
make
cd ../..
##
sudo yum install -y screen
```
##### Debian/Ubuntu
```shell
chmod +x */configure
##
cd libusb1-1.4.1
sudo apt install -y python3
sudo python setup.py install
cd ..
##
cd 'libg15-1.2.7 - G110 Patch'
sudo apt install -y gcc build-essential libusb-dev
./configure
make
sudo make install
cd ..
##
cd g15daemon-1.9.5.3
sudo apt install -y libg15render-dev
./configure
make
sudo make install
cd ..
##
cd g15macro-1.0.3
sudo apt install -y xorg-dev
./configure
# In case of errors: yum groupinstall "X Software Development"
make
sudo make install
cd ..
##
cd 'G110 Led Control'/logitech-keyboard-change-color-master
make
cd ../..
##
sudo apt install -y screen
```

#### Start:
##### RHEL
```shell
chmod +x ./'Start Script'/GoG110.sh
./'Start Script'/GoG110.sh
```
