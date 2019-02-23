### LinuxTricks

# Change SWAP file size while Ubuntu is running

Founded at https://bogdancornianu.com/change-swap-size-in-ubuntu/
1. Turn off all swap processes 
```
sudo swapoff -a
```
2. Resize the swap 
```
sudo dd if=/dev/zero of=/swapfile bs=1G count=8
```
3. Make the file usable as swap 
```
sudo mkswap /swapfile
```
4. Activate the swap file 
```
sudo swapon /swapfile
```
5. Check the amount of swap available 
```
grep SwapTotal /proc/meminfo
```
One liner:
```
sudo swapoff -a;sudo dd if=/dev/zero of=/swapfile bs=1G count=8;sudo mkswap /swapfile;sudo swapon /swapfile;grep SwapTotal /proc/meminfo
```

# Enable Vulkan drivers support at wine 


# Ubuntu 18.10 sound problem at Gigabyte X470 AORUS GAMING 7 WIFI motherboard
1. Install and run pavucontrol
```
sudo apt-get install pavucontrol -y; pavucontrol
```
2. In my case go to: "Output Devices" and change "Port: Line Out (plugged in)" to "Headphones (unplugged)

sudo apt remove --purge alsa-base pulseaudio
sudo apt install alsa-base pulseaudio
