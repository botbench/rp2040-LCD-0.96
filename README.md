# RP2040-LCD-0.96
RP2040-LCD-0.96 is a low-cost, high-performance Pico-like MCU board with flexible digital interfaces. It incorporates Raspberry Pi's RP2040 microcontroller chip, as same as the one on Raspberry Pi Pico. In addition, there're also an onboard 0.96inch IPS display, Lithium battery recharge/discharge header, and high-efficiency DC-DC buck-boost chip. 

For more information checkout the [product page](https://www.waveshare.com/wiki/RP2040-LCD-0.96)

This project is based on the [RP2040 Project Template](https://github.com/rp-rs/rp2040-project-template).

## How to build
I've replaced the `probe-run` with a standard `gdb` runner, as that worked better with `openocd` and the [picoprobe](https://github.com/rp-rs/rp2040-project-template). A `gdb` commands file is there for convenience. A version of openocd with support for the RP2040 based `picoprobe` is required. 

Before running `cargo run` to build and run the application on the target board, start `openocd-pico -f interface/picoprobe.cfg -f target/rp2040.cfg` in another terminal, to connect to the `picoprobe`.
## License

The contents of this repository are dual-licensed under the _MIT OR Apache 2.0_ License. That means you can chose either the MIT licence or the Apache-2.0 licence when you re-use this code. See `MIT` or `APACHE2.0` for more information on each specific licence.

Any submissions to this project (e.g. as Pull Requests) must be made available under these terms.