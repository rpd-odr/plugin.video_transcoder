# Transcode Video Files

Custom fork of the official Unmanic Transcode Video Files plugin.

This fork tracks the upstream plugin while adding optional Dolby Vision RPU preservation when transcoding Dolby Vision video to AV1 with SVT-AV1.

## Custom changes

- Optional **Add Dolby Vision to AV1** setting in Standard mode.
- Detects actual Dolby Vision RPU metadata before adding the FFmpeg dovi_rpu bitstream filter.
- Preserves Dolby Vision RPU metadata when converting compatible sources to AV1.
- Existing smart filters remain unchanged, including black-bar detection/cropping and resolution scaling.
- Sources without Dolby Vision RPU are transcoded normally without dovi_rpu.

## Versioning

Custom releases use the -rpdN suffix:

- 0.1.20-rpd1 — first custom release based on upstream 0.1.20.
- When upstream releases 0.1.21, the next rebased custom release will be 0.1.21-rpd1.

The custom repository is maintained separately from the official Unmanic plugin repository.

## Documentation

- [Description](description.md)
- [Changelog](changelog.md)

## Upstream

- [Official Unmanic plugin](https://github.com/Unmanic/plugin.video_transcoder)
- [Unmanic](https://github.com/Unmanic/Unmanic)
