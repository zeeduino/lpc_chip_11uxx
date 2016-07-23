## LPC11U37H chip support library

This is identical to the official LPCOpen LPC11U37H chip support library
which can be found [here][LPCOpen LPC11U37H library]

Changes are mostly fixes:

* chip.h - removed **`|| defined(CHIP_LPC11UXX)`** from the code that defines `UART_IRQHandler` as `USART_IRQHandler`. LPCXpresso IDE v8 auto-generates code for LPC11U37H which expects **`UART_IRQHandler`** and **not** `USART` and this results in serial comm not working if project uses LPCOpen library (`__LPC_OPEN` is defined)






[LPCOpen LPC11U37Hxx library]: http://www.nxp.com/products/software-and-tools/hardware-development-tools/lpcxpresso-boards/lpcopen-software-development-platform-lpc11xx:LPCOPEN-SOFTWARE-FOR-LPC11XX
