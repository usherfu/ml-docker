##
download tensorflow base docker image repo
https://github.com/tensorflow/tensorflow.git

under folder  /tensorflow/tensorflow/tools/docker

Build docker image from source (CPU or GPU)
 docker build --pull -t $USER/tensorflow-suffix -f Dockerfile.suffix .


##
Install keras for python3

apt-get update  && apt-get install python3-pip
pip3 install keras


##
Install tensorflow

pip3 install tensorflow
or
pip3 install tensorflow-gpu








##tips:
pip3 freeze: check python modules version

Check which tensorflow version is installed
https://stackoverflow.com/questions/38549253/how-to-find-which-version-of-tensorflow-is-installed-in-my-system

Difference between devel and runtime
https://github.com/NVIDIA/nvidia-docker/wiki/CUDA

