set(LINKER_SCRIPT
        ${CMAKE_CURRENT_LIST_DIR}/../SW4STM32/STM324xG_EVAL/STM32F407IGHx_FLASH.ld
        )
set(src
        ../Src/system_stm32f4xx.c
        ../Src/main.c
        ../Src/app_ethernet.c
        ../Src/stm32f4xx_it.c
        ../Src/stm32f4xx_hal_timebase_tim.c
        ../Src/ethernetif.c
        ../Src/httpserver-netconn.c
        ../Inc/app_ethernet.h
        ../Inc/ethernetif.h
        ../Inc/FreeRTOSConfig.h
        ../Inc/httpserver-netconn.h
        ../Inc/lcd_log_conf.h
        ../Inc/lwipopts.h
        ../Inc/main.h
        ../Inc/stm32f4xx_hal_conf.h
        ../Inc/stm32f4xx_it.h
        ../SW4STM32/startup_stm32f407xx.s
        ../SW4STM32/syscalls.c
        ${LINKER_SCRIPT}

        )


#<IncludePath>../Inc;
#../Src;
#../../../../../../Drivers/CMSIS/Device/ST/STM32F4xx/Include;
#../../../../../../Drivers/STM32F4xx_HAL_Driver/Inc;
#../../../../../../Drivers/BSP/STM324xG_EVAL;
#../../../../../../Drivers/BSP/Components;
#../../../../../../Middlewares/Third_Party/LwIP/src/include/;
#../../../../../../Middlewares/Third_Party/LwIP/system;
#../../../../../../Middlewares/Third_Party/FreeRTOS/Source/portable/RVDS/ARM_CM4F;
#../../../../../../Middlewares/Third_Party/FreeRTOS/Source/include;
#../../../../../../Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS;
#../../../../../../Utilities;
#../../../../../../Utilities/Log</IncludePath>

include_directories(
        ../Inc
)
add_executable(
        demo.elf
        ${src}
)


target_link_libraries(
        demo.elf
        FreeRTOS
        stBSP
        LwIP
)

target_link_options(demo.elf
        PRIVATE
        -T ${LINKER_SCRIPT}
        -Wl,-Map=${CMAKE_CURRENT_BINARY_DIR}/${PROJECT_NAME}.map
        )

