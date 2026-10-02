# CipherGuard

**Static analysis.** Level: approachable — this is the one to start with.

Everything you need is already inside the file. Nothing is generated at runtime, nothing
depends on the device, and you never need to run the app to finish it — though running it
will tell you whether you are right.

If you find yourself reaching for Frida here, stop and go back to the file. The whole point
of this one is that the answer shipped with it.

## Install

```bash
adb install cipherguard.apk
```

`arm64-v8a` and `x86_64`, so an emulator is fine.

## What done looks like

The app tells you when you are right. No flag is ever printed by accident, and nothing you
see on screen before you solve it is the answer.

## Please don't

Post the flag, or a walkthrough, in the issues. Someone else is three hours in.
