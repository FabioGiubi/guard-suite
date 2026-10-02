# NetGuard

**Public Key pinning.** Level: the one with the most moving parts.

Three cards, each a different refusal. Getting the traffic in front of you is the harder half
of this app — the part most pinning exercises skip, because they assume you already have a
proxy in the path and the only question left is the pin itself. Here it is not.

Work card by card. Each one fails differently, and the difference *is* the information.
Two of the refusals report the same message for different reasons; telling those two apart is
the exercise.

## Install

```bash
adb install netguard.apk
```

`arm64-v8a` and `x86_64`. You will want an intercepting proxy and a device you control.

## If a card is red before you have started

NetGuard pins live public endpoints, so it depends on certificates it does not control. Those
rotate. Verified all-green on **1 October 2026**; one of the pinned certificates is expected to
rotate around **late November 2026**, and when it does, that card will show red from the moment
you open the app — with no proxy, nothing instrumented, and nothing wrong on your side.

**This does not affect the exercise.** The job here is to defeat the check, and a defeated check
accepts whatever certificate it is handed. Solve the card and it goes green exactly as it always
did, and the flag is exactly where it always was. What an expired pin costs you is only the
*clean baseline* — the reassurance of seeing everything green before you begin.

So if a card is red on first launch, do not go hunting for what you broke. Check the date, note
that you have one less diagnostic to lean on, and carry on. That certificates expire out from
under a pin is not a flaw in this app — it is the real, recurring, unglamorous cost of pinning,
and it is the part that never shows up in a tutorial.

## Please don't

Post the pins, the bypass, or working proxy configs in the issues.
