# problems_library

1.libpython3.7m.so.1.0: cannot open shared object file
    ImportError: libpython3.7m.so.1.0: cannot open shared object file: No such file or directory
    
    after sudo ldconfig /home/usr/anaconda3/lib
    run sudo apt-get install libpython3.7


2.ubuntu20.04 + cuda10.1 + cudnn + chrome

nvidia-smi

sudo apt-get update
sudo apt-get upgrade

#upgrade all the software from command line & software updater, after that , the nvidia driver will be updated already

wget http://developer.download.nvidia.com/compute/cuda/10.1/Prod/local_installers/cuda_10.1.243_418.87.00_linux.run

sudo apt-get install gcc-7 g++-7

sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-7 9
sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-9 1

sudo update-alternatives --display gcc

sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-7 9
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-9 1

sudo update-alternatives --display g++

sudo sh cuda_10.1.243_418.87.00_linux.run

gedit ~/.bashrc

export PATH=/usr/local/cuda-10.1/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATH=/usr/local/cuda-10.1/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}

source ~/.bashrc

cd Downloads/

tar zxvf ./cudnn-10.1-linux-x64-v7.6.5.32.tgz -C ./

sudo cp cuda/include/cudnn.h /usr/local/cuda/include/
sudo cp cuda/lib64/libcudnn* /usr/local/cuda/lib64/

sudo chmod 755 /usr/local/cuda/include/cudnn.h /usr/local/cuda/lib64/libcudnn*

cd ~

#chrome
wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb

sudo apt install ./google-chrome-stable_current_amd64.deb

google-chrome