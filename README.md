# arftracksat: A (no longer CLI only) satellite tracking software for linux
SGDP-4 adaptation shamelessly copied from BatchDrake's suscan.

## Building
Install dependencies
```
sudo apt update
sudo apt install nlohmann-json3-dev libcurl4-openssl-dev libcurlpp-dev libgl1-mesa-dev libglu1-mesa-dev freeglut3-dev
```
Build
```
git clone https://github.com/arf20/arftracksat
cd arftracksat/
mkdir build
cd build
cmake ..
make
sudo make install
```
You may add -j<CPUs> to the make command to build faster.

## Configuring
The default config.json located at /usr/local/etc/arftracksat/ after install should work out of the box
```
Value           Description
tleroot:        Location to get and load TLE files, must be writable by the user,
                note: this default will delete TLEs after reboot. Modification advised
tlefile:        TLE filename to load from tleroot
tlesources:     A array of URLs to curl get into tleroot
updatePerdiod:  Screen update period in milliseconds
station:        Station data
  name:           Name
  lat:            Geodetic latitude
  lon:            East longitude
  hgt:            Altitude (height) over sea level in meters
show:           Array to only show sats by name. Leave empty to show all (possibly not good performing)
columns:        Sat data to show in columns in order
                name, azel, dis, geo, tab, pos, vel
```

# Where Windows?
I just broke support lol

Old VS project in my personal repos: https://arf20.com/source/arftracksat (it sucks)

# Support & help
https://discord.gg/GpgrnDQqtr
