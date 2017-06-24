Try to run https://github.com/upul/Behavioral-Cloning

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


##
Install PIL
pip3 install pillow flask

Install vim

???? apt-get install python-opencv

apt-get install -y python-tk



wget https://bootstrap.pypa.io/get-pip.py
$ sudo python3 get-pip.py

install opencv http://www.pyimagesearch.com/2015/07/20/install-opencv-3-0-and-python-3-4-on-ubuntu/



##tips:
pip3 freeze: check python modules version

Check which tensorflow version is installed
https://stackoverflow.com/questions/38549253/how-to-find-which-version-of-tensorflow-is-installed-in-my-system

Difference between devel and runtime
https://github.com/NVIDIA/nvidia-docker/wiki/CUDA




## troubleshooting

1. OSError: protocol not found
  File "/usr/local/lib/python3.5/dist-packages/eventlet/support/dns/rdtypes/IN/WKS.py", line 23, in <module>
    _proto_tcp = socket.getprotobyname('tcp')
OSError: protocol not found

Solution:
https://stackoverflow.com/questions/40184788/protocol-not-found-socket-getprotobyname


