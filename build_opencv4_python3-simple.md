```sh
$ sudo apt-get install build-essential cmake unzip pkg-config
  $ sudo apt-get install libjpeg-dev libpng-dev libtiff-dev
$ sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
$ sudo apt-get install libxvidcore-dev libx264-dev
  
  184  sudo apt-get install libgtk-3-dev
  $ sudo apt-get install libatlas-base-dev gfortran
  185  sudo apt-get install python3-dev
  
  
  $ wget https://bootstrap.pypa.io/get-pip.py
  186  sudo python3 get-pip.py
  188  sudo rm -rf ~/.cache/pip
  
  $ sudo pip install virtualenv virtualenvwrapper
  
  190  mkvirtualenv cv -p python3
  191  workon cv
  
  $ echo -e "\n# virtualenv and virtualenvwrapper" >> ~/.bashrc
$ echo "export WORKON_HOME=$HOME/.virtualenvs" >> ~/.bashrc
$ echo "export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3" >> ~/.bashrc
$ echo "source /usr/local/bin/virtualenvwrapper.sh" >> ~/.bashrc
  
  192  pip install numpy
  197  cmake -D CMAKE_BUILD_TYPE=RELEASE -D CMAKE_INSTALL_PREFIX=/usr/local -D INSTALL_PYTHON_EXAMPLES=ON -D INSTALL_C_EXAMPLES=OFF -D OPENCV_ENABLE_NONFREE=ON -D OPENCV_EXTRA_MODULES_PATH='/home/usv/opencv_contrib-4.5.2/modules' -D PYTHON_EXECUTABLE=~/.virtualenvs/cv/bin/python -D BUILD_EXAMPLES=ON ..

sudo make install
sudo ldconfig

$ workon cv
:/usr/local/lib/python3.6/site-packages/cv2/python-3.6$ python3 --version
Python 3.6.9
:/usr/local/lib/python3.6/site-packages/cv2/python-3.6$ ll
total 8452
drwxr-sr-x 2 root staff    4096 Apr 30 13:19 ./
drwxr-sr-x 3 root staff    4096 Apr 30 13:19 ../
-rw-r--r-- 1 root staff 8646352 Apr 30 13:18 cv2.cpython-36m-x86_64-linux-gnu.so
:/usr/local/lib/python3.6/site-packages/cv2/python-3.6$ 

(cv)  :~/.virtualenvs/cv/lib/python3.6/site-packages$ python
Python 3.6.9 (default, Jan 26 2021, 15:33:00) 
[GCC 8.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import cv2
>>> cv2.__version__
'4.5.2'
>>> quit()

```
