# adb

> Android Debug Bridge: communicate with an Android emulator instance or connected Android devices.

- Check whether the adb server process is running and start it:

`adb start-server`

- Terminate the adb server process:

`adb kill-server`

- Start a remote shell in the target emulator/device instance:

`adb shell`

- Push an Android application to an emulator/device:

`adb install -r {{path/to/file.apk}}`

- Copy a file/folder from the target device:

`adb pull {{path/to/device_file_or_folder}} {{path/to/local_destination_folder}}`

- Copy a file/folder to the target device:

`adb push {{path/to/local_file_or_folder}} {{path/to/device_destination_folder}}`

- Get a list of connected devices:

`adb devices`
- backup one app

`adb backup -f {{filename}} -noapk {{appname}}`
`adb backup -f net.mx17.overridedns.ab -noapk net.mx17.overridedns`



- List packages

`adb shell cmd package list packages`


- Restore file

`adb restore {{file.ab}}`


- log phone

`adb logcat`

- package download and examine
`adb shell pm list {package}`
`adb shell pm path {package}`
`adb pull {path}`
`qark --apk base.apk`
