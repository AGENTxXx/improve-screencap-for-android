Improve your android screencap.

Article in Russian: 

This project was compiled using the NDK (Mac OS Mojave) for Android 6.0. For another version, you need to replace ***.so** files in **./project**, as well as, possibly, some ***.h** files. Compilation was carried out under ARMv7.

The command to compile:
`./bin/clang -pie ./project/screencap.cpp ./project/*.so -o ./project/screencap -Wl,--unresolved-symbols=ignore-all -s`

Upload screencap to phone;
`adb shell ./project/screencap /data/local/tmp`

And run for check:
`adb shell`
`cd /data/local/tmp`
`//Print pixel color (HEX RGBA format). Example FF0000FF is RED`
`./screencap -с 400 400`
`./screencap -r /sdcard/test.png 0 0 500 500`
