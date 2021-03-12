 Start a container based on NVIDIA-CUDA docker images. 
 
 ```bash
docker run -it --rm nvidia/cuda:10.1-devel /bin/bash
```
 
Then update the distro.
 
```bash
apt-get update -y
apt-get upgrade -y
```
 
Install Python 3.8

```bash
apt-get install software-properties-common -y
add-apt-repository ppa:deadsnakes/ppa -y
apt-get update -y
apt-get install python3.8-dev -y
apt-get install python3-venv -y
apt-get install python3-pip -y
```

Make Python3.8 default.

```bash
update-alternatives --install /usr/bin/python python /usr/bin/python3.8 1
update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.8 1
```
Now install shap.

```pip3 install shap
```
