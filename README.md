# build-opencv-script

## ubuntu 18.04 / Opencv 4.4.x

```sh
sudo apt install libopenblas-dev,libopenblas-base
sudo apt install liblapacke-dev
sudo ln -s /usr/include/lapacke.h /usr/include/x86_64-linux-gnu # corrected path for the library 
export Open_BLAS_INCLUDE_SEARCH_PATHS=/usr/include/x86_64-linux-gnu
export Open_BLAS_LIB_SEARCH_PATHS=/usr/lib/x86_64-linux-gnu

```

```sh

sudo apt install python3-opencv
python3 -c "import cv2; print(cv2.__version__)"

sudo apt install build-essential cmake git pkg-config libgtk-3-dev \
    libavcodec-dev libavformat-dev libswscale-dev libv4l-dev \
    libxvidcore-dev libx264-dev libjpeg-dev libpng-dev libtiff-dev \
    gfortran openexr libatlas-base-dev python3-dev python3-numpy \
    libtbb2 libtbb-dev libdc1394-22-dev
    
cmake -D CMAKE_BUILD_TYPE=RELEASE \
    -D CMAKE_INSTALL_PREFIX=/usr/local \
    -D INSTALL_C_EXAMPLES=ON \
    -D INSTALL_PYTHON_EXAMPLES=ON \
    -D OPENCV_GENERATE_PKGCONFIG=ON \
    -D OPENCV_EXTRA_MODULES_PATH=~/opencv_build/opencv_contrib/modules \
    -D BUILD_EXAMPLES=ON ..
    
pkg-config --modversion opencv4
python3 -c "import cv2; print(cv2.__version__)"

```
