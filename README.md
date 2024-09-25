# ORB_SLAM3-setup

Install GCC: `sudo apt install build-essential`  
Install CMake: `sudo apt install cmake`  
Install OpenCV: `sudo apt install libopencv-dev`  
Install Eligen3: `sudo apt install libeigen3-dev`  
Then we: `sudo apt update`  



Install Homebrew:   
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`, once setup complete  
`echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"' >> ~/.profile`  
`eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"`  

Then Install Pangolin:  
`git clone --recursive https://github.com/stevenlovegrove/Pangolin.git`  
`cd Pangolin  `  
#Override the package manager choice and install all packages  
`./scripts/install_prerequisites.sh -m brew all`  

Configure and build  
`cmake -B build`  
`cmake --build build`

Test your Pangolin by running the following:
` cd ~/Pangolin/build/examples/HelloPangolin`  
` ./HelloPangolin `  
And this should pop up:  


![image](https://github.com/user-attachments/assets/f3bae113-290c-441e-8f7c-630efb1d11ec)  

Then we can move on to installing ORB-SLAM3:
`git clone -b c++14_comp https://github.com/UZ-SLAMLab/ORB_SLAM3.git`
`cd ORB_SLAM3`  
and open CMakeLists.txt and change openCV 4.4 to 4.2 if you have OpenCV 4.2 installed

Build `DBoW2` and `g2o`:  
`cd ~`    
`sudo apt install libboost-all-dev` 
`cd ORB_SLAM3`  
`cd Thirdparty`  
`cd DBoW2`  
`mkdir build`  
`cd build`  
`cmake ..`  
`make -j$(nproc)`  

`cd g2o`  
`mkdir build`  
`cd build`  
`cmake ..`  
`make -j$(nproc)`  



