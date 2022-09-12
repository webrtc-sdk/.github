## WebRTC SDKs for Mobile and Desktop

This repo contains a fork of Google's [WebRTC codebase](https://chromium.googlesource.com/external/webrtc/) (referred below as libwebrtc).

This fork is maintained by [LiveKit](https://github.com/livekit) and [Flutter WebRTC](https://github.com/flutter-webrtc/flutter-webrtc).

## Why we forked libwebrtc

libwebrtc has been the de-facto implementation to the WebRTC standard. It's been optimized for use in Chrome and Duo - the main internal applications that use WebRTC.

As we set out to build a [general-purpose framework](https://livekit.io) that can power a wide range of real-time video and audio applications, we found the need to make improvements to libwebrtc, particularly around interactions with video and audio devices.

Our preferred path would have been to submit patches to libwebrtc. However, Google has not always been interested in patches that don't benefit Chrome or Duo. There had been [basic behavioral issues](https://bugs.chromium.org/p/webrtc/issues/detail?id=5873) from 2016 that had been rejected. Because of that, we've decided to maintain our own fork with those improvements, and keeping this fork open source so others could benefit from them too.

This is not a hard-fork. We periodically sync back to WebRTC releases and reapply our patches to HEAD. We don't intent for it to diverge significantly from the main tree.

## Releases

We will publish pre-compiled binary SDKs for [iOS](https://github.com/webrtc-sdk/Specs) and [Android](https://github.com/webrtc-sdk/android). Refer to these repos for installation instructions.

## Changes

For a list of changes, please refer to [webrtc/README](https://github.com/webrtc-sdk/webrtc/blob/m104_release/README.md)
