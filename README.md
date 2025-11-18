# campsnappro-fun
Camp Snap Pro, aka CS Pro. Fun.

# random notes
  - 0603:8611 Novatek Microelectronics Corp. NTK96550-based camera (mass storage mode)
  - webcam mode (UVC) when no microsd is inserted
    - 0603:8612 Novatek Microelectronics Corp. NTK96550-based camera (webcam mode)
    - 1920x1080 max resolution. appears to be direct 1:1 pixels from the center of the sensor instead of downscaling the whole sensor image
  - shutter lag (time from pressing shutter button to completing taking a photo) seems to be around 150-320ms (best guess)
  - takes ~4 seconds to power up with 436 photos on microsd card
  - when holding down the button, it takes multiple photos at around 1.2 seconds per photo (probably dependent on light/exposure)

# sample exif data
```
  File size       : 3373983 Bytes
  MIME type       : image/jpeg
  Image size      : 4608 x 3456
  Thumbnail       : image/jpeg, 4901 Bytes
  Camera make     : CampSnap
  Camera model    : CSPro-100
  Image timestamp : 2025:11:17 16:49:58
  File number     : 
  Exposure time   : 1/60 s
  Aperture        : F1.8
  Exposure bias   : 0 EV
  Flash           : No, compulsory
  Flash bias      : 
  Focal length    : 3.0 mm
  Subject distance: 
  ISO speed       : 195
  Exposure mode   : Creative program
  Metering mode   : Average
  Macro mode      : 
  Image quality   : 
  White balance   : Auto
  Copyright       : 
  Exif comment    : charset=InvalidCharsetId _ID_1
```
