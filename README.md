# GiGa-Team
Surveillance Camera project 

We have implemented following codes one by one:
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install build-essential
sudo apt-get install cmake
sudo apt-get install gfortran
sudo apt-get install git
sudo apt-get install wget
sudo apt-get install curl
sudo apt-get install graphicsmagick
sudo apt-get install libgraphicsmagick1-dev
sudo apt-get install libatlas-base-dev
sudo apt-get install libavcodec-dev
sudo apt-get install libavformat-dev
sudo apt-get install libboost-all-dev
sudo apt-get install libgtk2.0-dev
sudo apt-get install libjpeg-dev
sudo apt-get install liblapack-dev
sudo apt-get install libswscale-dev
sudo apt-get install pkg-config
sudo apt-get install python3-dev
sudo apt-get install python3-numpy
sudo apt-get install python3-pip
sudo apt-get install zip
sudo apt-get clean

For our Camera we have insitalled followings on Raspberry Pi:
sudo apt-get install python3-picamera
sudo pip3 install --upgrade picamera[array]

Next step was insreasing SWAP file:
sudo nano /etc/dphys-swapfile   ===> Change CONF_SWAPSIZE=100 to CONF_SWAPSIZE=1024 and save / exit nano
sudo /etc/init.d/dphys-swapfile 

Next step is about Git clone and Installing dlib library:
mkdir -p dlib
git clone -b 'v19.6' --single-branch https://github.com/davisking/dlib.git dlib/
cd ./dlib
sudo apt-get install cmake
mkdir build; cd build; cmake .. ; cmake --build 

Installing dlib via pip3:
pip3 install dlib

Next step is installing supporting dlib libraries:
pip3 install numpy
pip3 install scikit-image
sudo apt-get install python3-scipy
sudo apt-get install libatlas-base-dev
sudo apt-get install libjasper-dev
sudo apt-get install libqtgui4
sudo apt-get install python3-pyqt5
sudo apt install libqt4-test
pip3 install opencv-python==3.4.6.27
pip3 install face_recognition

We cloned the face recognition library:
git clone --single-branch https://github.com/ageitgey/face_recognition.git
cd ./face_recognition/examples && python3 facerec_on_raspberry_pi.py
python3 facerec_on_raspberry_pi.py
