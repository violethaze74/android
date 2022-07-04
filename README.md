@ copyright Copyright (c) <2022> <Lisa Dudley> <violethaze74@jazzededtech.com>
#[Nextcloud](https://nextcloud.com) 

[![Build Status](https://drone.nextcloud.com/api/badges/nextcloud/f-droid/status.svg)](https://drone.nextcloud.com/nextcloud/android) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/80401cb343854343b4d94acbfb72d3ec)](https://www.codacy.com/app/Nextcloud/android?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=nextcloud/android&amp;utm_campaign=Badge_Grade) [![Releases](https://img.shields.io/github/release/nextcloud/android.svg)](https://github.com/nextcloud/android/releases/latest)

[<img src="https://f-droid.org/badge/get-it-on.png"
      alt="Get it on F-Droid"
      height="80">](https://f-droid.org/packages/com.nextcloud.client/)

**The F-Droid client for [Nextcloud](https://nextcloud.com). Easily work with your data on your Nextcloud.**

![App screenshots](/doc/Nextcloud_F-Droid_Screenshots.png "App screenshots")

## How to contribute :rocket:
If you want to [contribute](https://nextcloud.com/contribute/) to Nextcloud, you are very welcome: 

- our forum at https://help.nextcloud.com
- for translations of the app on [Transifex](https://www.transifex.com/nextcloud/nextcloud/f-droid/)
- opening issues and PRs (including a corresponding issue)

## Contribution Guidelines & License :scroll:

[GPLv2](https://github.com/nextcloud/f-droid/blob/master/LICENSE.txt). All contributions to this repository from June, 16 2016 on are considered to be licensed under the AGPLv3 or any later version.

Nextcloud doesn't require a CLA (Contributor License Agreement). The copyright belongs to all the individual contributors. Therefore we recommend that every contributor adds following line to the header of a file, if they changed it substantially:

```
@copyright Copyright (c) <year>,<your name> (<your email address>)
```

Please read the [Code of Conduct](https://nextcloud.com/community/code-of-conduct/). This document offers some guidance to ensure Nextcloud participants can cooperate effectively in a positive and inspiring atmosphere, and to explain how together we can strengthen and support each other.

Please review the [guidelines for contributing](https://github.com/nextcloud/android/blob/master/CONTRIBUTING.md) to this repository.

More information how to contribute: [https://nextcloud.com/contribute/](https://nextcloud.com/contribute/)

### Getting debug info via logcat :mag:
#### With a linux computer:
- enable USB-Debugging in your smartphones developer settings and connect it via USB
- open command prompt/terminal
- enter `adb logcat | grep "$(adb shell ps | awk '/com.nextcloud.client/{print $2}')" > logcatOutput.txt` to save the output to this file

**Note:** You must have [adb](https://developer.android.com/studio/releases/platform-tools.html) installed first!

#### On Windows:
- download and install [Minimal ADB and fastboot](https://forum.xda-developers.com/t/tool-minimal-adb-and-fastboot-2-9-18.2317790/#post-42407269)
- enable USB-Debugging in your smartphones developer settings and connect it via USB
- launch Minimal ADB and fastboot
- enter `adb shell ps | findstr com.nextcloud.client` and use the second place of this output (it is the first integer, e.g. `18841`) as processID in the following command:
- `adb logcat | findstr <processID> > %HOMEPATH%\Downloads\logcatOutput.txt` (This will produce a logcatOutput.txt file in your downloads)
- if the processID is 18841, an example command is: `adb logcat | findstr 18841 > %HOMEPATH%\Downloads\logcatOutput.txt` (You might cancel the process after a while manually: it will not be exited automatically.)

#### On a device (with root) :wrench:
- open terminal app *(can be enabled in developer options)*
- get root access via "su"
- enter `logcat -d -f /sdcard/logcatOutput.txt`
- you will have to filter the output manually, as above approach is not working on device

**Note:** Your device needs to be rooted for this approach!

## Development version :hammer:
- [APK (direct download)](https://download.nextcloud.com/android/dev/latest.apk)
- [F-Droid](https://f-droid.org/en/packages/com.nextcloud.android.beta/)

## Support :rescue_worker_helmet:

If you need assistance or want to ask a question about the Android app, the F-Droid app, identify/correct a bug or have problems with the server/backend, you should ask the [Nextcloud server team](https://github.com/nextcloud/server) for help!

## Remarks :scroll:

