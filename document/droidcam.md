# Install droidcam 
Droidcam connect computer with android camera

## Reuirement
- yay ( AUR helpher )
- Kernel header ( 'uname -r' )
- v4l2loopback 

## kernel header
1. `uname -r # to find computer kernel header`
2. `core/linux54-headers 5.4.150-1 [installed] # example`

## Install v4l2loopback 
```
git clone git@github.com:umlaeute/v4l2loopback.git
cd v4l2*
make 
make clean
make && sudo make install
sudo depmod -a
sudo modprobe v4l2loopback
```

## install droidcam 
`yay -S droidcam`
just type `droidcam` in terminal

## Refrence 
- https://www.dev47apps.com/droidcam/linux/
- https://bbs.archlinux.org/viewtopic.php?id=179918
- https://github.com/umlaeute/v4l2loopback
