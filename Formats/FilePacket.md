# Exynos USBDL Documentation

## File Packets

### Format

This shows the format of a file packet, before it is sent to the device.

| Offset  | Size (Bytes) | Description                                        |
|---------|------:|-----------------------------------------------------------|
| 0x00    | 4     | Address being written to (UINT32, Little Endian)          |
| 0x04    | 4     | Size of the file contents (UINT32, Little Endian)         |
| 0x08    | N     | File contents (Variable Size, Little Endian)              |
| 0x08+N  | 2     | Checksum (UINT16, Little Endian)                          |


For example, sending a file with the hex sequence of ```0xDEADBEEF1337``` to the device at address ```0xF100000000``` will result in
the following hex sequence being sent to the device: ```0x000000F106000000DEADBEEF13378203```
