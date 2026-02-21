## A Curated Directory of Awesome Cologne Chips' GateMate FPGA Links.

[Why GateMate Video](https://www.youtube.com/embed/ZokT2tEiXSA)    [Slides](https://pythonlinks.info/presentations/vectors/WhyGateMate.pdf)

## Documentation

[Documentation]()[GateMate FPGA | Cologne Chip](https://colognechip.com/programmable-logic/gatemate/#tab-313423).  Scroll down and click on the documentation tab.  The data sheet is very well writen.  Installation guide is also there.  If you want to understand LUT trees, make sure to read the primitives library. 

[Architectural Slides](https://colognechip.com/wp-content/uploads/Novel-GateMate-FPGA-Architecture-FPL2021.pdf)  Really these slides should be in the data sheet. [Video](https://underline.io/lecture/34046-novel-architecture-for-european-fpga)

[Serdes Slides 2025](https://colognechip.com/docs/presentations/gatemate-serdes-fpgaconf2025.pdf)

[Radiation Tolerance Slides 2025](https://colognechip.com/docs/presentations/gatemate-radiation-fpgaconf2025.pdf) 

[Seot 2025 Cern Talk](https://indico.cern.ch/event/1587509/contributions/6690211/attachments/3140818/5574499/gatemate-fdf2025.pdf)

[Project Peppercorn - GateMate FPGA Bitstream Documentation](https://github.com/YosysHQ/prjpeppercorn)  Placement flow is a modified [HeAP](https://ieeexplore.ieee.org/document/6339278). [CRoute](https://ieeexplore.ieee.org/document/8735564) does the routing, followed by simulated annealing.   

[LUT-Tree Analsysis](https://github.com/chili-chips-ba/openCologne/tree/main/8.StressTest#lut-tree-logic) An excellent explanation of the LUT trees. 

[Playground for various GateMate FPGA SerDes loopback tests](https://github.com/pu-cc/gm_serdes_lb)

[Interface Guide for Peripheral Devices with 3.3 V Signaling](https://www.colognechip.com/docs/ug1003-gatemate1-level-shifting-latest.pdf)

[LUTRAM_Stress_Test capacities](https://github.com/tarik-ibrahimovic/LUTRAM_Stress_Test)

[Phased Locked Loop (PLL) Implementation](https://colognechip.com/wp-content/uploads/c3-pll-white-paper.pdf) 

[ToolChain(https://colognechip.com/programmable-logic/gatemate/#tab-313424)

## Boards

[Olimex GateMateA1-EVB1](https://www.olimex.com/Products/FPGA/GateMate/GateMateA1-EVB/) This 50€ board is the popular choice for starting with the GateMate. You can buy a case from Olimex, or [print your own](https://www.printables.com/model/1591329-olimex-gatematea1-evb-case) You will probably want to use at lease one of these [extension boards](https://github.com/intergalaktik/Extension_Boards_for_Olimex_GateMate). Here is the list of [UEXT Extension boards](https://www.olimex.com/Products/Modules/UEXT/). At [the bottom of this page]([pico-ice: Using Pmods](https://pico-ice.tinyvision.ai/md_pmods.html)) is a list of lists of pMods. 

[Cologne Chip's GateMate FPGA Evaluation Board](https://www.colognechip.com/programmable-logic/gatemate-evaluation-board/)  This is the board made by Cologne Chips. [\$398 at Digikey](https://www.digikey.com.au/en/products/detail/cologne-chip/CCGM1A1-E1/16087880)

[Prototyping board for the GateMate Evaluation Board](https://github.com/fm4dd/gm-proto-e1)

[GMM-7550](https://www.gmm7550.dev/doc/hardware.html)  [2024 Feb FOSDEM Talk](https://archive.fosdem.org/2024/schedule/event/fosdem-2024-2107-cologne-chip-gatemate-fpga-filling-a-gap-between-hardware-and-software-with-a-presentation-of-the-gmm-7550-module-/) Includes a Raspberry Pi hat, an I/O Breakout board, a USB3.0 interface and a  memory module which provides [512Kx8 static RAM]([CY7C1049GN30-10ZSXI - Infineon Technologies](https://www.infineon.com/cms/en/product/memories/sram-static-ram/asynchronous-sram/cy7c1049gn30-10zsxi/)) with 10 ns access time and 16 MiB QSPI NOR FLASH (S25LP128-JBLE).
[Trenz Electonics # FPGA module](https://shop.trenz-electronic.de/de/TEG2000-01-P001-FPGA-Modul-mit-GateMate-A1-von-Cologne-Chip-16-MByte-QSPI-Flash-4-x-5-cm#)     16 MByte QSPI Flash, 4 x 5 cm]. 82.11 € (69.00 € net).     

[Sipeed Tang PMOD DVI](https://wiki.sipeed.com/hardware/en/tang/tang-PMOD/FPGA_PMOD.html)) (Scroll down to 5.1) is a module for HDMI output/input, which requires the use of LVDS differential pairs.  It works with the GateMate ColorBar DVI demo on the Cologne Chips eval circuit board.  The only change needed is to replace [this line](https://github.com/trabucayre/GateMate_demos/blob/main/colorBarDVI/colorBarDVI.v#L21 ) with ``A({~TMDS_0_clk, ~TMDS_0_data}),```. Does not work with the Olimex board, it seems to have an issue with the level shifters.  Thanks @gwenhaelgoavec.

[ULX5M](https://www.chili-chips.xyz/open-cologne/) is in development.  It will be in the popular Raspberry Pi Compute Module 4 (CM4) form-factor, so it can attach to lots of different base boards. 

[LED Matrix](https://github.com/Martoni/Martoni_Pcb_collection/tree/main/glm5va) A little PCB to adapt 2.5v GateMate signals to 5V for matrix Led.

## Pricing

One user told me that the 21€ Gatemate A1 board compares very roughly, to Lattice ECP5-5G LFE5UM5G-45 [53€-83€ at digikey,com](https://www.digikey.ie/en/products/filter/fpgas-field-programmable-gate-array/696?s=N4IgTCBcDaIDIDECiBWAqgWRQcQLQBYUEQBdAXyA), or AMD's Spartan 6 (XC6SLX45T, In Europe Lattice and AMD also face import duties, and a greater risk of supply chain disruptions, particularly if the chips are made in Taiwan.

## FirmWare

[JTag Programmer](https://github.com/phdussud/pico-dirtyJtag) Also supports Uart. 

[GGMM-7550/gmm7550-control-rp2040](https://github.com/GMM-7550/gmm7550-control-rp2040) Circuit Python control of the GateMate FPGA for the gmm7550 board. 

## GateWare

[Space Inavders on an Intel 8080.  Article](https://olimex.wordpress.com/2025/01/08/space-inavders-retrogame-runs-on-gatematea1-evb/)   [GitLab](https://gitlab.com/x653/spaceinvaders-fpga)

[Open Cologne](https://www.chili-chips.xyz/open-cologne)  is a project to expand the GateMate ecosystem,  funded by the EU.  [Github](https://github.com/chili-chips-ba/openCologne) 

[Integrated Logic Analyzer](https://www.cnx-software.com/2024/06/11/gatemate-integrated-logic-analyzer-ila-deep-dive/) allows you to capture and analyze all signals of your design as a waveform directly within the FPGA. [Video](https://www.youtube.com/watch?v=TZblFccw4kg&t=23s)   [GitHub](https://github.com/colognechip/gatemate_ila)

[FemtoRV Tutorial](https://github.com/fm4dd/gatemate-riscv)
[Litex VexRisc](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/058-litex-vexriscv)

[Litex FazyRV RISC-V](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/089-litex-fazyrv)  1 2 or 4 or maybe 8 bit RISC-V processor. 

[Litex Serv](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/061-litex-serv) An award winning one bit RISC-V serial processor.

[NEORV32 on GateMate Issues ](https://github.com/stnolting/neorv32/discussions/983) NEORV has a big enphasis on useability and realiability. 

[EduBoss](https://fpga-ignite.github.io/presentations-pdf/presentation16.pdf) written by people very active in the GateMate community. 

[PCIe on GateMate NLnet Project](https://github.com/chili-chips-ba/openCologne-PCIE)

[NLnet; USB 3](https://nlnet.nl/project/GateMate-USB3-PHY/)

## Hardware Testing

The [Project Peppercorn GateMate Test Cases](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main), has a large amount of useful code for testing the hardware.  These gateware tests are good starting points for controlling the hardware. 

[1080p @ 60Hz capable HDMI interface](https://elektronaut.tech/en/fpga/driving-full-hd-video-with-the-cologne-chip-gatemate-fpga/) using a dedicated TMDS interface IC

[OV7670 Camera Controller](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/107-ov7670)

VGA Tests: [color](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/011-vga-color)   [Image](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/041-vga-image), and 16 more, too many to index, just [search the page]((https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main))
[Button Test](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/022-buttons) 

OLED Tests: [color](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/031-oled-color) [sprite](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/032-oled-sprite) [pong-wall](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/033-oled-wall) 
[DVI Colorbar](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/072-dvi-lvds) Verical bars on the screen.
[PS2 port](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/080-ps2) (Keyboard or mouse)
[Serdes](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/084-serdes-loopback)
[ColecoVision Console](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/085-colecovision) 

[St7789 OLED](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/096-oled-st7789)

[Litexx I2C](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/097-litex-with-i2c)
[OPL2 Audio Synthesizer](https://docs.icebreaker-fpga.org/hardware/pmod/dvi/)

[HyperRAM](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/101-litex-hyperram)

[SDCard](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/102-litex-sdcard)
[Ethernet](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/103-litex-eth)

[PSRAM](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/104-psram)
[SPI Flash](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/105-litex-spi-flash)

[DVI Driver](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/099-dvi-12b) for the 12 bit Black Mesa Labs DVI PMOD

[OV7670 Camera](https://github.com/YosysHQ/prjpeppercorn-test-cases/tree/main/107-ov7670)

## Design Tools

[DI-FEntwumS](https://elektronikforschung.de/projekte/di-fentwums) (In German) Open source design and visualization environment for dynamically configurable microchips

## Videos

[Novel Architecture for European FPGA](https://underline.io/lecture/34046-novel-architecture-for-european-fpga) An introduction to the GateMate architecture.  [Slides](https://colognechip.com/wp-content/uploads/Novel-GateMate-FPGA-Architecture-FPL2021.pdf)

## Articles

[Accelerating the Game of Life with the GateMate FPGA: Computing 960 Cells in a Single Clock Cycle](https://www.linkedin.com/pulse/game-life-fpga-40x24-grid-computed-single-clock-cycle-dave-fohrn-ajhxe/) This is a great example of using the GateMate small adders in an innovateive way. 

[Using One and Two Bit Adders](https://forth.pythonlinks.info/using-gatemate-1-and-2-bit-adders) to solve the above game of life calculations. Not as efficient a solution, but easy to understand.

[GateMate FPGA Tool Chain](https://www.adiuvoengineering.com/post/gatemate-fpga-tool-chain)

[Cologne Chips GateMate FPGA Offers a Flexible Architecture](https://www.hackster.io/news/cologne-chip-s-gatemate-fpga-offers-a-flexible-cologne-programmable-element-architecture-2db40691dded)

[Would you buy a $20 GateMate FPGA from Germany’s Cologne Chip?](https://www.eejournal.com/article/would-you-buy-a-20-gatemate-fpga-from-germanys-cologne-chip/)

[Why GateMate?](https://forth.pythonlinks.info/why-i-am-using-the-gatemate-fpga) compares the GateMate to other FPGAs.

## Social Media

[OLIMEX Gatemate Board Discord Channel](https://discord.gg/5ahf3Rc46j)

[Radiona Gatemate Discord Channel]([radiona](https://discord.gg/BSJfFz2H3g)) They are making the Olimex Gagemate add on boards, and [OpenCologne and the ULX5S](https://www.chili-chips.xyz/open-cologne/).

[@olimex@mastodon.social](https://mastodon.social/@olimex) makers of the leading Gatemate board. 

[@PythonLinks@mastodon.social](https://mastodon.social/@PythonLinks) maintains this directory.

I encourage everyone to minimise your useage of corporate social media such as X/Twitter and [join the fediverse](https://JoinMastodon.org).   
