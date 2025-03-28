# GBA Flash Patcher

Patches an EEPROM or SRAM GBA game to save on Flash 512K. 

More info to come, espect things to change a lot too.

Compiling:

```# arm-none-eabi-gcc -c payload.c -o payload.o
# arm-none-eabi-ld -T payload.ld payload.o -o payload.elf
# arm-none-eabi-objcopy -O binary payload.elf payload.bin
# xxd -i payload.bin > payload_bin.h
# gcc patcher.c -o patcher

# ./patcher your_rom.gba
