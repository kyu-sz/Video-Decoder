# Video Decoder

[![AUR](https://img.shields.io/aur/license/yaourt.svg?maxAge=2592000)](LICENSE)

Video Decoder is a tool for decoding video stored in memory.

## Installation

It depends on FFMPEG. To build this tool, you should have avcodec, avformat, avutil and swscale installed on your 
machine. For Ubuntu, use the following commands to install:

```Shell
sudo apt-get install libavcodec-dev libavformat-dev libavutil-dev libswscale-dev
```

Also to test this tool, you should have OpenCV:

```Shell
sudo apt-get install libopencv-dev
```

As for CentOS 7, these libraries are available on Nux Desktop:

```bash
rpm --import http://li.nux.ro/download/nux/RPM-GPG-KEY-nux.ro 
rpm -Uvh http://li.nux.ro/download/nux/dextop/el7/x86_64/nux-dextop-release-0-1.el7.nux.noarch.rpm
yum repolist
yum install ffmpeg-devel
```

The video decoder is a header-only tool. To use it in your code, including the [video_decoder.hpp](inc/video_decoder.hpp) is enough.

To use it in Java, JNI wrapper building is supported with CMake. To build the JNI shared library, run in your console under the project directory:

```Shell
cmake .
make -j 4
sudo make install
```

If you want to enable test, run:

```Shell
cmake [-DTEST_VIDEO_PATH=/path/to/your/test/video] .
make -j 4 test
cd bin
ctest
``` 