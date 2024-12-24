# 부록 A: 용어집

임베디드 생태계는 다양한 프로토콜, 하드웨어 구성 요소 및 벤더별 고유 용어와 약어들이 혼합되어 있습니다. 이 용어집은 이를 나열하고 더 잘 이해할 수 있도록 돕기 위한 설명을 제공합니다.

### BSP

BSP 는 특정 보드에 맞춰 구성된 고수준 인터페이스를 제공합니다. 보통 [HAL](#hal) crate에 의존합니다.
자세한 설명은 [메모리 맵 레지스터 페이지](../start/registers.md) 에서 확인하거나,
더 넓은 개요를 보려면 [이 비디오](https://youtu.be/vLYit_HHPaY) 를 참조하세요.

### FPU

Floating-point Unit. A 'math processor' running only operations on floating-point numbers.

### HAL

A Hardware Abstraction Layer crate provides a developer friendly interface to a microcontroller's
features and peripherals. It is usually implemented on top of a [Peripheral Access Crate (PAC)](#pac).
It may also implement traits from the [`embedded-hal`](https://crates.io/crates/embedded-hal) crate.
There is a more detailed description on the [memory-mapped registers page](../start/registers.md)
or for a broader overview see [this video](https://youtu.be/vLYit_HHPaY).

### I2C

Sometimes referred to as `I²C` or Inter-IC. It is a protocol meant for hardware communication
within a single integrated circuit. See [here][i2c] for more details

[i2c]: https://en.wikipedia.org/wiki/I2c

### PAC

A Peripheral Access Crate provides access to a microcontroller's peripherals. It is one of
the lower level crates and is usually generated directly from the provided [SVD](#svd), often
using [svd2rust](https://github.com/rust-embedded/svd2rust/). The [Hardware Abstraction Layer](#hal)
would usually depend on this crate.
There is a more detailed description on the [memory-mapped registers page](../start/registers.md)
or for a broader overview see [this video](https://youtu.be/vLYit_HHPaY).

### SPI

Serial Peripheral Interface. See [here][spi] for more information.

[spi]: https://en.wikipedia.org/wiki/Serial_peripheral_interface

### SVD

System View Description is an XML file format used to describe the programmers view of a
microcontroller device. You can read more about it on
[the ARM CMSIS documentation site](https://www.keil.com/pack/doc/CMSIS/SVD/html/index.html).

### UART

Universal asynchronous receiver-transmitter. See [here][uart] for more information.

[uart]: https://en.wikipedia.org/wiki/Universal_asynchronous_receiver-transmitter

### USART

Universal synchronous and asynchronous receiver-transmitter. See [here][usart] for more information.

[usart]: https://en.wikipedia.org/wiki/Universal_synchronous_and_asynchronous_receiver-transmitter
