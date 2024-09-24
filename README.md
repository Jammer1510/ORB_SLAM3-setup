# ORB_SLAM3-setup

Install GCC: `sudo apt install build-essential`  
Install CMake: `sudo apt install cmake`  
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
`./HelloPangolin'




