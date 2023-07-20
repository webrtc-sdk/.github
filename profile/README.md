## WebRTC SDKs for Mobile and Desktop

This repo contains a fork of Google's [WebRTC codebase](https://chromium.googlesource.com/external/webrtc/) (referred below as libwebrtc).

This fork is maintained by [LiveKit](https://github.com/livekit) and [Flutter WebRTC](https://github.com/flutter-webrtc/flutter-webrtc).

## Why we forked libwebrtc

libwebrtc has been the de-facto implementation to the WebRTC standard, having been optimized for use in Chrome and Meet, the primary internal applications leveraging WebRTC.

As we set out to build a [general-purpose framework](https://livekit.io) that can power a wide range of real-time video and audio applications, we found the need to make improvements to libwebrtc, particularly when it's used as an SDK inside other applications. Some of the changes we've made include:

- [Simulcast support](https://github.com/webrtc-sdk/webrtc/commit/ee030264e2274a2c90548a99b448782049e48fb4)
- [Audio device handling](https://github.com/webrtc-sdk/webrtc/commit/272127d457ab48e36241e82549870405864851f6)
- [Screen capture for desktop](https://github.com/webrtc-sdk/webrtc/commit/8e832d1163644ab504412c9b8f3ba8510d9890d6)
- [End to end encryption](https://github.com/webrtc-sdk/webrtc/commit/3a2c008529a15fecde5f979a6ebb75c05463d45e)

Some of these patches make sense to be contributed back to Chromium, especially those relating to standards-compliant behavior. In such instances, LiveKit actively merges these changes back upstream.

However, it's considerably more challenging to contribute changes that aren't covered by standards. It's commonplace to see issues and PRs stagnate for years without resolution because reaching a consensus on the correct behavior is difficult. It's also understandable that Google would prioritize their engineering efforts on issues that directly benefit their product lines.

Because of these reasons, we've opted to maintain our own fork with those improvements. We are keeping this fork open-source so that others can also benefit from it.

This is not a hard fork. We periodically synchronize with WebRTC releases and reapply our patches to HEAD. We don't intent for it to diverge significantly from the main tree.

## Releases

We will publish pre-compiled binary SDKs for [iOS](https://github.com/webrtc-sdk/Specs) and [Android](https://github.com/webrtc-sdk/android). Refer to these repos for installation instructions.
