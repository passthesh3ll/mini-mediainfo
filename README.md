# mini-mediainfo

![image](https://i.postimg.cc/nc5r17Tn/2.png)

A basic mediainfo wrapper with minimalistic output. A simple tool for DataHoarders, Muxers and Encoders, based on [pymediainfo](https://pymediainfo.readthedocs.io/en/stable/pymediainfo.html) wrapper.

## Dependences

- mediainfo
- pymediainfo
- colorama

## Usage

A file:

```sh
mi <file.mkv/mp4/avi..>
```

All files in a folder:

```sh
mi .
```

Save output:

```sh
mi . -nc >> output.txt
```

![screen](https://i.postimg.cc/VkCQPbws/1.png)

## Help

```
usage: mi.py [-h] [-r] [-fn FILTER_NAME] [-fr {SD,HD,FHD,UHD}] [-fe] [-fm]
             [-fa {TrueHD,TrueHD-Atmos,DD,DDP,DDP-Atmos,DD-Atmos,DTS,DTS-ES,DTS-HD,DTS-MA,AAC}]
             [-fs {vob,srt,sup,ass,vtt}] [-fc] [-fnc] [-fnal <language_iso639>]
             [-fnsl <language_iso639>] [-nc] [-pfn] [-pn] [-v]
             path

print mediainfo output in a compact way

positional arguments:
  path                  the folder or file path

options:
  -h, --help            show this help message and exit
  -r, --recursive       parse all foders recursively without depth limit
  -fn, --filter_name FILTER_NAME
                        show only files with specific name
  -fr, --filter_resolution {SD,HD,FHD,UHD}
                        show only files with specific resolution
  -fe, --filter_errors  show only files with errors in tags
  -fm, --filter_missing_info
                        show only files with missing tags "?" or "-empty-"
  -fa, --filter_audio {TrueHD,TrueHD-Atmos,DD,DDP,DDP-Atmos,DD-Atmos,DTS,DTS-ES,DTS-HD,DTS-MA,AAC}
                        show only files with specific audio
  -fs, --filter_subs {vob,srt,sup,ass,vtt}
                        show only files with specific subs
  -fc, --filter_chapters
                        show only files with chapters
  -fnc, --filter_not_chapters
                        show only files without chapters
  -fnal, --filter_not_audio_language <language_iso639>
                        show only files without specific audio language
  -fnsl, --filter_not_subtitle_language <language_iso639>
                        show only files without specific subtitle language
  -nc, --no_colors      show output without colors
  -pfn, --printfullnames
                        print only full filenames
  -pn, --printnames     print only filenames
  -v, --verbose         fallback to vanilla mediainfo output

```
