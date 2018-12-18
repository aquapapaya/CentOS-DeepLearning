# CentOS 7-DeepLearning
## Install Python 3.6.7
> using root to install python
1. cd /usr/src
2. wget https://www.python.org/ftp/python/3.6.7/Python-3.6.7.tgz
3. tar xzf Python-3.6.7.tgz
4. cd Python-3.6.7
5. ./configure --enable-optimizations
6. make altinstall // *avoid new version substituting old version*
7. cd /usr/bin
8. ln -s /usr/src/Python-3.6.7/python python3
9. python3 -v
## Install pip3
> using root to install pip3
1. curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
2. python get-pip.py
3. pip3 --version
## Install GCC 6.4.0
> using root to install GCC
1. wget ftp://ftp.yzu.edu.tw/gnu/gcc/gcc-6.4.0/gcc-6.4.0.tar.gz
2. tar xzf gcc-6.4.0.tar.gz
3. cd gcc-6.4.0
4. ./contrib/download_prerequisites
5. cd ..
6. mkdir build_gcc-6.4.0
7. cd build_gcc-6.4.0
8. ../gcc-6.4.0/configure --prefix=/usr/local/gcc-6.4.0 --disable-multilib
9. make
10. make install
11. cd /usr/bin
12. ln -s /usr/local/gcc-6.4.0/bin/gcc gcc640
13. ln -s /usr/local/gcc-6.4.0/bin/g++ g++640
14. gcc640 --version
15. g++640 --version
