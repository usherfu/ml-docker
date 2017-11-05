##
download tensorflow base docker image repo
https://github.com/tensorflow/tensorflow.git

under folder  /tensorflow/tensorflow/tools/docker

Build docker image from source (CPU or GPU)
```bash
 docker build --pull -t $USER/tensorflow-suffix -f Dockerfile.suffix .
```

## Install keras for python3

apt-get update  && apt-get install python3-pip
pip3 install keras


## Install tensorflow

pip3 install tensorflow
or
pip3 install tensorflow-gpu


## Install PIL
pip3 install pillow flask


wget https://bootstrap.pypa.io/get-pip.py
$ sudo python3 get-pip.py

install opencv http://www.pyimagesearch.com/2015/07/20/install-opencv-3-0-and-python-3-4-on-ubuntu/

##tips:
pip3 freeze: check python modules version

Check which tensorflow version is installed
https://stackoverflow.com/questions/38549253/how-to-find-which-version-of-tensorflow-is-installed-in-my-system

Difference between devel and runtime
https://github.com/NVIDIA/nvidia-docker/wiki/CUDA




## Troubleshooting

1. OSError: protocol not found
  File "/usr/local/lib/python3.5/dist-packages/eventlet/support/dns/rdtypes/IN/WKS.py", line 23, in <module>
    _proto_tcp = socket.getprotobyname('tcp')
OSError: protocol not found
[Solution](https://stackoverflow.com/questions/40184788/protocol-not-found-socket-getprotobyname)


## Clean up docker folder aufs/diff
- Sort folder size 
```bash 	
 	sudo du -H --max-depth=1 /var/lib/docker/aufs/ | sort -n -r
```

- Clean up docker folder /var/lib/docker/aufs/
```bash
	docker run --rm -v /var/run/docker.sock:/var/run/docker.sock -v /etc:/etc spotify/docker-gc 
```