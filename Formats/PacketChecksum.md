# Exynos USBDL Documentation

## Packet Checksum Generation

This process is done *AFTER* writing the file header. The checksum generation process consists of

- Going to the end of the data
- Moving back 2 bytes (I assume to account for the space for the checksum)
- Iterating over the data for (data_len - 10) times, 8 bytes at a time, in reverse.
- Sum all bytes
- After iteration, mask the sum of the bytes to 16 bits ```sum & 0xFFFF```
- The checksum is then stored in the last 2 bytes of available data
