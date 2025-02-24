# uvgRTP

uvgRTP is an *Real-Time Transport Protocol (RTP)* library written in C++ with a focus on simple to use and high-efficiency media delivery over the Internet. It features an intuitive and easy-to-use *Application Programming Interface (API)*, built-in support for transporting *Versatile Video Coding (VVC)*, *High Efficiency Video Coding (HEVC)*, *Advanced Video Coding (AVC)* encoded video and Opus encoded audio. uvgRTP also supports *End-to-End Encrypted (E2EE)* media delivery using the combination of *Secure RTP (SRTP)* and ZRTP. According to [our measurements](https://researchportal.tuni.fi/en/publications/open-source-rtp-library-for-high-speed-4k-hevc-video-streaming) uvgRTP is able to reach a goodput of 600 MB/s (4K at 700fps) for HEVC stream when measured in LAN. The CPU usage is relative to the goodput value, and therefore smaller streams have a very small CPU usage.

uvgRTP is licensed under the permissive BSD 2-Clause License. This cross-platform library can be run on both Linux and Windows operating systems. Mac OS is currently not supported, but contributions are welcome to help with this. For SRTP/ZRTP support, uvgRTP uses [Crypto++ library](https://www.cryptopp.com/). 

Currently supported specifications:
   * [RFC 3550: RTP: A Transport Protocol for Real-Time Applications](https://tools.ietf.org/html/rfc3550)
   * [RFC 7798: RTP Payload Format for High Efficiency Video Coding (HEVC)](https://tools.ietf.org/html/rfc7798)
   * [RFC 6184: RTP Payload Format for H.264 Video](https://tools.ietf.org/html/rfc6184)
   * [RFC 7587: RTP Payload Format for the Opus Speech and Audio Codec](https://tools.ietf.org/html/rfc7587)
   * [RFC 3711: The Secure Real-time Transport Protocol (SRTP)](https://tools.ietf.org/html/rfc3711)
   * [RFC 6189: ZRTP: Media Path Key Agreement for Unicast Secure RTP](https://tools.ietf.org/html/rfc6189)
   * [Draft: RTP Payload Format for Versatile Video Coding (VVC)](https://tools.ietf.org/html/draft-ietf-avtcore-rtp-vvc-08)

The original version of uvgRTP is based on Marko Viitanen's [fRTPlib library](https://github.com/fador/fRTPlib).

## Notable features

* Built-in support for:
    * AVC/HEVC/VVC video streaming
    * Opus audio streaming
    * Delivery encryption with SRTP/ZRTP
* Generic interface for custom media types
* UDP hole punching
* Simple to use API
* Permissive license

## Building and linking

See [BUILDING.md](BUILDING.md) for instructions on how to build and use uvgRTP

## Documentation and examples

See [documentation](docs/README.md) and [examples](docs/examples) to get a better understanding of uvgRTP

## Contributing

We warmly welcome any contributions to the project. If you are thinking about submitting a pull request, please read [CONTRIBUTING.md](CONTRIBUTING.md) before proceeding.

## Test framework

We also have an easy to use performance test framework for benchmarking uvgRTP against FFmpeg and Live555 on Linux OS. The framework can be found [here](https://github.com/ultravideo/rtp-benchmarks).

## Papers

If you use uvgRTP in your research, please cite one of the following papers based on your topic. Cite the first one if you are unsure.

[Open-Source RTP Library for High-Speed 4K HEVC Video Streaming](https://researchportal.tuni.fi/en/publications/open-source-rtp-library-for-high-speed-4k-hevc-video-streaming)

```A. Altonen, J. Räsänen, J. Laitinen, M. Viitanen, and J. Vanne, “Open-source RTP library for high-speed 4K HEVC video streaming,” in Proc. IEEE Int. Workshop on Multimedia Signal Processing, Tampere, Finland, Sept. 2020.```

[UVGRTP 2.0: Open-Source RTP Library For Real-Time VVC/HEVC Streaming](https://researchportal.tuni.fi/en/publications/uvgrtp-20-open-source-rtp-library-for-real-time-vvchevc-streaming)

```A. Altonen, J. Räsänen, A. Mercat, and J. Vanne, “uvgRTP 2.0: open-source RTP library for real-time VVC/HEVC streaming,” in Proc. IEEE Int. Conf. Multimedia Expo, Shenzhen, China, July 2021.```

[Open-source RTP Library for End-to-End Encrypted Real-Time Video Streaming Applications](https://researchportal.tuni.fi/en/publications/open-source-rtp-library-for-end-to-end-encrypted-real-time-video-)

```J. Räsänen, A. Altonen, A. Mercat, and J. Vanne, “Open-source RTP library for end-to-end encrypted real-time video streaming applications,” in Proc. IEEE Int. Symp. Multimedia, Naples, Italy, Nov.-Dec. 2021.```
