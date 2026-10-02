# The Guard Suite

Three Android crackmes, one discipline each.

| App | Demands |
|---|---|
| **CipherGuard** | static analysis |
| **HookGuard** | dynamic analysis |
| **NetGuard** | public key pinning |

Built for a talk — *From UnCrackable to Uncrackable*, masCon 2026, Berlin, 8 October — and
they exist because the OWASP UnCrackable series has no target for pinning, and nothing that
forces you to instrument a native guard on its own terms.

---

## Read this before you start

**If you point an AI coding agent at these apps, you will have the flags quickly and you will
have learned nothing.** That is not a guess — it was measured on these exact artefacts, by
several independent agents given nothing but the stripped binaries and no documentation. The
fastest had a flag inside two hours.

So the flags are cheap. **The apps are not**, and the flag was never the point. The point is
the route you take to it, and the route is the part an agent skips on your behalf.

Use an agent afterwards — to check your working, or to read a page of AArch64 you are stuck on.
Not instead.

**Obfuscation buys time, not secrecy.** That is one of the things these apps are here to teach,
and you will be able to say exactly how much time once you are through them.

---

## Install

```bash
adb install cipherguard/cipherguard.apk
adb install hookguard/hookguard.apk
adb install netguard/netguard.apk
```

**HookGuard needs a real arm64 device** — it ships `arm64-v8a` only, so an x86 emulator image
will not run it. CipherGuard and NetGuard carry `arm64-v8a` and `x86_64`.

Verify what you downloaded:

```bash
sha256sum -c SHA256SUMS
```

## Rules of engagement

- **No solutions are published here**, and no walkthroughs. That is deliberate.
- Debug-signed crackmes. Install on a test device, not on a phone you care about.
- No network traffic except NetGuard, which talks to public endpoints over TLS.
- Nothing is malicious; nothing persists outside the app sandbox.

## Reporting

A crash, a flag that cannot be reached, or an unintended shortcut that trivialises an app — open
an issue. **Please do not post flags, hints or solutions in issues.** Others are still working.
