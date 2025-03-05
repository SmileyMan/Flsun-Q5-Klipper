# Klipper-Backup 💾 
Klipper backup script for manual or automated GitHub backups 

This backup is provided by [Klipper-Backup](https://github.com/Staubgeborener/klipper-backup).

---
# Firmware Setup - Robin Nano 1.2

make clean

make menuconfig

1. Enable extra low-level configuration options

2. Set the Bootloader offeset as 28 KiB

3. Set the “Micro-controller Architecture” as “STMicroelectronics STM32” - Processor model (STM32F103) 

4. Set the Communication interface as “USART1 PB10/PB9”

6. Enter the last option, enter “!PC6, !PD13”

make

## Create Flash Binary
scripts/update_mks_robin.py ./out/klipper.bin ./out/Robin_nano.bin

---
# Firmware Setup - BTT EBB36 - USB

make clean

make menuconfig

1. Enable extra low-level configuration options

2. Micro-controller Architecture = STMicroelectronics STM32

3. Processor model = STM32G0B1

4. Bootloader offset = No bootloader

5. Clock Reference = 8 MHz crystal

6. Communication interface = USB (on PA11/PA12)

Put board into DFU mode (Hold Boot and press and release Reset)

Find device ID using lsusb (will have DFU indicated)

make flash FLASH_DEVICE=[ID]

---
# Firmware Setup - BTT LIS2DW

make clean

make menuconfig

1. Enable extra low-level configuration options

2. Micro-controller Architecture = PI 2040

3. Bootloader offset = No bootloader

4. Flash chip = W25Q080 with CLKDIV2

5. Communication interface = USB

Put board into DFU mode (Hold boot and reconnect USB)

Find device ID using lsusb (RP2 Boot)

make flash FLASH_DEVICE=[ID]
