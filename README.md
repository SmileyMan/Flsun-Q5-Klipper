# Klipper-Backup 💾 
Klipper backup script for manual or automated GitHub backups 

This backup is provided by [Klipper-Backup](https://github.com/Staubgeborener/klipper-backup).

---
# Firmware Setup

make clean

make menuconfig

1. Enable extra low-level configuration options

2. Set the Bootloader offeset as 28 KiB

3. Set the “Micro-controller Architecture” as “STMicroelectronics STM32” - Processor model (STM32F103) 

4. Set the Communication interface as “USART1 PB10/PB9”

6. Enter the last option, enter “!PC6, !PD13”

make

# Create Flash Binary
scripts/update_mks_robin.py ./out/klipper.bin ./out/Robin_nano.bin
