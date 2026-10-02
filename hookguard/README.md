# HookGuard

**Dynamic analysis.** Level: the hard one.

The secrets are nowhere in the file. They are built on the device, and the thing you are
after does not exist until you ask for it — so no amount of reading the binary alone will
hand it to you. You will have to run it, and the app has opinions about that.

Expect to be fought. When it stops, it stops deliberately; treat every exit as information
rather than a bug, and ask what the app learned immediately before it died.

## Install

```bash
adb install hookguard.apk
```

**A real arm64 device is required.** This app ships `arm64-v8a` only — an x86 emulator image
will not run it. You will also want root or a device you can instrument.

## What done looks like

The app confirms each secret as you reach it, and it will not confirm something that is not
one. If it has not told you you are right, you are not finished.

## Please don't

Post flags, or any part of a bypass, in the issues.
