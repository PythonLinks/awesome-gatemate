# 

## A Curated Directory of Awesome Cologne Chips' GateMate FPGA Links.

[Why I am using the Colgne Chip's GateMate FPGA](https://forth.pythonlinks.info/why-i-am-using-the-gatemate-fpga) compares the GateMate to other FPGAs. 

## Documentation

[Documentation]()[GateMate FPGA | Cologne Chip](https://colognechip.com/programmable-logic/gatemate/#tab-313423).  Scroll down and click on the documentation tab.  The data sheet is very well writen.  Installation guide is also there.  If you want to understand LUT trees, make sure to read the primitives library. 

[Project Peppercorn - GateMate FPGA Bitstream Documentation](https://github.com/YosysHQ/prjpeppercorn)

[Architectural Slides](https://colognechip.com/wp-content/uploads/Novel-GateMate-FPGA-Architecture-FPL2021.pdf)  Really these slides should be in the data sheet. 

## Boards

[Olimex GateMateA1-EVB1](https://www.olimex.com/Products/FPGA/GateMate/GateMateA1-EVB/) This 50€ board is the popular choice for starting with the GateMate.  You will probably want to use at lease one of these [extebsuib boards](https://github.com/intergalaktik/Extension_Boards_for_Olimex_GateMate). Here is the list of [UEXT Extension boards](https://www.olimex.com/Products/Modules/UEXT/). At [the bottom of this page]([pico-ice: Using Pmods](https://pico-ice.tinyvision.ai/md_pmods.html)) is a list of lists of pMods. 

[Cologne Chip's GateMate FPGA Evaluation Board](https://www.colognechip.com/programmable-logic/gatemate-evaluation-board/)  This is the board made by Cologne Chips. [\$398 at Digikey](https://www.digikey.com.au/en/products/detail/cologne-chip/CCGM1A1-E1/16087880)

[Prototyping board for the GateMate Evaluation Board](https://github.com/fm4dd/gm-proto-e1)

[GMM-7550](https://github.com/GMM-7550/gmm7550-hardware)  [2024 Feb FOSDEM Talk](https://archive.fosdem.org/2024/schedule/event/fosdem-2024-2107-cologne-chip-gatemate-fpga-filling-a-gap-between-hardware-and-software-with-a-presentation-of-the-gmm-7550-module-/) Includes a Raspberry Pi hat and a  memory module which provides 512Kx8 static RAM (CY7C1049GN30-10ZSXI) with 10 ns access time and 16 MiB QSPI NOR FLASH (S25LP128-JBLE).
[Trenz Electonics # FPGA module](https://shop.trenz-electronic.de/de/TEG2000-01-P001-FPGA-Modul-mit-GateMate-A1-von-Cologne-Chip-16-MByte-QSPI-Flash-4-x-5-cm#)     16 MByte QSPI Flash, 4 x 5 cm]. 82.11 € (69.00 € net)

## Pricing

One user told me that the 21€ Gatemate A1 board compares very roughly, to Lattice ECP5-5G LFE5UM5G-45 [53€-83€ at digikey,com](https://www.digikey.ie/en/products/filter/fpgas-field-programmable-gate-array/696?s=N4IgTCBcDaIDIDECiBWAqgWRQcQLQBYUEQBdAXyA), or AMD's Spartan 6 (XC6SLX45T, In Europe Lattice and AMD also face import duties, and a greater risk of supply chain disruptions, particularly if the chips are made in Taiwan.

## FirmWare

[JTag Programmer](https://github.com/phdussud/pico-dirtyJtag) Also supports Uart. 

[GGMM-7550/gmm7550-control-rp2040](https://github.com/GMM-7550/gmm7550-control-rp2040) Circuit Python control of the GateMate FPGA for the gmm7550 board. 

## GateWare

[Open Cologne](https://www.chili-chips.xyz/open-cologne)  is a project to expand the GateMate ecosystem,  funded by the EU.  [Github](https://github.com/chili-chips-ba/openCologne) 

[GateMate Integrated Logic Analyzer (ILA) deep dive - CNX Software](https://www.cnx-software.com/2024/06/11/gatemate-integrated-logic-analyzer-ila-deep-dive/)

[FemtoRV Tutorial](https://github.com/fm4dd/gatemate-riscv)

[NEORV32 on GateMate Issues ](https://github.com/stnolting/neorv32/discussions/983) NEORV has a big enphasis on useability and realiability. 

[litex](https://github.com/enjoy-digital/litex) now supports both the Olimex and Cologne Chips boards. 

## Design Tools

[DI-FEntwumS](https://elektronikforschung.de/projekte/di-fentwums) (In German) Open source design and visualization environment for dynamically configurable microchips

## Documentation

[Playground for various GateMate FPGA SerDes loopback tests](https://github.com/pu-cc/gm_serdes_lb)

[Interface Guide for Peripheral Devices with 3.3 V Signaling](https://www.colognechip.com/docs/ug1003-gatemate1-level-shifting-latest.pdf)

## Articles

[Accelerating the Game of Life with the GateMate FPGA: Computing 960 Cells in a Single Clock Cycle](https://www.linkedin.com/pulse/game-life-fpga-40x24-grid-computed-single-clock-cycle-dave-fohrn-ajhxe/) This is a great example of using the GateMate small adders in an innovateive way. 

[GateMate FPGA Tool Chain](https://www.adiuvoengineering.com/post/gatemate-fpga-tool-chain)

[Cologne Chips GateMate FPGA Offers a Flexible Architecture](https://www.hackster.io/news/cologne-chip-s-gatemate-fpga-offers-a-flexible-cologne-programmable-element-architecture-2db40691dded)

[Would you buy a $20 GateMate FPGA from Germany’s Cologne Chip?](https://www.eejournal.com/article/would-you-buy-a-20-gatemate-fpga-from-germanys-cologne-chip/)

## Social Media

[OLIMEX Gatemate Board Discord Channel](https://discord.gg/5ahf3Rc46j)

[Radiona Gatemate Discord Channel]([radiona](https://discord.gg/BSJfFz2H3g)) They are making the Olimex Gagemate add on boards, and [OpenCologne and the ULX5S](https://www.chili-chips.xyz/open-cologne/).

[@olimex@mastodon.social](https://mastodon.social/@olimex) makers of the leading Gatemate board. 

[@PythonLinks@mastodon.social](https://mastodon.social/@PythonLinks) maintains this directory.

I encourage everyone to minimise your useage of corporate social media such as X/Twitter and [join the fediverse](https://JoinMastodon.org).   
