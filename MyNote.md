Try to run https://github.com/upul/Behavioral-Cloning

#missing modules/software for current docker
apt-get update && apt-get upgrade -y
apt-get install -y libcudnn5 python3-tk vim python-matplotlib
apt-get -o Dpkg::Options::="--force-confmiss" install -y --reinstall netbase
pip3 install eventlet python-socketio pillow flask pandas opencv-python matplotlib h5py
pip3 install --upgrade tensorflow tensorflow-gpu

#How to build docker image
- build gpu version
```bash
	sudo docker build --pull -t ml-docker-devel-gpu -f Dockerfile.devel-gpu .
```
- build cpu version
```bash
	sudo docker build --pull -t ml-docker-devel-cpu -f Dockerfile.devel .
```

## How to start docker instance
```bash
	sudo nvidia-docker run -it --rm -v ~/Work/repo/Behavioral-Cloning/:/sharedfolder -p 4567:4567 ml-docker-devel-gpu bash
```

## run python script to autonomous drive
python3 drive.py model.json


Steering ratio
- https://zhengludwig.wordpress.com/projects/self-driving-rc-car/
 build CNN to directly predict "left, right, forward, reverse"

https://medium.com/@ksakmann/behavioral-cloning-make-a-car-drive-like-yourself-dc6021152713


center,left,right,steering,throttle,brake,speed



1. collect data and preprocessing the data (augmentation, steering and etc)
2. train the model with collected data
3. test model