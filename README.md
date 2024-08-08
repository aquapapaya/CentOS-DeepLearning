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
9. make -j4
10. make install
11. cd /usr/bin
12. ln -s /usr/local/gcc-6.4.0/bin/gcc gcc640
13. ln -s /usr/local/gcc-6.4.0/bin/g++ g++640
14. gcc640 --version
15. g++640 --version
----------------------------------------------------------------------
Libraries have been installed in: /usr/local/gcc-6.4.0/lib/../lib64

If you ever happen to want to link against installed libraries
in a given directory, LIBDIR, you must either use libtool, and
specify the full pathname of the library, or use the `-LLIBDIR'
flag during linking and do at least one of the following:
   - add LIBDIR to the `LD_LIBRARY_PATH' environment variable
     during execution
   - add LIBDIR to the `LD_RUN_PATH' environment variable
     during linking
   - use the `-Wl,-rpath -Wl,LIBDIR' linker flag
   - have your system administrator add LIBDIR to `/etc/ld.so.conf'

See any operating system documentation about shared libraries for
more information, such as the ld(1) and ld.so(8) manual pages.
