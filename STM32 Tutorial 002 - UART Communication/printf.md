

### Includes 

```c
/* USER CODE BEGIN Includes */
#include <stdio.h>              // printf
/* USER CODE END Includes */
```

### Private Function Prototypes

```c
/* USER CODE BEGIN PFP */
/**
 *  @see https://github.com/STMicroelectronics/STM32CubeF4/blob/master/Projects/STM32F401RE-Nucleo/Examples/UART/UART_Printf/Src/main.c
 */
#ifdef __GNUC__
/* With GCC, small printf (option LD Linker->Libraries->Small printf
 set to 'Yes') calls __io_putchar() */
#define PUTCHAR_PROTOTYPE int __io_putchar(int ch)
#else
#define PUTCHAR_PROTOTYPE int fputc(int ch, FILE *f)
#endif /* __GNUC__ */
/* USER CODE END PFP */
```


### Implementation

(end of file)

```c
/* USER CODE BEGIN 4 */
/**
 * @brief  Retargets the C library printf function to the USART.
 * @param  None
 * @retval None
 * @see    https://github.com/STMicroelectronics/STM32CubeF4/blob/master/Projects/STM32F401RE-Nucleo/Examples/UART/UART_Printf/Src/main.c
 */
PUTCHAR_PROTOTYPE {
	/* Place your implementation of fputc here */
	/* e.g. write a character to the EVAL_COM1 and Loop until the end of transmission */
	HAL_UART_Transmit(&huart3, (uint8_t *) &ch, 1, 1);

	return ch;
}
/* USER CODE END 4 */
```

