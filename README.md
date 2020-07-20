
<!-- TOC GitLab -->

- [HOW-TO](#how-to)
- [Development](#development)
    - [Import](#import)
        - [Performance](#performance)
    - [Export](#export)
    - [Daemon](#daemon)
    - [Viewing](#viewing)

<!-- /TOC -->

Photon is the elementary particle of light and electromagnetic radiation. Photon is a mimimalistic no-cloud alternative to Google Cloud that provides phone-computer sync and smart archiving with open source tools.

Right now it moves images from folder A to B. It does nice things like renaming images in a neatly organized **YY-MM/timestamp.jpg** pattern, mime file type parsing, reading date from exif metadata when that's available, resolve collisions, move non-images to root.

# HOW-TO
Install dependencies: ripgrep, exiv2, ImageMagick, trash-cli

Run `setup.sh` to install to `.local/bin/`

Configure source and destination dirs in `move_pics` and run it.

# Development
TODO: AUR script. +later

TODO: Fix getopts. +later

TODO: Merged, cleaner code. +done

## Import
TODO: Import video files.

### Performance
Parsing performance is good but could be better. In a modern desktop I moved 2GB of photos in less than a minute while also parsing over 1K of non-image files amounting over 1,5GB. Daily processing for non-photographers will be insignificant.

TODO: Parallelize IO writes to mitigate bottlenecks. +later

TODO: Multi-thread script execution. +later

## Export
Converting to 1440p and stripping metadata I got from 1,4GB to 697MB. A 51,4% reduction in size with same image quality unless hyper zooming. Converting to webp and 1080p you would get a bigger size reduction while losing a bit of image quality. Just to save space on phone there isn't a need for cloud storage.

TODO: Reencode videos.

TODO: Set exif date in exported pics. +done

TODO: Fix images upscaling when optimizing.

TODO: Avoid exporting already exported and not newer. +done

TODO: Delete from mirror when the original was deleted. +done

## Daemon
TODO: Daemon for importing/exporting via inotify.

## Viewing
Is there anything great for this? Shotwell is the best Gnome tool that I know. I have my AutoWebGallery project but it's crude. I really just need a web gallery with a minimap scroller and tags searching and that throws anything at me like cat does. Network IO is not a constraint because it's local.

