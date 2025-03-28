# Exynos USBDL Documentation

## Protocol

Sadly there isn't actually anything special, just load a file, write the relevant header and just send it off to the device.

## Return statuses

Length of the file sent (in bytes) means a successful send, the device has authenticated this image!

Anything else, unsuccessful send, the image is either invalid, corrupted or did not pass authentication.
