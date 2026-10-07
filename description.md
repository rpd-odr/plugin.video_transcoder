# Transcode Video Files

This is a custom fork of the Unmanic Transcode Video Files plugin.

The plugin provides the same standard and advanced transcoding functionality as the upstream plugin, with an optional Dolby Vision RPU preservation feature for AV1.

## Dolby Vision to AV1

When Config mode is Standard, Video Codec is AV1, and Add Dolby Vision to AV1 is enabled, the plugin:

1. Probes the source video for Dolby Vision RPU metadata.
2. Adds FFmpeg's dovi_rpu bitstream filter only when RPU metadata is actually present.
3. Leaves sources without Dolby Vision RPU on the normal AV1 transcoding path.

This allows compatible Dolby Vision sources to retain their RPU metadata after AV1 encoding. In tested sources, FFmpeg/MediaInfo reports AV1 Dolby Vision Profile 10 with BL+RPU.

Existing smart filters are preserved, including automatic black-bar detection/cropping and resolution scaling.

## Versioning

This fork uses versions in the form <upstream-version>-rpd<revision>.

For example:

- 0.1.20-rpd1 is based on upstream 0.1.20.
- A later upstream 0.1.21 release will be rebased into a new custom version such as 0.1.21-rpd1.

The custom plugin repository is separate from the official repository. Install and update the custom plugin from the custom repository.

## Support

For issues specific to the custom Dolby Vision functionality, use the custom fork:

- [GitHub repository](https://github.com/rpd-odr/plugin.video_transcoder)

For upstream functionality, consult the original project:

- [Official plugin](https://github.com/Unmanic/plugin.video_transcoder)
- [Unmanic](https://github.com/Unmanic/Unmanic)

## Encoder documentation

- [FFmpeg](https://ffmpeg.org/ffmpeg.html)
- [SVT-AV1](https://gitlab.com/AOMediaCodec/SVT-AV1)
