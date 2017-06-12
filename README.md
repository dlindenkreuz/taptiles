# Taptiles

> Gestural control for musical parameters for trackpads with vibrotactile feedback

Developed at the [IMWI Institute for Musicology and Music Informatics, University of Music Karlsruhe](http://imwi.hfm.eu/) under the supervision of [Dr. Paulo Ferreira-Lopes](http://ima.zkm.de/~pfl/).

## Requirements

- macOS >= 10.11
- Apple Magic Trackpad 2
- Built-in MacBook Trackpads with Force Touch capabilities work as well

## Disclaimer

This is a prototype version and may or may not work with your setup. No guarantees are made. Use this software at your own risk.

The app is unsigned and macOS might refuse to open it. In this case please follow [these instructions](https://support.apple.com/kb/PH25088?locale=en_US)
to open the app.

## OSC Communication

Taptiles sends updates to other apps via [OSC](https://en.wikipedia.org/wiki/Open_Sound_Control). Currently, all communication is sent to `localhost:57100`.

OSC messages follow this pattern:

```
/taptiles/scene/{n}/value/{type} {value}
```

- `n`: scene index (zero-based)
- `type`: gesture type
  - 0: pinch / zoom
  - 1: rotate
  - 2: force click
- `value`: the sole argument of all messages, a floating-point value ranging from 0 to 1

## Download

[Download .zip](https://github.com/dlindenkreuz/taptiles/releases/latest)

## What about open source?

The current codebase is a complete mess. Taptiles is written in Swift 2 which was recently deprecated and needs upgrading. I might spend some time to clean this up so watch this repo if you are interested in contributing.

In the meanwhile, feel free to use the compiled application (see [Download](#download)) provided under the MIT License.
