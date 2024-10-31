---

# Internal Temperature Sensor with Blue Pill using STM32CubeIDE

## Overview
This project demonstrates how to utilize the internal temperature sensor of the STM32F103C8T6 (Blue Pill) microcontroller to measure temperature in both Celsius and Fahrenheit. The STM32CubeIDE is used to configure the ADC (Analog-to-Digital Converter) and GPIO settings, enabling the temperature readings to control LEDs to indicate different temperature ranges.

## Prerequisites
- **STM32CubeIDE**: Ensure you have STM32CubeIDE installed on your computer.
- **Basic Knowledge of STM32CubeIDE**: A fundamental understanding of STM32CubeIDE, including configuring and uploading a simple LED blink program to the Blue Pill board.
  
  *Note*: For guidance, refer to video tutorials on installing STM32CubeIDE and running an LED blink project.

## STM32CubeIDE Configuration

### GPIO Settings
Set the following pins as output pins for the LEDs:
- **PA1** - LED indicator
- **PA4** - LED indicator
- **PA7** - LED indicator

### ADC Settings
To configure the ADC1 to read the internal temperature sensor:
1. Enable **Temperature Sensor Channel** in ADC1 settings.
2. Under **Parameter Settings**, enable **Continuous Conversion Mode**.
3. Set the sampling time to **55.5 Cycles** by navigating to **Rank → Sampling Time**.

For more details on sampling time calculation, refer to the STM32 reference manual:
- Page 225 and 235 of [Reference Manual](https://www.st.com/resource/en/reference_manual/cd00171190-stm32f101xx-stm32f102xx-stm32f103xx-stm32f105xx-and-stm32f107xx-advanced-arm-based-32-bit-mcus-stmicroelectronics.pdf).

## Temperature Calculation Formula

To calculate the temperature in Celsius and Fahrenheit, refer to the STM32 reference and datasheet:
- Formula derivation on [Page 236](https://www.st.com/resource/en/reference_manual/cd00171190-stm32f101xx-stm32f102xx-stm32f103xx-stm32f105xx-and-stm32f107xx-advanced-arm-based-32-bit-mcus-stmicroelectronics.pdf)
- Variable values on [Page 79](https://www.st.com/resource/en/datasheet/stm32f103c8.pdf)
  
![STM32-Internal-Temperatuer-Sensor-Equation](https://github.com/user-attachments/assets/d00ef69f-ceb2-4307-90da-e3da8dc20417)

This project will allow you to understand the basics of internal temperature sensing with STM32, using direct formulas and GPIO to reflect temperature conditions.
