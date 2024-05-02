# Anim Mouse's ABC sheet music
This is a collection of sheet music written in ABC notation.

## Rendering to video

### Video
[Zenith](https://github.com/arduano/Zenith-MIDI)

FFmpeg options: `-c:v libsvtav1 -preset 8 -crf 34 -pix_fmt yuv420p10le -svtav1-params "tune=0:keyint=10s"`

### Audio
[abctools](https://abcplus.sourceforge.net/index.it.html)

`abc2midi <abc file> -o <filename>`

[Keppy's MIDI Converter](https://github.com/KeppySoftware/KMC)

[ffmpeg-normalize](https://github.com/slhck/ffmpeg-normalize)

`ffmpeg-normalize <filename>.flac -o <filename>_normalized.flac -c:a flac`

### Mux

`ffmpeg -i video_only.mkv" -itsoffset 2.333 -i "audio.flac" -to <end time> -c:v copy -c:a copy <filename>.mkv`