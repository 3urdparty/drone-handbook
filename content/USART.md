**Setting up .ioc**:
![[Screenshot from 2025-07-11 18-36-55.png]]
Set `EXTI line[15:10] interrupts` to **Enabled**
![[Pasted image 20250711213337.png]]

>![NOTE] Info:
>Oversampling: redundancy to reduce error/noise


To transmit a message over `UART`:
```c
HAL_UART_Transmit(&huart2, (const uint8_t*) msg, 15, TIMEOUT);
```

To open a console in STM32CubeIDE:
![[Pasted image 20250711213031.png]]
And select Command Shell Console. Make sure to select `Serial Port` and set up the connection.
![[Pasted image 20250711213117.png]]