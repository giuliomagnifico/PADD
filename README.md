# PADD

PADD (formerly Chronometer2) is a more expansive version of the original chronometer.sh that is included with [Pi-Hole](https://pi-hole.net). PADD provides in-depth information about your Pi-hole.

### Original PADD

[PADD Screenshot](https://pi-hole.github.io/graphics/Screenshots/padd.png)

### PADD-Hyper for 800x480px, 100clx32ln - Tested on Pimoroni HyperPixel 4.0 display

![PADD-Hyper](https://github.com/user-attachments/assets/6ae24843-9331-4e59-bb0d-51a084dc12dc)


***Note:** PADD has been adopted by the Pi-hole team, thanks to JPMCK for creating this helpful tool!

# Setup PADD

*For more info, check out the details in the original repo: [pi-hole/PADD](https://github.com/pi-hole/PADD)*

*More in-depth information about setting up PADD can be found in this repo’s [wiki](https://github.com/pi-hole/PADD/wiki/Setup).*

## Setup This Custom PADD

To display it correctly, you'll need an 800x480px display (I'm using the [HyperPixel 4.0 - Hi-Res Display for Raspberry Pi](https://shop.pimoroni.com/products/hyperpixel-4?variant=12569485443155)). You’ll also need to run Unbound to get the updated stats from `root.hints`.

To install this custom version, simply replace the original `padd.sh` with the modified [padd.sh](https://github.com/giuliomagnifico/PADD/blob/master/padd.sh) from this repository  (check the execution permission when you replace the file).

Launch it with a 0 offset on both the x and y axes:


```
# Run PADD

if [ "$TERM" == "linux" ] ; then
  while :
  do
    ./padd.sh --xoff 0 --yoff 0
    sleep 1
  done
fi
```
