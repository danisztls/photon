
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
- Store your photos locally so you preserve all your photos safely in your computer or NAS, saving space in the phone without losing your photos original quality or using you mobile data quota.
- Zero privacy concerns. Yours photos will not leave the network unless unless you are explicitly sharing them. Block unknow third parties access to your personal life and intimacy. 
- Automatically organize your photos, save time and easily find what you're looking for.
- Have all your photos with you all the time, find, view and share them with others without fuss via a lightweight offline gallery. 

**Implemented features**
- Import photos from phone with time-based file renaming, deduplication and collision avoidance.
- Export light copies of photos back to phone resulting in huge space saving and fast image loading.

# Install
Install dependencies: ripgrep, exiv2, ImageMagick, trash-cli

Run `setup.sh` to install to `.local/bin/`

Configure source and destination dirs in `move_pics` and run it.

# Development
TODO: AUR script. +later

TODO: Use getopts. +later


## Import
TODO: Import video files.

TODO: Fix metadata during import instead of stripping and reinserting it at export.

## Export
Converting to 1440p and stripping metadata I got from 1,4GB to 697MB. A 51,4% reduction in size with same image quality unless hyper zooming. Converting to webp and 1080p you would get a bigger size reduction while losing a bit of image quality. Just to save space on phone there isn't a need for cloud storage.

TODO: Don't strip exif and fix it on import. +done

TODO: All bugs were fixed. +done

TODO: Reencode videos.

It should not difficult to write an auto-enhance script that will do an average job for at least 2 sigmas of use cases.

TODO: Experiment with enhancement scripts. +later

## Daemon
TODO: Daemon for importing/exporting via inotify.

TODO: Does Syncthing provides a after sync hook?

## Viewing
Pictures can be viewed in any photo gallery but if you are looking for something simple and open-source I recommend [SimpleGallery](https://github.com/SimpleMobileTools/Simple-Gallery).

