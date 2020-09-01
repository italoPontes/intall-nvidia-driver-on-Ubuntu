# Intall Nvidia driver on Ubuntu 

A simple and fast tutorial to install Nvidia drivers on Ubuntu 18.04 LTS version.

**Step 1: Download the Nvidia driver.**

Click on badge above to be redirect to Nvidia website and fill the form with your GPU card informations as the following image:

[<img src="https://images.bjorn3d.com/Material/revimages/video/Nvidia_GTX680/NV_GF_GTX_preferred_badge_FOR_WEB_ONLY.png" width="150" />](https://www.nvidia.com/Download/index.aspx)

<figure>
  <img src="/img/nvidia_driver_screenshot.png" alt="Caption text">
  <figcaption>If you don't know what is your GPU model, type this command in terminal: </figcaption>
</figure>

```console
foo@bar:~$ ubuntu-drivers devices
```

<figure>
  <img src="/img/ubuntu-drivers-devices.png" alt="Caption text">
</figure>

**Step 2: Run the following commands:

```console
foo@bar:~$ sudo apt-get install gcc make
foo@bar:~$ sudo bash -c "echo blacklist nouveau > /etc/modprobe.d/blacklist-nvidia-nouveau.conf"
foo@bar:~$ sudo bash -c "echo options nouveau modeset=0 >> /etc/modprobe.d/blacklist-nvidia-nouveau.conf"
foo@bar:~$ sudo update-initramfs -u
foo@bar:~$ sudo reboot
```


**Add permissions to execute the file.**

```console
foo@bar:~$ chmod +x NVIDIA-Linux-x86_64-450.66.run
```
