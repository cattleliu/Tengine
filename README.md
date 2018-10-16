# Tengine for Rasberry Pi(Education Edition)
## For education only!     

Tengine, developed by OPEN AI LAB, is a lite, high-performance, and modular inference engine for embedded device.    
Github: https://github.com/OAID/Tengine     

## Installation

1. Install tools & libraries       
    ```bash
    sudo apt-get install git cmake

    sudo apt-get install libprotobuf-dev protobuf-compiler
    sudo apt-get install libboost-all-dev
    sudo apt-get install libgoogle-glog-dev
    sudo apt-get install libopencv-dev
    sudo apt-get install libopenblas-dev
    ```    

2. Get Tengine code       
    ```bash
    git clone https://github.com/OAID/Tengine.git
    ```    

3. Prepare config files    
    * copy config example file
        ```bash
        cd ~/Tengine
        cp makefile.config.example makefile.config
        ```
    * edit `makefile.config`            
        * comment `CONFIG_ARCH_ARM64` option to invalid arm64 arch.       
        * uncomment `CONFIG_ARCH_BLAS=y` option to valid Openblas arch.        

4. Build          
    ```bash
    make -j4
    ```

5. Get the binary library      
    Replace `Tengine/install/lib/libtengine.so` with the new one.

## Example       
Reference: [树莓派也能玩转深度学习——Tengine推断引擎/测试 | Hey~YaHei!](http://hey-yahei.cn/2018/10/13/RasPi-Tengine/#%E6%B5%8B%E8%AF%95)      
    
With Tengine for Rasberry Pi(Education Edition), SPF(Second Per Frame) of mobilenet-ssd model drops from **1.148** to **0.286**.     