# Exynos USBDL Documentation

## Packet Checksum Generation

- Sum up all bytes of the file (JUST THE FILE, NOT THE HEADER)
- Mask the resultant sum to 0xFFFF
- Store that masked result in the last 2 bytes of the File Packet Header (doesn't make sense to me either but heywho)
