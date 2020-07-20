
<!-- TOC GitLab -->

- [Install](#install)
- [Development](#development)
    - [Import](#import)
    - [Export](#export)
    - [Daemon](#daemon)
    - [Viewing](#viewing)

<!-- /TOC -->

Photon is the elementary particle of light and electromagnetic radiation and also an open-source no-cloud alternative to Google Photos that provides smart archiving of your photos.

**Use case**
Local network photos storage so you preserve all your photos safely in your computer or NAS, saving space in the phone without losing your photos original quality.

Zero privacy concerns. Yours photos will not leave your network or be shared with unknow third parties unless you are explicitly doing it.

Automatically organized collection so you save time and still can easily find what you're looking for.

Lightweight offline gallery so you can have all your photos with you all the time, find, view and share them with others without any fuss. Works in any device without slowning it down. 

**Implemented features**
- Import photos from phone with time-based file renaming, deduplication and collision avoidance.
- Export light more than adequate to mobile copies of your photos back to your phone that will amount to huge space savings.

# Install
Install dependencies: ripgrep, exiv2, ImageMagick, trash-cli

Run `setup.sh` to install to `.local/bin/`

Configure source and destination dirs in `move_pics` and run it.

# Development
TODO: AUR script. +later

TODO: Fix getopts. +later

It is not difficult to write an auto-enhance GIMP script that will do an average job for at least 2 sigmas of use cases.

## Import
TODO: Import video files.

TODO: Fix metadata during import instead of stripping and reinserting it at export.

## Export
Converting to 1440p and stripping metadata I got from 1,4GB to 697MB. A 51,4% reduction in size with same image quality unless hyper zooming. Converting to webp and 1080p you would get a bigger size reduction while losing a bit of image quality. Just to save space on phone there isn't a need for cloud storage.

TODO: Exif stripping should be optional and not default. +asap

TODO: All bugs were fixed. +done

TODO: Reencode videos.

## Daemon
TODO: Daemon for importing/exporting via inotify.

TODO: Does Syncthing provides a after sync hook?

## Viewing
Pictures can be viewed in any photo gallery but if you are looking for something simple and open-source I recommend [SimpleGallery](https://github.com/SimpleMobileTools/Simple-Gallery).

