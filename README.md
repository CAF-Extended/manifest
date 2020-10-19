<p align="center">
  <img src="https://i.imgur.com/A5riwr0.png"/>
</p>

CAF-Extended Eleven

Pure CAF rom with minimal Customisations


How to Build?
-------------

To initialize your local repository using the AospExtended trees, use a 
command like this:

```bash
  repo init -u https://github.com/CAF-Extended/manifest -b 11.0
```
To initialize a shallow clone, which will save even more space & time, use a command like this:

```bash
  repo init --depth=1 -u https://github.com/CAF-Extended/manifest -b 11.0
```
  
Then to sync up:
----------------

```bash
  repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```
Finally to build:
-----------------

```bash
  . build/envsetup.sh
  lunch cafex_device_codename-userdebug
  m cafex -j$(nproc --all) | tee log.txt
```
