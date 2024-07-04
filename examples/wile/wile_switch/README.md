# Wile Example - 4 Gag Smart Switch 
This is an example for the Rogo Wile SDK based on Esp32 series Micro-controller, this is customization version of the ESP IDF 5.1.1, which comes with Rogo's proprietary Libraries for Wile Functionalities 
## Supported Hardware 
- ESP32C3 
- ESP32S3
- 
### Upload when using Secure Boot

- Build project:\
  `idf.py build`
- Upload bootloader:\
  `esptool.py --chip esp32c3 --before=default_reset --after=no_reset --no-stub write_flash --flash_mode dio --flash_freq 80m --flash_size 4MB 0x0 ./build/bootloader/bootloader.bin`
- Upload partition table:\
  `idf.py partition-table-flash`
- Upload app:\
  `idf.py encrypted-flash monitor`

