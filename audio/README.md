# Video music bed (Episode #64 — Never Give Up)

The animated short uses **real** royalty-free disco/funk — not procedural ffmpeg tones.

| Field | Value |
|-------|--------|
| **Track** | Funky Disco Beats to Boogie/Woogie to |
| **Artist** | Fupi |
| **License** | [CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) (public domain) |
| **Source page** | https://opengameart.org/content/funky-disco-beats-to-boogiewoogie-to |
| **File in repo** | `disco-bed-source.flac` |

Pixabay tracks (e.g. [Disco Funk Revival](https://pixabay.com/music/upbeat-disco-funk-revival-instrumental-01-359835/)) are also allowed under the [Pixabay Content License](https://pixabay.com/service/license/) if you swap the source file.

## Re-mix with another track

From the repo root:

```bash
npm run mix:music -- public/videos/SW64_never-give-up_animated.mp4
```

Custom MP3/FLAC and start offset (seconds into the source):

```bash
node scripts/mix-video-music.mjs public/videos/SW64_never-give-up_animated.mp4 --bed path/to/track.mp3 --start 45
```

Prepare a WAV bed only (trim/loop + rising volume):

```bash
node scripts/prepare-disco-bed.mjs 28 /tmp/bed.wav public/audio/disco-bed-source.flac --start 0
```

The mix script strips existing MP4 audio and muxes the new bed with **video stream copy** (`-c:v copy`).
