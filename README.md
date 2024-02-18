# openlte_redirection

## Installation : 
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

-            usrp->set_tx_antenna("BAND2");

+           usrp->set_rx_antenna("LNAH");

             // Setup the TX and RX streams

             tx_stream  = usrp->get_tx_stream(stream_args);

             rx_stream  = usrp->get_rx_stream(stream_args);

# */
```

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



git clone https://github.com/ettusresearch/uhd
cd uhd/
git checkout aea0e2de34803d5ea8f25d7cf2fb08f4ab9d43f0


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

## Homemade installation :  
* https://github.com/SitrakaResearchAndPOC/Readme_hacklte/blob/main/hacklte_readme.txt  
* https://github.com/SitrakaResearchAndPOC/Readme_hacklte


