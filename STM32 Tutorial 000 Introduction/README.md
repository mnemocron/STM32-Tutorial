# STM32 Tutoriall 000 - Intro

Embedded Software Programming on the STM32 Plattform

---

## Getting Started

In this first chapter I will give a brief introduction on how to get started with programming STM32 microcontrollers.
I will point out sources of information and I will show how to use this information for your daily programming work.

---

### IDE

#### STM32CubeMX Initialization Code Generator

- **[STM32CubeMX Download](https://www.st.com/en/development-tools/stm32cubemx.html)**
- User Manual STM32CubeMX for STM32 configuration and initialization C code generation **[UM1718](https://www.st.com/content/ccc/resource/technical/document/user_manual/10/c5/1a/43/3a/70/43/7d/DM00104712.pdf/files/DM00104712.pdf/jcr:content/translations/en.DM00104712.pdf)** (pdf)


#### Keil µVision

The professional tool by ARM in eval mode with a 32kB code size limitation.
In my tutorials I will use Keil µVision 5.

- [arm Keil Downloads](https://www.keil.com/download/product/)
    + **[MDK-ARM eval](https://www.keil.com/demo/eval/arm.htm)** (Keil µVision) (registration required)

#### System Workbench for MCU by AC6 (Open Source)

Uses the open source `gcc-arm-none-eabi` compiler.

- STMicroelectronics [AC6](https://www.st.com/content/st_com/en/partner/partner-program/partnerpage/AC6.html)
    + [ac6-tools](https://www.ac6-tools.com/content.php/content_SW4MCU/lang_en_GB.xphp)
    + openstm32.org **[Download](https://www.openstm32.org/System%2BWorkbench%2Bfor%2BSTM32)** (registration required)

---

### Hardware Documentation (Datasheets / User Manuals)

For the basic introduction I will use the STM32F103 Nucleo board and link to the files related to this board.

#### ARM

Here you will find more generic documentation about the ARM Cortex<span><sup>&trade;</sup></span>-M Core.

- [Keil Product Manuals](http://www.keil.com/support/man_arm.htm)
    + **[Getting started with MDK](https://armkeil.blob.core.windows.net/product/gs_MDK5_4_en.pdf)** (pdf)
    + [µVision User's Guide](http://www.keil.com/support/man/docs/uv4/)

It is an engineers job to be able to read manufacturer documentation. This is why I will not explain any further how to use the IDE, as the [Getting started with MDK](https://armkeil.blob.core.windows.net/product/gs_MDK5_4_en.pdf) already covers the installation process and the usage of the software.
Please note that Keil µVision uses a **Package Manager** for Hardware specific drivers and software.

- [arm Developer Documentation](https://developer.arm.com/docs)
- **[arm Infocenter](http://infocenter.arm.com/help/index.jsp)**

##### Architecture Overview

ARM Cortex<span><sup>&trade;</sup></span>-M stands for Microcontroller architecture. There are different profiles, hence M0, M1, M3, M4 and M7.


- Cortex<span><sup>&trade;</sup></span>-M0 [Generic User Guide](http://infocenter.arm.com/help/topic/com.arm.doc.dui0497a/DUI0497A_cortex_m0_r0p0_generic_ug.pdf) (pdf) (contains Instruction Set information)
- Cortex<span><sup>&trade;</sup></span>-M1 Generic User Guide (reference needed)
- Cortex<span><sup>&trade;</sup></span>-M3 [Generic User Guide](http://infocenter.arm.com/help/topic/com.arm.doc.dui0552a/DUI0552A_cortex_m3_dgug.pdf) (pdf) (contains Instruction Set information)
- Cortex<span><sup>&trade;</sup></span>-M4 [Generic User Guide](http://infocenter.arm.com/help/topic/com.arm.doc.dui0553b/DUI0553.pdf) (pdf) (contains Instruction Set information)
- Cortex<span><sup>&trade;</sup></span>-M7 [Generic User Guide](http://infocenter.arm.com/help/topic/com.arm.doc.dui0646a/DUI0646A_cortex_m7_dgug.pdf) (pdf) (contains Instruction Set information)

#### STMicroelectronics

##### Hardware Abstraction Layer (**HAL**) Libraries

The following documents contain the documentation for the HAL libraries provided by STMicroelectronics. 

- Description of **STM32F0** HAL and low-layer drivers **[UM1785](https://www.st.com/content/ccc/resource/technical/document/user_manual/2f/77/25/0f/5c/38/48/80/DM00122015.pdf/files/DM00122015.pdf/jcr:content/translations/en.DM00122015.pdf)** (pdf)
- Description of **STM32F1** HAL and low-layer drivers **[UM1850](https://www.st.com/content/ccc/resource/technical/document/user_manual/72/52/cc/53/05/e3/4c/98/DM00154093.pdf/files/DM00154093.pdf/jcr:content/translations/en.DM00154093.pdf)** (pdf)
- Description of **STM32F2** HAL and low-layer drivers **[UM1940](https://www.st.com/content/ccc/resource/technical/document/user_manual/56/32/53/cb/69/86/49/0e/DM00223149.pdf/files/DM00223149.pdf/jcr:content/translations/en.DM00223149.pdf)** (pdf)
- Description of **STM32F3** HAL and low-layer drivers **[UM1786](https://www.st.com/content/ccc/resource/technical/document/user_manual/a6/79/73/ae/6e/1c/44/14/DM00122016.pdf/files/DM00122016.pdf/jcr:content/translations/en.DM00122016.pdf)** (pdf)
- Description of **STM32F4** HAL and low-layer drivers **[UM1725](https://www.st.com/content/ccc/resource/technical/document/user_manual/2f/71/ba/b8/75/54/47/cf/DM00105879.pdf/files/DM00105879.pdf/jcr:content/translations/en.DM00105879.pdf)** (pdf)
- Description of **STM32L4** HAL and low-layer drivers **[UM1884](https://www.st.com/content/ccc/resource/technical/document/user_manual/63/a8/8f/e3/ca/a1/4c/84/DM00173145.pdf/files/DM00173145.pdf/jcr:content/translations/en.DM00173145.pdf)** (pdf)
- Description of **STM32F7** HAL and low-layer drivers **[UM1905](https://www.st.com/content/ccc/resource/technical/document/user_manual/45/27/9c/32/76/57/48/b9/DM00189702.pdf/files/DM00189702.pdf/jcr:content/translations/en.DM00189702.pdf)** (pdf)
- Description of **STM32H7** HAL and low-layer drivers **[UM2217](https://www.st.com/content/ccc/resource/technical/document/user_manual/group0/40/ee/88/53/f6/1e/4c/87/DM00392525/files/DM00392525.pdf/jcr:content/translations/en.DM00392525.pdf)** (pdf)

---

### JTAG Debugers / Programmers

amongst others...

- STMicroelectronics [ST-Link/V2](https://www.st.com/en/development-tools/st-link-v2.html) (included on STM32-Nucleo boards) (~ $25)
- 1bitsquared [Black Magic Probe](https://github.com/blacksphere/blackmagic/wiki) ([store](https://1bitsquared.com/products/black-magic-probe)) (~ $60)
- Segger [J-Link EDU Mini](https://www.segger.com/products/debug-probes/j-link/models/j-link-edu-mini/) (~ $25)














