# tensor-usbdl

## History
Steps so far for Google Pixel Tablet (Tangorpro)

- Tangorpro (Pixel Tablet) in Pixel Recovery Mode

- ```lsusb``` shows: 

```Bus 001 Device 001: ID 18d1:4f00 Google Inc. Pixel ROM Recovery  Serial: 098ecd98ea08```

## Files needed for flashing
- Download [Tangorpro firmware](https://dl.google.com/dl/android/aosp/tangorpro-bp1a.250405.007-factory-834a2dad.zip)
- extract zip file

- ```mkdir sources```
- ```cp tangorpro-bp1a.250405.007/bootloader-tangorpro-tangorpro-15.2-13237001.img sources/bootloader.img```
- ```/Applications/imjtool/imjtool sources/bootloader.img extract```
- ```mv extracted/* sources/ && rmdir extracted```
- rename all files according to ```main.go``` (append .img and replace / with _)


## Help Menu
- ```go run ./cmd/tensor-usbdl -h``` for help menu

## Execute
- ```go run ./cmd/tensor-usbdl```

This runs for a very, very long time:

```
[Sat, May 10, 2025 - 11:16:42.698 AM CEST]  INFO Tensor-USBDL: Scanning for device...
[Sat, May 10, 2025 - 11:16:42.711 AM CEST]  INFO Tensor-USBDL: Connected to device!
[Sat, May 10, 2025 - 11:16:42.711 AM CEST] TRACE Tensor-USBDL: - Port:   /dev/cu.usbmodemXXXXX
[Sat, May 10, 2025 - 11:16:42.711 AM CEST] TRACE Tensor-USBDL: - ID:     18D1:4F00
[Sat, May 10, 2025 - 11:16:42.711 AM CEST] TRACE Tensor-USBDL: - Serial: XXXXX
[Sat, May 10, 2025 - 11:16:42.711 AM CEST] TRACE Tensor-USBDL: - USB:    true
[Sat, May 10, 2025 - 11:16:42.711 AM CEST] DEBUG Tensor-USBDL: Device identified as XXXXX
[Sat, May 10, 2025 - 11:16:42.711 AM CEST]  INFO Tensor-USBDL: Requested DPM
[Sat, May 10, 2025 - 11:16:42.714 AM CEST] DEBUG Tensor-USBDL: Wrote 4096 bytes
[Sat, May 10, 2025 - 11:16:42.714 AM CEST]  INFO Tensor-USBDL: Successfully wrote DPM
[Sat, May 10, 2025 - 11:16:42.716 AM CEST] TRACE Tensor-USBDL: Received control: C
[Sat, May 10, 2025 - 11:16:42.716 AM CEST]  INFO Tensor-USBDL: Requested DPM
[Sat, May 10, 2025 - 11:16:42.719 AM CEST] DEBUG Tensor-USBDL: Wrote 4096 bytes
[Sat, May 10, 2025 - 11:16:42.719 AM CEST]  INFO Tensor-USBDL: Successfully wrote DPM
[Sat, May 10, 2025 - 11:16:42.720 AM CEST] TRACE Tensor-USBDL: Received control: C
[Sat, May 10, 2025 - 11:16:42.720 AM CEST]  INFO Tensor-USBDL: Requested DPM
[Sat, May 10, 2025 - 11:16:42.723 AM CEST] DEBUG Tensor-USBDL: Wrote 4096 bytes
[Sat, May 10, 2025 - 11:16:42.723 AM CEST]  INFO Tensor-USBDL: Successfully wrote DPM
```

