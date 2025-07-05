# Bare-Metal STM32F411 LED Blinker  

## Description  
Blinks an LED on PA5 using direct register access (no HAL/LL libraries).  
![E71D8326-0F6F-43B3-9C35-EC16BE7DE33B](https://github.com/user-attachments/assets/57616265-c84c-4b0f-878d-f362205d784d)

## Key Features  
- **Register-level control**:  
  - `RCC->AHB1ENR`: Enables GPIOA clock  
  - `GPIOA->MODER`: Sets PA5 as output  
  - `GPIOA->ODR`: Toggles LED state  
- **Simple delay**: Busy-loop for blink timing  
- **Hardware**: Any STM32 with LED on PA5  

## Usage  
1. Connect LED to PA5 (with current-limiting resistor)  
2. Compile & flash (e.g., with `arm-none-eabi-gcc`)  
3. LED blinks at ~1Hz (adjust loop counter for timing)  

## Why?  
Demonstrates bare-metal STM32 programming, bypassing HAL for minimal overhead.  
