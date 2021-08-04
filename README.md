# eBPF
Program kernel to enable eBPF
Steps to install bpf in the kernel if it is not already present , in aws which is usually the case...
Install zlib
Install libelf-dev
  sudo apt install libelf-dev
sudo apt-get install -y gcc-multilib

Install libbpf from the github repo....
git pull https://github.com/sudipm-mukherjee/libbpf
cd src
sudo apt install -y make
sudo make


PKG_CONFIG_PATH=/usr/src DESTDIR=/usr/src sudo make install
PKG_CONFIG_PATH=/usr/include DESTDIR=/usr/include sudo make install

the bpf will be installed in /usr/include/bpf directory.....
