
#### Missing modules/software for current docker

```bash
apt-get update && apt-get upgrade -y
apt-get install -y libcudnn5 python3-tk vim python-matplotlib
apt-get -o Dpkg::Options::="--force-confmiss" install -y --reinstall netbase

```

#### Actually need to pin opencv-python to version ==3.2.0.8 https://github.com/ray-project/ray/issues/923 https://github.com/ray-project/ray/pull/926/files

```bash
pip3 install eventlet python-socketio pillow flask pandas opencv-python matplotlib h5py
pip3 install --upgrade tensorflow tensorflow-gpu
```

#### How to build docker image
- build gpu version
```bash
	sudo docker build --pull -t ml-docker-devel-gpu -f Dockerfile.devel-gpu .
```
- build cpu version
```bash
	sudo docker build --pull -t ml-docker-devel-cpu -f Dockerfile.devel .
```

#### How to start docker instance

```bash
	sudo nvidia-docker run -it --rm -v ~/Work/repo/OthersCarND/Behavioral-Cloning:/sharedfolder -p 4567:4567 ml-docker-devel-gpu bash
```

#### How to start docker instance with DISPLAY support
```bash
sudo nvidia-docker run -it --rm -v /tmp/.X11-unix:/tmp/.X11-unix -v $XAUTHORITY:$XAUTHORITY -e XAUTHORITY=$XAUTHORITY -h $(hostname) -e DISPLAY=$DISPLAY -v ~/Work/repo/OthersCarND/jeremy-shannon/CarND-Behavioral-Cloning-Project:/sharedfolder -p 4567:4567 ml-docker-devel-gpu  bash
```
