
<!-- TOC GitLab -->

- [Install](#install)

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

**Syncing**

I recommend [Syncthing](https://github.com/syncthing/syncthing). It is a robust and easy to set-up peer-to-peer tool for continuous file syncing throught LAN or WAN.

**Viewing**

Pictures can be viewed in any photo gallery but if you are looking for something simple and open-source I recommend [SimpleGallery](https://github.com/SimpleMobileTools/Simple-Gallery).

# Install
Install dependencies: ripgrep, exiv2, ImageMagick, trash-cli

Run `setup` to install photon to `.local/bin/`

