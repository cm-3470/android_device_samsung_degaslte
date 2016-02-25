# Device configuration for Samsung Galaxy Tab 4 7.0 LTE SM-T235 (degaslte)

## Important

This tree is currently WIP meaning that it may not even boot at it's current state!

## Spec Sheet

| Feature                 | Specification                     |
| :---------------------- | :-------------------------------- |
| CPU                     | Quad-core 1.4 GHz                 |
| Chipset                 | Exynos 3 Quad 3470                |
| GPU                     | Mali-400MP4                       |
| Memory                  | 1.5GB RAM                         |
| Shipped Android Version | (4.4.2)                           |
| Storage                 | 8 GB                              |
| MicroSD                 | Up to 64GB                        |
| Battery                 | 4000 mAh                          |
| Dimensions              | 186.9 x 107.9 x 9 mm              |
| Display                 | 800 x 1280 pixels                 |
| Camera                  | 3 MP, 2048 x 1536 pixels          |
| Release Date            | May 2014                          |


## Device Picture

![Samsung Galaxy Tab 4 7.0](http://images.samsung.com/is/image/samsung/de_SM-T235NYKADBT_000241627_Front_black?$DT-Gallery$ "Samsung Galaxy Tab 4 7.0")

## How to build

0. Open a terminal at the top of your CyanogenMod 13 dir

1. Next clone the local manifests by running :

```Shell
git clone https://github.com/cm-3470/android_.repo_local_manifests -b cm-13.0 .repo/local_manifests
```

however if you already obtian local manifests ftrom a different device, just copy the following file into .repo/local_manifests :
```html
https://github.com/cm-3470/android_.repo_local_manifests/blob/cm-13.0/degaslte.xml
```

2. Once that is done, sync to sources by running the following in your terminal :

```python
repo sync
```

3. Once the sync is done, run envsetup.sh :
```makefile
. build/envsetup.sh
```

4. Now run the degaslte specific patches by entering :
```Shell
bash device/samsung/degaslte/patch/apply.sh
```

5. Now open the lunch menu by entering
```Shell
lunch
```

6. If you see the device on the list, you have successfully synced the sources. Now enter the following :
```Shell
cm_degaslte-userdebug
```

7. You're now set to compile CyanogenMod, just run the following to start compiling :
```Shell
make bacon
```

8. After the compile is done, the CM package will appear in your out directory. As default, it is set in :
```
out/target/product/degaslte/
```

9. You have now successfully compiled CyanogenMod for degaslte!
