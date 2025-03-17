# STM32L431CCT6 QSPI External Loader with W25Q128

## Description

This repository provides an external loader for the STM32L431CCT6 microcontroller interfacing with the Winbond W25Q128 Quad SPI (QSPI) flash memory. It facilitates the creation of `.stldr` files for the W25Q128 and other W25QXX series flash memories.

## Features

- **QSPI External Loader**: Enables programming of external QSPI flash memory using STM32CubeProgrammer.
- **Configurable for Various Flash Sizes**: Supports different W25QXX series chips by adjusting the `MEMORY_FLASH_SIZE` definition in `quadspi.h`.

## Getting Started

### Prerequisites

- **Hardware:** STM32L431CCT6 microcontroller and Winbond W25Q128 (or compatible W25QXX series) QSPI flash memory.
- **Software:** [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html) or another compatible development environment.

### Installation

```sh
git clone https://github.com/alixahedi/STM32L431-W25Q128-QSPI.git
```

### Usage

#### Open the Project

1. Launch STM32CubeIDE.
2. Navigate to `File` > `Open Projects from File System...`.
3. Select the cloned repository folder.

#### Configure Flash Size

Modify `MEMORY_FLASH_SIZE` in `quadspi.h` to match your flash memory size:

```c
#define MEMORY_FLASH_SIZE 0x1000000 // 16MB (128Mbit)
```

#### Build the Project

```sh
# Inside STM32CubeIDE, click 'Build' or use shortcut Ctrl+B
```

#### Generate `.stldr` File

Locate the generated `.stldr` file in the `Debug` or `Release` folder.

#### Flashing with STM32CubeProgrammer

1. Open STM32CubeProgrammer.
2. Select the generated `.stldr` file.
3. Program the external QSPI flash memory.

## Notes

- Ensure correct hardware connections for QSPI communication.
- Refer to the [Winbond W25Q128 Datasheet](https://www.mouser.com/datasheet/2/949/w25q128jv_revf_03272018_plus-1489608.pdf?srsltid=AfmBOoqCO0SuejjTnDtp5m3vgZcyLOtywsdRBBxNlNx1ajRBm__T7O2F)) for specifications.

## Contributing

Contributions are welcome! Fork the repository and submit a pull request.

## License

This project is licensed under the MIT License. See `LICENSE` for details.
