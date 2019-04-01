# APG: AV1 Portable Graphics [![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/joedrago/apg?branch=master&svg=true)](https://ci.appveyor.com/project/joedrago/apg/history)


APG is a new image format intended to be a stopgap, lightweight alternative to [AVIF](https://aomediacodec.github.io/av1-avif/) until a
proper/stable/mature/turnkey AVIF library with BMFF and alpha channel support exists. It is a
barebones format, only capable of wrapping a single AV1 encoded image along with an optional ICC
profile.

I chose the name as a nod to Fabrice Bellard's [BPG](https://bellard.org/bpg/) format, which appears
to be a lightweight alternative to HEIF for encoding single images with HEVC. This library is
attempting to the same thing, only with AV1.

I pronounce it *AY-peg*, which rhymes with JPEG.

# Disclaimer

It isn't quite ready for primetime now, so I'd avoid it unless you're just curious about testing
basic AV1 image compression. It currently encodes all images in YUV444 12-bit (with an adjustable
1-100 quality level), and doesn't support alpha. If you're discovering this library right now and a
turnkey, feature complete AVIF library out there exists since I wrote this README, you should
probably use that instead.

# Build Notes

You need CMake and nasm.

---

# License

Released under the Boost Software License (Version 1.0). It depends on AOM's
[AV1](https://aomedia.org/) library, which has its own (similarly permissive) license.
