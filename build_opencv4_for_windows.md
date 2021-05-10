# Build OpenCV 4 from scratch for Windows 10

## CMake Options

```SH
pip uninstall opencv-python opencv-contrib-python
pip install numpy
```


```sh
WITH_CUDA — Checked
OPENCV_DNN_CUDA — Checked
ENABLE_FAST_MATH — Checked
OPENCV_EXTRA_MODULES_PATH — “Give path to “opencv-contrib-4.4.0
CUDA_FAST_MATH — Checked
CUDA_ARCH_BIN — 8.6
```


```SH
PYTHON3_EXECUTABLE= C:/program files/python38/python.exe
PYTHON3_INCLUDE_DIR= C:/program files/python38/include
PYTHON3_LIBRARY= C:/program files/python38/libs/python38.lib
PYTHON3_NUMPY_INCLUDE_DIRS= C:/program files/python38/Lib/site-packages/numpy/core/include
PYTHON3_PACKAGES_PATH= C:/program files/python38/Lib/site-packages


```

```sh
-DCMAKE_INSTALL_PREFIX=$(python3 -c "import sys; print(sys.prefix)")
-DPYTHON_EXECUTABLE=$(python3 -c "import sys; print(sys.executable)")
-DPYTHON_INCLUDE_DIR=$(python3 -c "import sysconfig; print(sysconfig.get_config_var('INCLUDEPY'))")
-DPYTHON_PACKAGES_PATH=$(python3 -c "import sysconfig; print(sysconfig.get_config_var('LIBDEST'))")
-DPYTHON3_NUMPY_INCLUDE_DIRS=$(python3 -c "import numpy; print(numpy.get_include())")


python3 -c "import sys; print(sys.prefix)"
which python3
python3 -c "from distutils.sysconfig import get_python_inc; print(get_python_inc())"
python3 -c "from distutils.sysconfig import get_python_lib; print(get_python_lib())"
python3 -c "import numpy; print(numpy.get_include())"
```
