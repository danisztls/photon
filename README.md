Photon is the elementary particle of light and electromagnetic radiation. Photon is a mimimalistics no-cloud alternative to Google Cloud that provides phone-computer sync and archiving with open-source tools.

Right now it's just a script that moves images from folder A to B. It does nice things like renaming images in a pattern of **YY-MM/timestamp.jpg**, mime file type parsing, reading date from exif metadata when available and collision resolution.

# HOW-TO
Create source and destination dirs, configure them in script and execute it.

Source is where you intend to drop new pictures and destination is where you want to have your pictures saved in neatly organized by time.

## Performance
Performance is good but could be better. In a modern desktop I moved 2GB of photos in less than a minute while also parsing over 1K of non-image files amounting over 1,5GB.

TODO: Parallelize IO writes to mitigate bottlenecks. +later

TODO: Multi-thread script execution. +later

## Syncing

TODO: Setup Syncthing syncing

## Gallery
I'm using Shotwell right now to manage my gallery but you can use your favorite photo manager.

