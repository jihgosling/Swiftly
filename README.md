# Swiftly 

developed by a broke ahh student who hates the terrible Image Edging app

A photo browser for iPhone and iPad that fixes the weak iOS file manager for reviewing photos from a camera's SD card, and works wirelessly with Sony cameras (developed and tested on the **Sony a6100 / ILCE-6100**).

> Swiftly is an independent project. It is not affiliated with, endorsed by, or sponsored by Sony. "Sony" and "a6100" are trademarks of their owners and are used only to say which camera it works with.

## Features

**SD card / folder**
- Pick the card's folder and browse a thumbnail grid.
- Sort and filter by date, name, and RAW or JPEG.
- Hold-and-slide multi-select, pinch-zoom viewer, EXIF info.
- Opens real Sony `.ARW` RAW files.
- Save to Photos (original format kept), Export to Files, and Delete (single or multiple).

**Over Wi-Fi (Send to Smartphone > Select on Smartphone)**
- Browse the camera's photos and save them to your device.
- JPEGs download at full size.

**Wireless control (Ctrl w/ Smartphone) [Experimental]**
- Live view, plus aperture, shutter speed, ISO, white balance, and exposure compensation, depending on the camera's exposure mode.
- The shutter button takes about 2 photos per press in Continuous Lo, because the camera's remote API has no single-shot call for this model.

## Limits you should know about

- **RAW over Wi-Fi is not possible.** The camera only shares small JPEG previews of RAW photos. Use the SD card or USB for real `.ARW` files.
- **Deleting over Wi-Fi is not possible.** The camera refuses it. Swiftly can delete photos only from an opened SD card folder, and deleting is permanent.
- After deleting on the card, the camera may show "Unable to show the photo". Run **Recover Image DB** in the camera's Setup menu, or delete the blank entries on the camera.
- Only one device can be connected to the camera at a time.

## Testing (so far)

As i only own a a6100, all the testings for this app has been done and worked with a6100. Though reading all the logs from the previous test build, it should work with models that supports the edging app (2019 Sony Alpha lineups). Feedbacks are most appreciates!

## Requirements

- iOS / iPadOS 17 or later.
- Allow **Local Network** access when asked (needed for Wi-Fi mode).

## Install (sideloading)

Download `Swiftly.ipa` from the Releases page and install it with a sideloading tool such as AltStore/Sidestore or Sideloadly. Builds signed with a free Apple ID expire after 7 days and must be refreshed.
!!Edit!!
As of testing, this build isnt working properly when sideloaded via Esign/Ksign using private cert.


## Build from source

Built with [xtool](https://github.com/xtool-org/xtool) (SwiftPM, no Xcode needed), on Linux:

```
xtool dev build --ipa -c release
```

The `.ipa` is written to `xtool/`.

## Author

Created and maintained by ajihgosling (my insta handle lol if anything can find me there). Designed, directed, and tested build by build on a real camera by the author, with AI assistance (cs I dont know Swift lol) for writing the Swift code.
