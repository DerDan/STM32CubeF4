#THIS FILE IS AUTO GENERATED FROM THE TEMPLATE! DO NOT CHANGE!
set(CMAKE_SYSTEM_NAME Generic)
set(CMAKE_SYSTEM_VERSION 1)
cmake_minimum_required(VERSION 3.7)

#set(TOOLCHAIN_DIR "C:/Program Files (x86)/GNU Tools ARM Embedded/4.9 2014q4")
set(TOOLCHAIN_DIR "C:/Program Files (x86)/GNU Tools ARM Embedded/8 2018-q4-major")

# specify cross compilers and tools
#set(CMAKE_C_COMPILER_WORKS 1)
#set(CMAKE_CXX_COMPILER_WORKS 1)
set(CMAKE_C_COMPILER ${TOOLCHAIN_DIR}/bin/arm-none-eabi-gcc.exe)
set(CMAKE_CXX_COMPILER ${TOOLCHAIN_DIR}/bin/arm-none-eabi-g++.exe)
set(CMAKE_ASM_COMPILER ${TOOLCHAIN_DIR}/bin/arm-none-eabi-gcc.exe)
set(CMAKE_AR ${TOOLCHAIN_DIR}/bin/arm-none-eabi-ar.exe)
set(CMAKE_OBJCOPY ${TOOLCHAIN_DIR}/bin/arm-none-eabi-objcopy.exe)
set(CMAKE_OBJDUMP ${TOOLCHAIN_DIR}/bin/arm-none-eabi-objdump.exe)
set(SIZE ${TOOLCHAIN_DIR}/bin/arm-none-eabi-size.exe)


set(CMAKE_EXE_LINKER_FLAGS_INIT "-Wl,-nostdlib -Wl,-X -Wl,--omagic -Wl,--fatal-warnings -Wl,-EL -Wl,--gc-sections")
set(CMAKE_EXE_LINKER_FLAGS "-specs=nosys.specs" CACHE INTERNAL "")

#set(LINKER_SCRIPT_MAIN ${CMAKE_SOURCE_DIR}/G071_SoundCam/STM32G071KBUX_FLASH.ld)
#set(LINKER_SCRIPT ${CMAKE_SOURCE_DIR}/G071_SoundCam/stm32_flash.ld)


#set(CMAKE_CXX_FLAGS_INIT "${COMMON_FLAGS} -std=c++11")
#set(CMAKE_C_FLAGS_INIT "${COMMON_FLAGS} -std=gnu99")


add_link_options(
        -specs=nano.specs
)


project(demo C ASM)
set(CMAKE_C_STANDARD 11)


add_compile_options(
        -fmessage-length=0
        -fno-diagnostics-show-caret
        -mtp=soft
        -mcpu=cortex-m4
        -mlittle-endian
        -mfloat-abi=hard
        -mfpu=fpv4-sp-d16
        -mthumb
        -fno-dwarf2-cfi-asm
        -fno-builtin
        -ffunction-sections
        -fdata-sections
        -fshort-enums
        -fno-common
        -Wunused-variable
        -Wunused-but-set-variable
        -Wunused-value
        -Waddress
        -Wreturn-type
        -Wparentheses
        -g2
        -fno-diagnostics-show-caret
        -fshort-enums
        -Wall
        -ffreestanding
        -fmessage-length=0
        -mlittle-endian
        -mthumb
        -fno-dwarf2-cfi-asm
        -ffunction-sections
        -fdata-sections
        -fno-common
)

add_link_options(
        -fmessage-length=0
        -fno-diagnostics-show-caret
        -mtp=soft
        -mcpu=cortex-m4
        -mlittle-endian
        -mfloat-abi=hard
        -mfpu=fpv4-sp-d16
        -mthumb
        -nostdinc
        -g3
        -fno-dwarf2-cfi-asm
        -fno-builtin
        -ffunction-sections
        -fdata-sections
        -fshort-enums
        -fno-common
        -Wunused-variable
        -Wunused-but-set-variable
        -Wunused-value
        -Waddress
        -Wreturn-type
        -Wparentheses
        -fno-exceptions
        -fno-rtti
        -Wdelete-non-virtual-dtor
        -g2
        -Wl,--gc-sections
        -specs=nano.specs
        -Wl,-X
        -Wl,--omagic
        -Wl,--fatal-warnings
        -Wl,-EL
        -Wl,--gc-sections
)
add_definitions(
        -DUSE_HAL_DRIVER
        -DSTM32F407xx
        -DUSE_STM324xG_EVAL
)

set(ST_LIB_SOURCE
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_adc.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_adc_ex.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_can.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_cortex.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_crc.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_cryp.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_cryp_ex.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_dac.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_dac_ex.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_dcmi.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_dma.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_dma2d.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_dma_ex.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_eth.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_flash.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_flash_ex.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_gpio.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_hash.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_hash_ex.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_hcd.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_i2c.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_i2c_ex.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_i2s.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_i2s_ex.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_irda.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_iwdg.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_ltdc.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_msp_template.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_nand.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_nor.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_pccard.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_pcd.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_pcd_ex.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_pwr.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_pwr_ex.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_rcc.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_rcc_ex.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_rng.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_rtc.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_rtc_ex.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_sai.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_sd.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_sdram.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_smartcard.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_spi.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_sram.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_tim.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_tim_ex.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_uart.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_usart.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_hal_wwdg.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_ll_fmc.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_ll_fsmc.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_ll_sdmmc.c
        ${CMAKE_CURRENT_LIST_DIR}/Drivers/STM32F4xx_HAL_Driver/Src/stm32f4xx_ll_usb.c
        )

add_library(
        stHAL
        ${ST_LIB_SOURCE}
)
target_include_directories(
        stHAL
        PUBLIC
        Drivers/CMSIS/Device/ST/STM32F4xx/Include
        Drivers/STM32F4xx_HAL_Driver/Inc
        Drivers/STM32F4xx_HAL_Driver/Inc/Legacy
        Drivers/CMSIS/Core/Include
        Projects/STM324xG_EVAL/Applications/LwIP/LwIP_HTTP_Server_Netconn_RTOS/Inc

)


add_library(
        stBSP
        Drivers/BSP/Components/cs43l22/cs43l22.c
        Drivers/BSP/Components/ili9325/ili9325.c
        Drivers/BSP/Components/ov2640/ov2640.c
        Drivers/BSP/Components/stmpe811/stmpe811.c
        Drivers/BSP/STM324xG_EVAL/stm324xg_eval.c
#        Drivers/BSP/STM324xG_EVAL/stm324xg_eval_audio.c
#        Drivers/BSP/STM324xG_EVAL/stm324xg_eval_camera.c
        Drivers/BSP/STM324xG_EVAL/stm324xg_eval_io.c
        Drivers/BSP/STM324xG_EVAL/stm324xg_eval_lcd.c
#        Drivers/BSP/STM324xG_EVAL/stm324xg_eval_sd.c
        Drivers/BSP/STM324xG_EVAL/stm324xg_eval_sram.c
#        Drivers/BSP/STM324xG_EVAL/stm324xg_eval_ts.c
        Utilities/CPU/cpu_utils.c
        Utilities/Fonts/font8.c
        Utilities/Fonts/font12.c
        Utilities/Fonts/font16.c
        Utilities/Fonts/font20.c
        Utilities/Fonts/fonts.h
        Utilities/Log/lcd_log.c
        Utilities/Log/lcd_log.h
)

target_include_directories(
        stBSP
        PUBLIC
        Drivers/BSP/Components
        Drivers/BSP/Components/Common
        Drivers/BSP/STM324xG_EVAL
        Utilities/CPU/
        Utilities/Fonts/
        Utilities/Log
)

target_link_libraries(
        stBSP
        stHAL
        FreeRTOS
)

add_library(
        FreeRTOS
        Middlewares/Third_Party/FreeRTOS/Source/portable/MemMang/heap_4.c
        Middlewares/Third_Party/FreeRTOS/Source/portable/GCC/ARM_CM4F/port.c
        Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS/cmsis_os.c
        Middlewares/Third_Party/FreeRTOS/Source/croutine.c
        Middlewares/Third_Party/FreeRTOS/Source/tasks.c
        Middlewares/Third_Party/FreeRTOS/Source/queue.c
        Middlewares/Third_Party/FreeRTOS/Source/list.c
        Middlewares/Third_Party/FreeRTOS/Source/timers.c


)

target_include_directories(
        FreeRTOS
        PUBLIC
        Middlewares/Third_Party/FreeRTOS/Source/portable/GCC/ARM_CM4F
        Middlewares/Third_Party/FreeRTOS/Source/include
        Drivers/CMSIS/Include
        Projects/STM324xG_EVAL/Applications/LwIP/LwIP_HTTP_Server_Netconn_RTOS/Inc
        Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS
)


add_library(
        LwIP
        Middlewares/Third_Party/LwIP/src/core/ipv4/autoip.c
        Middlewares/Third_Party/LwIP/src/core/ipv4/igmp.c
        Middlewares/Third_Party/LwIP/src/core/ipv4/ip4_frag.c
        Middlewares/Third_Party/LwIP/src/core/ipv4/ip4_addr.c
        Middlewares/Third_Party/LwIP/src/core/ipv4/ip4.c
        Middlewares/Third_Party/LwIP/src/core/ipv4/etharp.c
        Middlewares/Third_Party/LwIP/src/core/ipv4/dhcp.c
        Middlewares/Third_Party/LwIP/src/core/ipv4/icmp.c
        Middlewares/Third_Party/LwIP/src/api/tcpip.c
        Middlewares/Third_Party/LwIP/src/api/api_msg.c
        Middlewares/Third_Party/LwIP/src/api/netbuf.c
        Middlewares/Third_Party/LwIP/src/api/sockets.c
        Middlewares/Third_Party/LwIP/src/api/err.c
        Middlewares/Third_Party/LwIP/src/api/netifapi.c
        Middlewares/Third_Party/LwIP/src/api/api_lib.c
        Middlewares/Third_Party/LwIP/src/api/netdb.c
        Middlewares/Third_Party/LwIP/src/apps/http/fs.c
        Middlewares/Third_Party/LwIP/src/apps/http/httpd.c
        Middlewares/Third_Party/LwIP/system/OS/sys_arch.c
        Middlewares/Third_Party/LwIP/src/netif/ethernet.c
        Middlewares/Third_Party/LwIP/src/core/netif.c
        Middlewares/Third_Party/LwIP/src/core/stats.c
        Middlewares/Third_Party/LwIP/src/core/mem.c
        Middlewares/Third_Party/LwIP/src/core/inet_chksum.c
        Middlewares/Third_Party/LwIP/src/core/tcp.c
        Middlewares/Third_Party/LwIP/src/core/timeouts.c
        Middlewares/Third_Party/LwIP/src/core/ip.c
        Middlewares/Third_Party/LwIP/src/core/sys.c
        Middlewares/Third_Party/LwIP/src/core/raw.c
        Middlewares/Third_Party/LwIP/src/core/tcp_out.c
        Middlewares/Third_Party/LwIP/src/core/init.c
        Middlewares/Third_Party/LwIP/src/core/pbuf.c
        Middlewares/Third_Party/LwIP/src/core/dns.c
        Middlewares/Third_Party/LwIP/src/core/def.c
        Middlewares/Third_Party/LwIP/src/core/memp.c
        Middlewares/Third_Party/LwIP/src/core/udp.c
        Middlewares/Third_Party/LwIP/src/core/tcp_in.c
)

target_include_directories(
        LwIP
        PUBLIC
        #        <IncludePath>../Inc
        Middlewares/Third_Party/LwIP/src/include
        Middlewares/Third_Party/LwIP/src
        Middlewares/Third_Party/LwIP/system
        Projects/STM324xG_EVAL/Applications/LwIP/LwIP_HTTP_Server_Netconn_RTOS/Inc
        Projects/STM324xG_EVAL/Applications/LwIP/LwIP_HTTP_Server_Netconn_RTOS/Src
        #;../Src
        #;../../../../../../Utilities
        #;../../../../../../Utilities/Log</IncludePath>
)

target_link_libraries(
        LwIP
        FreeRTOS
)


add_subdirectory(Projects/STM324xG_EVAL/Applications/LwIP/LwIP_HTTP_Server_Netconn_RTOS/CMake)



