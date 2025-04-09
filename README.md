# linux-rocm-guide

## How to install ROCm

Execute the follow in terminal:

```bash
sudo apt update
sudo apt install "linux-headers-$(uname -r)" "linux-modules-extra-$(uname -r)"
sudo apt install python3-setuptools python3-wheel
sudo usermod -a -G render,video $LOGNAME # Add the current user to the render and video groups
wget https://repo.radeon.com/amdgpu-install/6.3.3/ubuntu/noble/amdgpu-install_6.3.60303-1_all.deb
sudo apt install ./amdgpu-install_6.3.60303-1_all.deb
sudo apt update
sudo apt install amdgpu-dkms rocm
```

![alt text](image.png)

Set a password:

![alt text](image-1.png)

Execute the following:

```bash
sudo usermod -aG video $USER
sudo usermod -aG render $USER
```

After this, just reboot.

```bash
sudo reboot
```

![alt text](image-3.png)

![alt text](image-4.png)

Put the password we setted a few moments before ad reboot..

![alt text](image-5.png)

Check the installation with:

```bash
rocminfo | grep gfx
```

[Complete video here](https://www.youtube.com/watch?v=NhGtBL4fi0c)

## How to install Pytorch

### Create environment

### Install inside environment

### Script to setup and change over environments