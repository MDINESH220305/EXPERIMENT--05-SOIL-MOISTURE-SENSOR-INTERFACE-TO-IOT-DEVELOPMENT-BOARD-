# NAME:Dinesh.M
# REGNO:212222043002
# EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-
## Aim: To Interface a Analog Input  (soil moisture sensor) to ARM IOT development board and write a  program to obtain  the data on the com port 
## Components required: STM32 CUBE IDE, ARM IOT development board,  STM programmer tool.
## Theory 
#### Hardware Overview
A typical soil moisture sensor consists of two parts.

The Probe
The sensor includes a fork-shaped probe with two exposed conductors that is inserted into the soil or wherever the moisture content is to be measured.

As previously stated, it acts as a variable resistor, with resistance varying according to soil moisture.

![1](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/8dac5c37-21eb-4e0c-87da-c7884fd73120)


The Module
In addition, the sensor includes an electronic module that connects the probe to the Arduino.

The module generates an output voltage based on the resistance of the probe, which is available at an Analog Output (AO) pin.

The same signal is fed to an LM393 High Precision Comparator, which digitizes it and makes it available at a Digital Output (DO) pin.

![2](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/882a234a-df46-4fba-bb31-468e5c94b085)


The module includes a potentiometer for adjusting the sensitivity of the digital output (DO).

You can use it to set a threshold, so that when the soil moisture level exceeds the threshold, the module outputs LOW otherwise HIGH.

This setup is very useful for triggering an action when a certain threshold is reached. For example, if the moisture level in the soil exceeds a certain threshold, you can activate a relay to start watering the plant.


Soil Moisture Sensor Pinout
The soil moisture sensor is extremely simple to use and only requires four pins to connect.

soil moisture sensor pinout
AO (Analog Output) generates analog output voltage proportional to the soil moisture level, so a higher level results in a higher voltage and a lower level results in a lower voltage.

DO (Digital Output) indicates whether the soil moisture level is within the limit. D0 becomes LOW when the moisture level exceeds the threshold value (as set by the potentiometer), and HIGH otherwise.

VCC supplies power to the sensor. It is recommended that the sensor be powered from 3.3V to 5V. Please keep in mind that the analog output will vary depending on the voltage supplied to the sensor.

GND is the ground pin.

![3](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/137d6910-cb12-42dc-bf86-d2864c6945c3)


## Procedure:
 1. click on STM 32 CUBE IDE, the following screen will appear 
 
![4](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/40eb53fd-d643-4599-997e-3782e2f3620a)

 2. click on FILE, click on new stm 32 project
 3. ![5](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/3faff339-649e-4746-b863-c99e4676af05)

![6](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/34f00d07-3b6d-4f5e-9fcd-b64a99485a45)

4. select the target to be programmed  as shown below and click on next 


![7](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/a10c6ab8-f008-40c3-abc3-45f8a9ff590a)

4.select the program name 

![8](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/6ebdef74-4935-437e-97c5-19f7e3d0802d)


5. corresponding ioc file will be generated automatically 

![9](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/90429448-de66-4cb3-bd53-1138e8b98ea2)


6.select the appropriate pins as gipo, in or out, USART or required options and configure 

![10](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/dc3da6ef-ce0a-4994-a8a0-3ae6e98a48d6)

![11](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/f7253e47-05a3-44fc-97a3-d03ffc4759a5)



7.click on cntrl+S , automaticall C program will be generated 

![12](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/3d9f038b-5a2a-4cb8-8bdf-dead236d48f0)

![13](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/965633e5-92d9-4551-b45d-8fb1d4db8337)


8. edit the program and as per required 
![14](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/c19e0e92-0ada-4886-b415-e2699470ad23)



9. use project and build all 

![15](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/e5435d6f-65d1-4f50-9a7f-411e175ba078)

  
10. once the project is bulild 

 ![16](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/b815c0d4-887a-4509-9e91-dc09bba000a1)


11. click on debug option 


![17](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/3a136fb7-736a-4579-a5ed-b25e3bd20501)


12. connect the  iot board to power supply and usb 

![18](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/6a31a959-b351-476d-8b0d-8c189296292b)


13. After connecting open the STM cube programmer 
14. click on UART and click on connect 

![19](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/cd4912b1-bcd5-4acc-a0aa-da3fe26d2aac)


15. once it is connected , click on Erasing and programming option 
![20](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/8be1c1ca-4ab2-428f-a39d-ac7b6ef7d725)


16. flash the bin or hex file as shown below by switching the switch to flash mode 

![21](https://github.com/MDINESH220305/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/162429215/eef74b7a-e242-48c5-9e48-984ef8ac7244)


17. check for execution of the output by switching the board to run mode 
18. open serial port utility and select appropritate com port, run and verify the reuslts of moisture content .


## STM 32 CUBE PROGRAM :
```C

#include "main.h"
#include "Soil Moisture Sensor.h"
#include "stdio.h"

UART_HandleTypeDef huart2;
void SystemClock_Config(void);
static void MX_GPIO_Init(void);
static void MX_USART2_UART_Init(void);
void ADC_Init(void);
void GPIO_Init(void);

#if defined (__ICCARM__) || defined (__ARMCC_VERSION)
#define PUTCHAR_PROTOTYPE int fputc(int ch, FILE *f)
#elif defined(__GNUC__)
#define PUTCHAR_PROTOTYPE int __io_putchar(int ch)
#endif 

PUTCHAR_PROTOTYPE
{
    HAL_UART_Transmit(&huart2, (uint8_t *)&ch, 1, 0xFFFF);
    return ch;
}

int main(void)
{
    HAL_Init();
    SystemClock_Config();
    MX_GPIO_Init();
    MX_USART2_UART_Init();
    ADC_Init();
    GPIO_Init();
    while (1)
    {
        soil_moisture();
    }
}

void SystemClock_Config(void)
{
    RCC_OscInitTypeDef RCC_OscInitStruct = {0};
    RCC_ClkInitTypeDef RCC_ClkInitStruct = {0};
    __HAL_PWR_VOLTAGESCALING_CONFIG(PWR_REGULATOR_VOLTAGE_SCALE2);
    RCC_OscInitStruct.OscillatorType = RCC_OSCILLATORTYPE_MSI;
    RCC_OscInitStruct.MSIState = RCC_MSI_ON;
    RCC_OscInitStruct.MSICalibrationValue = RCC_MSICALIBRATION_DEFAULT;
    RCC_OscInitStruct.MSIClockRange = RCC_MSIRANGE_6;
    RCC_OscInitStruct.PLL.PLLState = RCC_PLL_NONE;
    if (HAL_RCC_OscConfig(&RCC_OscInitStruct) != HAL_OK)
    {
        Error_Handler();
    }
    RCC_ClkInitStruct.ClockType = RCC_CLOCKTYPE_HCLK3 | RCC_CLOCKTYPE_HCLK | RCC_CLOCKTYPE_SYSCLK | RCC_CLOCKTYPE_PCLK1 |  RCC_CLOCKTYPE_PCLK2;
    RCC_ClkInitStruct.SYSCLKSource = RCC_SYSCLKSOURCE_MSI;
    RCC_ClkInitStruct.AHBCLKDivider = RCC_SYSCLK_DIV1;
    RCC_ClkInitStruct.APB1CLKDivider = RCC_HCLK_DIV1;
    RCC_ClkInitStruct.APB2CLKDivider = RCC_HCLK_DIV1;
    RCC_ClkInitStruct.AHBCLK3Divider = RCC_SYSCLK_DIV1;
    if (HAL_RCC_ClockConfig(&RCC_ClkInitStruct, FLASH_LATENCY_0) != HAL_OK)
    {
        Error_Handler();
    }
}
 
```


## Output screen shots on serial monitor   :
![1](https://github.com/Rajkiran0604/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/164345543/8020cc73-cca4-4e94-8d50-9aa1875e5067)
![2](https://github.com/Rajkiran0604/EXPERIMENT--05-SOIL-MOISTURE-SENSOR-INTERFACE-TO-IOT-DEVELOPMENT-BOARD-/assets/164345543/1e61c8f1-ded0-45e4-9c3c-24f513d3b174)
 
## Result :
Interfacing a Analog Input (soil moisture sensor) with ARM microcontroller based IOT development is executed and the results visualized on serial monitor 
