# Photon 

Photon is the elementary particle of light and electromagnetic radiation and also an open-source no-cloud alternative to Google Photos that provides smart archiving of your photos.

<!-- TOC GFM -->

* [Use case](#use-case)
* [Current state](#current-state)
  * [Implemented features](#implemented-features)
* [Setup](#setup)
* [Usage](#usage)

<!-- /TOC -->

## Use case
- Store your photos locally so you preserve all your photos safely in your computer or NAS, saving space in the phone without losing your photos original quality or using you mobile data quota.
- Zero privacy concerns. Yours photos will not leave the network unless unless you are explicitly sharing them. Block unknown third parties access to your personal life and intimacy. 
- Automatically organize your photos, save time and easily find what you're looking for.
- Have all your photos with you all the time, find, view and share them with others without fuss via a lightweight offline gallery. 

## Current state
Currently it is in alpha state.

Check development notes on [DEVELOPMENT.md](https://github.com/lbcnz/photon/blob/main/DEVELOPMENT.md). Contributions such as code and feedback are welcomed.

### Implemented features
- Importing photos from a dir with time-based file renaming, deduplication and collision avoidance.
- Exporting copies of the photos back to the phone, with metadata stripped, resized, and optionally converted, resulting in huge space saving and fast image loading.

Converting to 1440p and stripping metadata I got from 1,4GB to 697MB. A 51,4% reduction in size with same image quality unless hyper zooming. Converting to webp and 1080p I would get a bigger size reduction while losing a bit of image quality. And of course, originals would be preserved on local storage and could be encrypted and them sent to the cloud as backup.

## Setup
Install dependencies: ripgrep, exiv2, ImageMagick, trash-cli

Run `setup` to install photon to `.local/bin/`

Currently there are no syncing and viewing tools integrated and for that purpose I recommend:

- [Syncthing](https://github.com/syncthing/syncthing) as it's a robust and easy to set-up peer-to-peer tool for continuous file syncing through LAN or WAN.
- [SimpleGallery](https://github.com/SimpleMobileTools/Simple-Gallery) as it's open-source and works well as far as I tested.

Although pictures can be viewed in any photo gallery and synced through any file syncing tool that works in your phone.

## Usage
```sh
# import pics 
photon import <srcPath> <dstPath>

# dedup pics
photon dedup <targetPath>

# to convert when exporting (optional)
export optimal_format=webp

# export pics (resize, strip metadata)
photon export <srcPath> <dstPath>

# delete from destination files not found on source
photo clean <srcPath> <dstPath>
```
