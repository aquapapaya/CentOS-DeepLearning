# CentOS-DeepLearning
## Install Python3.6
> using root to install python
1. cd /usr/src
2. wget https://www.python.org/ftp/python/3.6.7/Python-3.6.7.tgz
3. tar xzf Python-3.6.7.tgz
4. cd Python-3.6.7
5. ./configure --enable-optimizations
6. make altinstall // **avoid new version substituting old version**
7. cd /usr/bin
8. ln -s /usr/src/Python-3.6.7/python python3
9. python3 -v
## Install pip3
> using root to install pip3
1. curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
2. python get-pip.py
3. pip3 --version
