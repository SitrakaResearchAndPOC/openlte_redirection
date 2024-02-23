# openlte_redirection

## Installation : 
## FIRST STEP INSTALLING ALL COMMONS DRIVERS
```
mkdir src
```
```
cd src
```
```
mkdir drivers
```
```
cd drivers
```
```
mkdir ../../Desktop/ltehack_backup
```
```
apt update
```
May be need it : </br>
python3-pyqt4     python-qt4    libgsi-dev     libssl1.0-dev   </br>
libqt4-opengl-dev    libssl1.0-dev </br>
libnicursesw5-dev     libpython-dev     python-pip </br>
python-sphinx* </br>
libpython-dev libncursesw5-dev </br>
```
apt-get install libjeromq-java libzmq-ffi-perl libzmq-java libzmq-java-doc libzmq-jni libzmq3-dev libzmq5 libzmqpp-dev libzmqpp4 python3-zmq python3-zmq libboost-dev libpython3.8-dev cmake build-essential python3-qwt python3-guiqwt python3-pyqt5.qwt libgmp-dev libxi-dev libcppunit-dev libx11-6 libx11-dev flex libncurses5 libncurses5-dev libncursesw6 libpcsclite-dev libsdl1.2-dev zlib1g-dev libmpfr6 libmpc3 lemon aptitude libtinfo-dev libtool shtool autoconf git-core pkg-config make libmpfr-dev python-cheetah libmpc-dev libtalloc-dev libfftw3-dev libgnutls28-dev libtool-bin python-lxml libxml2-dev python-sip sofia-sip-bin libsofia-sip-ua-dev sofia-sip-bin bison libgmp3-dev alsa-oss asn1c libdbd-sqlite3 libboost-all-dev libusb-1.0-0-dev python-mako python3-mako doxygen python-docutils cmake build-essential g++ python-numpy python3-numpy swig libsqlite3-dev libi2c-dev libwxgtk3.0-gtk3-dev freeglut3-dev composer phpunit python3-pip libfontconfig1-dev libxrender-dev python-sip-dev  libusb-dev libusb-1.0.0-dev libcomedi-dev libzmq3-dev javascript-common libjs-jquery libjs-sphinxdoc libjs-underscore python-sphinx-click-doc python-sphinx-copybutton-doc python-sphinx-feature-classification-doc python-sphinx-gallery-doc python-sphinxcontrib.bibtex-doc python-sphinxcontrib.programoutput-doc python-sphinxcontrib.spelling-doc build-essential libgmp-dev libx11-6 libx11-dev flex libncurses5 libncurses5-dev libncursesw6 libpcsclite-dev zlib1g-dev libmpfr6 libmpc3 lemon aptitude libtinfo-dev libtool shtool autoconf git-core pkg-config make libmpfr-dev libmpc-dev libtalloc-dev libfftw3-dev libgnutls28-dev  libtool-bin libxml2-dev sofia-sip-bin libsofia-sip-ua-dev sofia-sip-bin bison libgmp3-dev alsa-oss asn1c libdbd-sqlite3 libboost-all-dev libusb-1.0-0-dev python-mako python3-mako doxygen python-docutils cmake build-essential g++ python-numpy python3-numpy swig libsqlite3-dev libi2c-dev libwxgtk3.0-gtk3-dev freeglut3-dev composer phpunit python3-pip
```

## Installing UHD
```
git clone https://github.com/ettusresearch/uhd
```
```
cd uhd/
```
```
git checkout aea0e2de34803d5ea8f25d7cf2fb08f4ab9d43f0
```
```
cd ..
```
```
zip -r uhd.zip uhd
```
```
mv uhd.zip ../../Desktop/ltehack_backup 
```
```
cd uhd/host/ && mkdir build && cd build/
```
```
cmake ..
```
```
make
```
```
#make test
```
```
make install
```
```
ldconfig
```
```
cd ../../..
```


## Installing soapyUHD
```
git clone https://github.com/pothosware/SoapySDR
```
```
cd SoapySDR/
```
```
git checkout f722f9ce5b629c3c44401a9bf628b3f8e67a9695
```
```
cd ..
```
```
zip -r SoapySDR.zip SoapySDR/
```
```
mv SoapySDR.zip ../../Desktop/ltehack_backup 
```
```
cd SoapySDR && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```
```
/usr/local/lib/uhd/utils/uhd_images_downloader.py
```

## Installing BladeRF
```
git clone https://github.com/nuand/BladeRF
```
```
zip -r BladeRF_final.zip BladeRF/
```
```
mv BladeRF_final.zip ../../Desktop/ltehack_backup 
```
```
cd BladeRF/
```
```
git checkout 45521019c540392287eb6e03d52b8073b2fd0743
```
```
cd ..
```
```
zip -r BladeRF.zip BladeRF/
```
```
mv BladeRF.zip ../../Desktop/ltehack_backup 
```
```
cd BladeRF && mkdir build && cd build/
```
```
cmake ..
```
```
cd ../..
```
```
zip -r BladeRF_with_noOS.zip BladeRF/
```
```
mv BladeRF_with_noOS.zip ../../Desktop/ltehack_backup 
```
```
cd BladeRF && cd build
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```

## Installing SoapyBladeRF
```
git clone https://github.com/pothosware/SoapyBladeRF
```
```
cd SoapyBladeRF/
```
```
git checkout 1c1e8aaba5e8ee154b34c6c3b17743d1c9b9a1ea
```
```
cd ..
```
```
zip -r SoapyBladeRF.zip SoapyBladeRF/
```
```
mv SoapyBladeRF.zip ../../Desktop/ltehack_backup 
```
```
cd SoapyBladeRF && mkdir build && cd build/
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```

#If Problem_bladerf </br>
#bladeRF-cli -v verbose -L hostedxA4.rbf </br>
 
## Installing LimeSuite
```
git clone https://github.com/myriadrf/LimeSuite
```
```
cd LimeSuite
```
```
#git checkout c931854ead81307206bce750c17c230181065545
```
```
git checkout c931854ead81307206bce750c17c
```
```
cd ..
```
```
zip -r LimeSuite.zip LimeSuite
```
```
mv LimeSuite.zip ../../Desktop/ltehack_backup 
```
```
cd LimeSuite && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```
## Installing HackRF
```
git clone https://github.com/mossmann/hackrf.git
```
```
cd hackrf
```
#date 2018 : 5e9cad66363467fae93aec29679c041c03905047
```
git checkout 189b5bf693620d43d27fe8accdf112c85ce833a0
```
```
cd ..
```
```
zip -r hackrf_grc37.zip hackrf
```
```
mv hackrf_grc37.zip ../../Desktop/ltehack_backup 
```
```
cd hackrf/host && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../../..
```

## Installing SoapyHackRF
```
git clone https://github.com/pothosware/SoapyHackRF.git
```
```
cd SoapyHackRF/
```
```
git checkout 6c0c33f0aa44c3080674e6bca0273184d3e9eb44
```
```
cd ..
```
```
zip -r SoapyHackRF_grc37.zip SoapyHackRF
```
```
mv SoapyHackRF_grc37.zip ../../Desktop/ltehack_backup 
```
```
cd SoapyHackRF && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```
#FLASHING HACKRF WITH NEW FIRMWARE </br>
```
wget https://github.com/greatscottgadgets/hackrf/releases/download/v2023.01.1/hackrf-2023.01.1.tar.xz
```
```
tar -xvf hackrf-2023.01.1.tar.xz
```
```
mv hackrf-2023.01.1.tar.xz ../../Desktop/ltehack_backup 
```
```
cd hackrf-2023.01.1/firmware-bin/
```
#PRESS DFU AND RESET
```
hackrf_spiflash -w hackrf_one_usb.bin
```
#PRESS RESET
```
#apt-get install dfu-util </br>
#dfu-util -D hackrf_one_usb.dfu  </br>
#Test : plug hackrf </br>
```
hackrf_info
```
```
SoapySDRUtil --info
```
#Available factories...hackrf, null,
```
SoapySDRUtil --probe="driver=hackrf"
```
SoapySDRUtil --make="driver=hackrf"
```
## Installing SoapyUHD
```
git clone https://github.com/pothosware/SoapyUHD
```
```
cd SoapyUHD/
```
```
git checkout 47972ba8b96beffb79915e300acea168bacd8d84
```
```
cd ..
```
```
zip -r SoapyUHD_grc37.zip SoapyUHD
```
```
mv SoapyUHD_grc37.zip ../../Desktop/ltehack_backup 
```
```
cd SoapyUHD && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../../..
```
Test :
```
uhd_usrp_probe
```
#UNPLUG HACKRF


## Installing GRC3.7
#Installing HackRF Software — HackRF documentation </br>
#How to install hackrf on Ubuntu 20.04 (Focal Fossa)? (devmanuals.net) </br>
```
mkdir grc37
```
```
cd grc37
```

#/* </br>
#https://kb.ettus.com/Building_and_Installing_the_USRP_Open-Source_Toolchain_(UHD_and_GNU_Radio)_on_Linux </br>
#*/ </br>
#apt-get install python-zmq </br>
```
sudo apt-get -y install autoconf automake build-essential ccache cmake cpufrequtils doxygen ethtool fort77 g++ gir1.2-gtk-3.0 git gobject-introspection gpsd gpsd-clients inetutils-tools libasound2-dev libboost-all-dev libcomedi-dev libcppunit-dev libfftw3-bin libfftw3-dev libfftw3-doc libfontconfig1-dev libgmp-dev libgps-dev libgsl-dev liblog4cpp5-dev libncurses5 libncurses5-dev libpulse-dev libqt5opengl5-dev libqwt-qt5-dev libsdl1.2-dev libtool libudev-dev libusb-1.0-0 libusb-1.0-0-dev libusb-dev libxi-dev libxrender-dev libzmq3-dev libzmq5 ncurses-bin python3-cheetah python3-click python3-click-plugins python3-click-threading python3-dev python3-docutils python3-gi python3-gi-cairo python3-gps python3-lxml python3-mako python3-numpy python3-numpy-dbg python3-opengl python3-pyqt5 python3-requests python3-scipy python3-setuptools python3-six python3-sphinx python3-yaml python3-zmq python3-ruamel.yaml swig wget
```
```
git clone https://github.com/gnuradio/gnuradio
```
```
zip -r gnuradio_final.zip gnuradio
```
```
mv gnuradio_final.zip ../../Desktop/ltehack_backup 
```
```
cd gnuradio/
```
```
git checkout 2d7f82342c1d63a1c4d7e18eb1289636ebcbb855
```
```
git submodule init && git submodule update
```
```
cd ..
```
## Compiling gnuradio3.7
```
zip -r gnuradio_grc37.zip gnuradio
```
```
mv gnuradio_grc37.zip ../../Desktop/ltehack_backup 
```
```
cd gnuradio && mkdir build && cd build
```
```
cmake ..
```
```
make
```
#make test
```
make install
```
```
ldconfig
```
```
cd ../..
```

## Installing gr-osmosdr
```
git clone https://github.com/osmocom/gr-osmosdr
```
```
cd gr-osmosdr/
```
```
git checkout 4d83c60
```
```
cd ..
```
```
zip -r gr-osmosdr_grc37.zip gr-osmosdr
```
```
mv gr-osmosdr_grc37.zip ../../Desktop/ltehack_backup 
```
```
cd gr-osmosdr && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```

## Installing attack LTE
* Before the attack , preparing :
```
exit
```
Open terminal
```
cd src
```
```
mkdir attacklte
```
```
cd attacklte
```
#One line command
```
mkdir polarssl && cd polarssl && wget https://src.fedoraproject.org/repo/pkgs/polarssl/polarssl-1.3.7-gpl.tgz/b656e4c83ee94f93d19eb0832fd7f976/polarssl-1.3.7-gpl.tgz
```
#or
```
git clone https://github.com/ImsicatcherBastienbaranoff/polarssl && cd polarssl
```
```
tar xvzf polarssl-1.3.7-gpl.tgz  
```
```
mv polarssl-1.3.7-gpl.tgz ../../../Desktop/ltehack_backup 
```
```
cd polarssl-1.3.7 
```
```
mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../../..
```
```
apt-get  install net-tools
```
</br></br>
FOR LIMESDR, NO MODIFICATION FOR USRP
</br></br>
Have a look at the [patch](https://github.com/SitrakaResearchAndPOC/fork_OpenLTE_RedirectionPatch) </br>
In /LTE_fdd_enodeb/src/LTE_fdd_enb_radio.cc , Replace if((devs[idx-1]["type"] == "soapy")) by
```
       if((devs[idx-1]["type"] == "soapy")||(devs[idx-1]["type"] == "uhd"))
```

For LIMESDR, replace BAND2 by LNAH
```
             usrp->set_rx_freq((double)liblte_interface_ul_earfcn_to_frequency(ul_earfcn));

             usrp->set_tx_gain(tx_gain);

             usrp->set_rx_gain(rx_gain);

+            usrp->set_tx_antenna("BAND2");

+           usrp->set_rx_antenna("LNAH");

             // Setup the TX and RX streams

             tx_stream  = usrp->get_tx_stream(stream_args);

             rx_stream  = usrp->get_rx_stream(stream_args);

# */
```

* Redirection by Bastien Baranoff
```
git clone https://github.com/bbaranoff/openlte
```
```
cd openlte/
```
```
git checkout 4bd673b
```
```
cd ..
```
```
mv openlte openlte_redir
```
```
zip -r openlte_redir.zip openlte_redir
```
```
mv openlte_redir.zip  ../../Desktop/ltehack_backup/
```
```
cd openlte_redir
```
```
mkdir build && cd build/
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
LTE_fdd_enodeb
```
```
cd ../..
```

 
#/* </br>
Use the last version of Openlte with the name of attack by using :
```
git checkout name_of_attack
```
Some attacks implemented by @onkarmumbrekar can be found in the different branches: </br>
https://github.com/ImsicatcherBastienbaranoff/Advanced_LTE_ATTACK </br>
https://drive.google.com/drive/folders/1u5bRMle3_iirDNfIEe8toGC4WDKfvkA5?usp=share_link </br>
https://github.com/mgp25/OpenLTE </br> </br>

#LTE ATTACK TYE : </br> 
    akabypass </br>
    attach_reject </br>
    dos_tau_reject_dualcause </br>
    dos_tau_reject </br>
    malformed_detach </br>
    numb_attack </br>
    service_reject_on_tau </br>
    tau_numb_attack </br> </br>

More information at: https://github.com/mgp25/OpenLTE </br>
#*/ </br>

```
git clone https://github.com/mgp25/OpenLTE
```
```
mv OpenLTE OpenLTE_mgp25
```
```
zip -r OpenLTE_mgp25.zip OpenLTE_mgp25
```
```
mv OpenLTE_mgp25.zip ../../Desktop/ltehack_backup/
```
```
cd OpenLTE_mgp25/
```
```
mkdir build
```
```
cd build && cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```


#/* </br>
Let's test the attack, if the checkout doesn't exist , look at drive file </br>
Fixing problem bladerf : https://github.com/ImsicatcherBastienbaranoff/OpenLTE_Patch_AdvancedAttack </br> </br>

#*/ </br>
```
gedit LTE_fdd_enodeb/src/LTE_fdd_enb_radio.cc
```
</br>
</br>
#look the function : bladerf_get_timestamp </br>
#Replace 

```
BLADERF_MODULE_RX
```
by 
```
BLADERF_RX 
```
</br>
</br>
#Replace all : 

```
BLADERF_MODULE_TX  
```
by  
```
BLADERF_TX_X1 
```
</br>
#Replace all : 

```
BLADERF_MODULE_RX
```
by
```
BLADERF_RX_X1 
```
</br> </br>

* akabypass :
```
git clone https://github.com/mgp25/OpenLTE
```
```
zip -r OpenLTE.zip OpenLTE
```
```
cd OpenLTE
```
```
git checkout akabypass
```
```
gedit LTE_fdd_enodeb/src/LTE_fdd_enb_radio.cc
```

</br>
</br>
#look the function : bladerf_get_timestamp </br>
#Replace 

```
BLADERF_MODULE_RX
```
by 
```
BLADERF_RX 
```
</br>
</br>
#Replace all : 

```
BLADERF_MODULE_TX  
```
by  
```
BLADERF_TX_X1 
```
</br>
#Replace all : 

```
BLADERF_MODULE_RX
```
by
```
BLADERF_RX_X1 
```
</br> </br>

```   
rm -rf build/
```
```
cd ..
```
```
mv OpenLTE OpenLTE_akabypass
```
```
zip -r OpenLTE_akabypass.zip OpenLTE_akabypass/
```
```
mv OpenLTE_akabypass.zip ../../Desktop/ltehack_backup/
```
```
cd OpenLTE_akabypass && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```
 
* attach_reject : 
```
unzip OpenLTE.zip 
```
```
cd OpenLTE
```
```
git checkout attach_reject
```
```
gedit LTE_fdd_enodeb/src/LTE_fdd_enb_radio.cc
```
</br>
</br>
#look the function : bladerf_get_timestamp </br>
#Replace 

```
BLADERF_MODULE_RX
```
by 
```
BLADERF_RX 
```
</br>
</br>
#Replace all : 

```
BLADERF_MODULE_TX  
```
by  
```
BLADERF_TX_X1 
```
</br>
#Replace all : 

```
BLADERF_MODULE_RX
```
by
```
BLADERF_RX_X1 
```
</br> </br>

```
rm -rf build/
```
```
cd ..
```
```
mv OpenLTE OpenLTE_attach_reject
```
```
zip -r OpenLTE_attach_reject.zip OpenLTE_attach_reject
```
```
mv OpenLTE_attach_reject.zip ../../Desktop/ltehack_backup/
```
```
cd OpenLTE_attach_reject && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```


* dos_tau_reject_dualcause : 
```
unzip OpenLTE.zip 
```
```
cd OpenLTE
```
```
git checkout dos_tau_reject_dualcause
```
```
gedit LTE_fdd_enodeb/src/LTE_fdd_enb_radio.cc
```

</br>
</br>
#look the function : bladerf_get_timestamp </br>

#Replace 

```
BLADERF_MODULE_RX
```
by 
```
BLADERF_RX 
```
</br>
</br>
#Replace all : 

```
BLADERF_MODULE_TX  
```
by  
```
BLADERF_TX_X1 
```
</br>
#Replace all : 

```
BLADERF_MODULE_RX
```
by
```
BLADERF_RX_X1 
```
</br> </br>

```
rm -rf build/
```
```
cd ..
```
```
mv OpenLTE OpenLTE_dos_tau_reject_dualcause
```
```
zip -r OpenLTE_dos_tau_reject_dualcause.zip OpenLTE_dos_tau_reject_dualcause
```
```
mv OpenLTE_dos_tau_reject_dualcause.zip ../../Desktop/ltehack_backup/
```
```
cd OpenLTE_dos_tau_reject_dualcause && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```

 

* dos_tau_reject : 
```
unzip OpenLTE.zip 
```
```
cd OpenLTE
```
```
git checkout dos_tau_reject
```
```
gedit LTE_fdd_enodeb/src/LTE_fdd_enb_radio.cc
```
</br>
</br>
#look the function : bladerf_get_timestamp </br>
#Replace 

```
BLADERF_MODULE_RX
```
by 
```
BLADERF_RX 
```
</br>
</br>
#Replace all : 

```
BLADERF_MODULE_TX  
```
by  
```
BLADERF_TX_X1 
```
</br>
#Replace all : 

```
BLADERF_MODULE_RX
```
by
```
BLADERF_RX_X1 
```
</br> </br>
   
```
rm -rf build/
```
```
cd ..
```
```
mv OpenLTE OpenLTE_dos_tau_reject
```
```
zip -r OpenLTE_dos_tau_reject.zip OpenLTE_dos_tau_reject
```
```
mv OpenLTE_dos_tau_reject.zip  ../../Desktop/ltehack_backup/
```
```
cd OpenLTE_dos_tau_reject && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
``` 


* malformed_detach :
```  
unzip OpenLTE.zip 
```
```
cd OpenLTE
```
```
git checkout malformed_detach 
```
```
gedit LTE_fdd_enodeb/src/LTE_fdd_enb_radio.cc
```
</br>
</br>
#look the function : bladerf_get_timestamp </br>

#Replace 

```
BLADERF_MODULE_RX
```
by 
```
BLADERF_RX 
```
</br>
</br>
#Replace all : 

```
BLADERF_MODULE_TX  
```
by  
```
BLADERF_TX_X1 
```
</br>
#Replace all : 

```
BLADERF_MODULE_RX
```
by
```
BLADERF_RX_X1 
```
</br> </br>

```   
rm -rf build/
```
```
cd ..
```
```
mv OpenLTE OpenLTE_malformed_detach 
```
```
zip -r OpenLTE_malformed_detach.zip OpenLTE_malformed_detach 
```
```
mv OpenLTE_malformed_detach.zip  ../../Desktop/ltehack_backup/
```
```
cd OpenLTE_malformed_detach && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```



* numb_attack :
```
unzip OpenLTE.zip 
```
```
cd OpenLTE
```
```
git checkout numb_attack
```
```
gedit LTE_fdd_enodeb/src/LTE_fdd_enb_radio.cc
```
</br>
</br>
#look the function : bladerf_get_timestamp </br>
#Replace 

```
BLADERF_MODULE_RX
```
by 
```
BLADERF_RX 
```
</br>
</br>
#Replace all : 

```
BLADERF_MODULE_TX  
```
by  
```
BLADERF_TX_X1 
```
</br>
#Replace all : 

```
BLADERF_MODULE_RX
```
by
```
BLADERF_RX_X1 
```
</br> </br>


```
rm -rf build/
```
```
cd ..
```
```
mv OpenLTE OpenLTE_numb_attack 
```
```
zip -r OpenLTE_numb_attack.zip OpenLTE_numb_attack 
```
```
mv OpenLTE_numb_attack.zip ../../Desktop/ltehack_backup/
```
```
cd OpenLTE_numb_attack && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```

* service_reject_on_tau :

```  
unzip OpenLTE.zip 
```
```
cd OpenLTE
```
```
git checkout service_reject_on_tau
```
```
gedit LTE_fdd_enodeb/src/LTE_fdd_enb_radio.cc
```
</br>
</br>
#look the function : bladerf_get_timestamp </br>
#Replace 

```
BLADERF_MODULE_RX
```
by 
```
BLADERF_RX 
```
</br>
</br>
#Replace all : 

```
BLADERF_MODULE_TX  
```
by  
```
BLADERF_TX_X1 
```
</br>
#Replace all : 

```
BLADERF_MODULE_RX
```
by
```
BLADERF_RX_X1 
```
</br> </br>

```
rm -rf build/
```
```
cd ..
```
```
mv OpenLTE OpenLTE_service_reject_on_tau
```
```
zip -r OpenLTE_service_reject_on_tau.zip OpenLTE_service_reject_on_tau
```
```
mv OpenLTE_service_reject_on_tau.zip ../../Desktop/ltehack_backup/
```
```
cd OpenLTE_service_reject_on_tau && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
```


 
* tau_numb_attack :

```
unzip OpenLTE.zip 
```
```
cd OpenLTE
```
```
git checkout tau_numb_attack
```
```
gedit LTE_fdd_enodeb/src/LTE_fdd_enb_radio.cc
```

</br>
</br>
#look the function : bladerf_get_timestamp </br>
#Replace 

```
BLADERF_MODULE_RX
```
by 
```
BLADERF_RX 
```
</br>
</br>
#Replace all : 

```
BLADERF_MODULE_TX  
```
by  
```
BLADERF_TX_X1 
```
</br>
#Replace all : 

```
BLADERF_MODULE_RX
```
by
```
BLADERF_RX_X1 
```
</br> </br>

```   
rm -rf build/
```
```
cd ..
```
```
mv OpenLTE OpenLTE_tau_numb_attack
```
```
zip -r OpenLTE_tau_numb_attack.zip OpenLTE_tau_numb_attack
```
```
mv OpenLTE_tau_numb_attack.zip ../../Desktop/ltehack_backup/
```
```
cd OpenLTE_tau_numb_attack && mkdir build && cd build
```
```
cmake ..
```
```
make
```
```
make install
```
```
ldconfig
```
```
cd ../..
 ```




 ## Reading articles 
 * [article1](https://github.com/SitrakaResearchAndPOC/openlte_redirection/blob/main/ArticleLTE1_CS3235-SemI-2018-19-Projects.pdf)
 * [article2](https://github.com/SitrakaResearchAndPOC/openlte_redirection/blob/main/ArticleLTE2_CS3235-SemI-2018-19-Projects.pdf)
 * [article3](https://github.com/SitrakaResearchAndPOC/openlte_redirection/blob/main/ArticleLTE3_CS3235-SemI-2019-20.pdf)
 * [article4](https://github.com/SitrakaResearchAndPOC/openlte_redirection/blob/main/DEF%20CON%2024%20-%20Zhang-Shan-Forcing-Targeted-Lte-Cellphone-Into-Unsafe-Network.pdf)
 * [article5a](https://github.com/SitrakaResearchAndPOC/openlte_redirection/blob/main/lin.pdf) [article5b](https://github.com/SitrakaResearchAndPOC/openlte_redirection/blob/main/lte_redirection_huanglin.pdf)
 * [article6](https://github.com/SitrakaResearchAndPOC/openlte_redirection/blob/main/Lin_Huan_-_UE_Security.pdf) 

## Documentation bastien baranoff :   
* Redirect_4G_to_2G [link](https://pl4y.store/en/latest/Redirect_4G_to_2G.html) [pdf](https://github.com/SitrakaResearchAndPOC/openlte_redirection/blob/main/Redirect_4G_to_2G.pdf)  [videos](https://www.youtube.com/watch?v=93o9XMZXGWY)
* Hacking_4G_Redirection [link](https://pl4y.store/en/latest/Hacking_4G_Redirection.html) [pdf](https://github.com/SitrakaResearchAndPOC/openlte_redirection/blob/main/Hacking_4G_Redirection.pdf)
* telco_story [link](https://github.com/bbaranoff/telco_story) [fork_link](https://github.com/SitrakaResearchAndPOC/fork_telco_story)  
* openLTE2GSM [link](https://github.com/bbaranoff/openLTE2GSM) [fork_link](https://github.com/SitrakaResearchAndPOC/fork_openLTE2GSM)  
* LTE-Redirect-v21  [link](https://github.com/bbaranoff/LTE-Redirect-v21) [fork_link](https://github.com/SitrakaResearchAndPOC/fork_LTE-Redirect-v21)  
* openlte_redirection_patch [link](https://github.com/bbaranoff/openlte_redirection_patch) [fork_link](https://github.com/SitrakaResearchAndPOC/fork_openlte_redirection_patch)


## Code to read :
* oldcode by color_light [link](https://github.com/macherie/lteAttack) [fork_link](https://github.com/SitrakaResearchAndPOC/fork_lteAttack_redirection)
* openlte_redirection_patch [link](https://github.com/bbaranoff/openlte_redirection_patch) [fork_link](https://github.com/SitrakaResearchAndPOC/fork_openlte_redirection_patch)
* [article1](https://github.com/SitrakaResearchAndPOC/openlte_redirection/blob/main/ArticleLTE1_CS3235-SemI-2018-19-Projects.pdf)

## Videos demos 
* defcon [videos](https://www.youtube.com/watch?v=Nn8Pwz9MxSA&t=27s)
* hitb [videos](https://www.youtube.com/watch?v=hNDChDM1hEE&t=1s)
* bastien baranoff [videos1](https://www.youtube.com/watch?v=6r9qZOxY_BQ&t=36s)
[videos2](https://www.youtube.com/watch?v=GmPN6CblvaQ) [videos3](https://www.youtube.com/shorts/j5cs28u4DAo) [videos4](https://www.youtube.com/watch?v=9_qWjXa5FBI&pp=ygUVYmFzdGllbiBiYXJhbm9mZiArIDRH)  [videos5](https://www.youtube.com/watch?v=93o9XMZXGWY)
[videos6](https://www.youtube.com/watch?v=XvdtCdNAPBY&t=411s)  

## More documentations : 
https://securityaffairs.com/53180/hacking/hacking-lte-networks.html </br>
https://nse.digital/pages/guides/Wireless/lte-hacking.html </br>
https://thecybersecurityman.com/2018/07/05/the-recent-4g-lte-network-vulnerabilities-and-attacks/ </br>
https://sec.sorint.it/en/2018/03/07/4g-lte-attack-2/ </br>
https://www.sharetechnote.com/html/Communication_CellularSecurity.html </br>
https://syssec.kaist.ac.kr/pub/2019/kim_sp_2019.pdf </br>

## More videos
https://www.youtube.com/watch?v=DEeOFE_DreU </br>
https://www.youtube.com/watch?v=slnc98KYLmw </br>
wirelessoffensive in youtube

## Homemade installation :  
* https://github.com/SitrakaResearchAndPOC/Readme_hacklte/blob/main/hacklte_readme.txt  
* https://github.com/SitrakaResearchAndPOC/Readme_hacklte


