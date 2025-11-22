# campsnappro-fun
Camp Snap Pro, aka CS Pro. Fun.

## random notes
- 0603:8611 Novatek Microelectronics Corp. NTK96550-based camera (mass storage mode)
- webcam mode (UVC) when no microsd is inserted
  - 0603:8612 Novatek Microelectronics Corp. NTK96550-based camera (webcam mode)
  - 1920x1080 max resolution. appears to be direct 1:1 pixels from the center of the sensor instead of downscaling the whole sensor image
- shutter lag (time from pressing shutter button to completing taking a photo) seems to be around 150-320ms (best guess)
- takes ~4 seconds to power up with 436 photos on microsd card
- when holding down the shutter button, it takes multiple photos at around 1.2 seconds per photo (probably dependent on light/exposure)
- when powering up while holding the shutter button, it will start taking photos right after it finishes booting
- custom filter files named `std.flt` `vtg1.flt` `vtg2.flt` `bw.flt`
  - format:
    ```
    lum:-22
    contrast:3
    rgain:-38
    ggain:-18
    bgain:-16
    hue:8
    sat:-15
    ```
  - the order of the values matter
  - labels to the left of the colon do not matter
- auto poweroff is at 10 minutes
  - camera can only be revived by turning the switch to the OFF position first, plugging in a USB cable, or poking the reset button
  - changing filter/flash mode will reset timer
- reset button does not seem to reset the date/time
- the battery gauge consisting of 4 leds is very non-linear
  - the last led (technically the first one) is like a low battery indicator. if it's down to the last dot, don't be surprised if the camera does not turn back on when powered off (4 beeps).
  - that last led will blink (and there will be beeps? i forgot) when battery is extremely low. expect it to turn off shortly after.
- battery is 1200mAh
- charges at ~570mA when turned off
  - uses an additional ~80mA while in usb storage mode
  - uses an additional ~240mA while in photo mode
  - uses 300-310mA while in photo mode after fully charged, drops to ~70mA for a few seconds after turning off
- can turn on and take photos while charging if connected to a power-only source (or using a power-only cable)
  - may still end up in usb storage mode if using a regular usb-c data cable with a power-only source...

## sample exif data
```
Exif.Image.ImageDescription                  Ascii       7  CAMERA
Exif.Image.Make                              Ascii       9  CampSnap
Exif.Image.Model                             Ascii      10  CSPro-100
Exif.Image.Orientation                       Short       1  top, left
Exif.Image.XResolution                       Rational    1  72
Exif.Image.YResolution                       Rational    1  72
Exif.Image.ResolutionUnit                    Short       1  inch
Exif.Image.Software                          Ascii       8  V1.1.7A
Exif.Image.DateTime                          Ascii      20  2025:11:17 16:49:58
Exif.Image.YCbCrPositioning                  Short       1  Co-sited
Exif.Image.ExifTag                           Long        1  218
Exif.Photo.ExposureTime                      Rational    1  1/60 s
Exif.Photo.FNumber                           Rational    1  F1.8
Exif.Photo.ExposureProgram                   Short       1  Creative program
Exif.Photo.ISOSpeedRatings                   Short       1  195
Exif.Photo.ExifVersion                       Undefined   4  2.20
Exif.Photo.DateTimeOriginal                  Ascii      20  2025:11:17 16:49:58
Exif.Photo.DateTimeDigitized                 Ascii      20  2025:11:17 16:49:58
Exif.Photo.ComponentsConfiguration           Undefined   4  YCbCr
Exif.Photo.ShutterSpeedValue                 SRational   1  1/60 s
Exif.Photo.ApertureValue                     Rational    1  F1.7
Exif.Photo.BrightnessValue                   SRational   1  1
Exif.Photo.ExposureBiasValue                 SRational   1  0 EV
Exif.Photo.MaxApertureValue                  Rational    1  F1.7
Exif.Photo.MeteringMode                      Short       1  Average
Exif.Photo.LightSource                       Short       1  Unknown
Exif.Photo.Flash                             Short       1  No, compulsory
Exif.Photo.FocalLength                       Rational    1  3.0 mm
Exif.Photo.MakerNote                         Undefined  16  0 48 53 54 0 0 165 165 124 64 51 0 35 59 0 0
Exif.Photo.UserComment                       Undefined  20  charset=InvalidCharsetId _ID_1
Exif.Photo.FlashpixVersion                   Undefined   4  1.00
Exif.Photo.ColorSpace                        Short       1  sRGB
Exif.Photo.PixelXDimension                   Short       1  4608
Exif.Photo.PixelYDimension                   Short       1  3456
Exif.Photo.InteroperabilityTag               Long        1  768
Exif.Iop.InteroperabilityIndex               Ascii       4  R98
Exif.Iop.InteroperabilityVersion             Undefined   4  1.00
Exif.Photo.SensingMethod                     Short       1  One-chip color area
Exif.Photo.FileSource                        Undefined   1  Digital still camera
Exif.Photo.SceneType                         Undefined   1  Directly photographed
Exif.Photo.CustomRendered                    Short       1  Normal process
Exif.Photo.ExposureMode                      Short       1  Manual
Exif.Photo.WhiteBalance                      Short       1  Auto
Exif.Photo.DigitalZoomRatio                  Rational    1  0.0
Exif.Photo.SceneCaptureType                  Short       1  Standard
Exif.Photo.Sharpness                         Short       1  Normal
Exif.Thumbnail.Compression                   Short       1  JPEG (old-style)
Exif.Thumbnail.XResolution                   Rational    1  72
Exif.Thumbnail.YResolution                   Rational    1  72
Exif.Thumbnail.ResolutionUnit                Short       1  inch
Exif.Thumbnail.JPEGInterchangeFormat         Long        1  892
Exif.Thumbnail.JPEGInterchangeFormatLength   Long        1  4901
```
