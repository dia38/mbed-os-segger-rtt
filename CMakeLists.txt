add_library(mbed-segger-rtt INTERFACE)

target_sources(
    mbed-segger-rtt
    INTERFACE
        segger/Config/SEGGER_RTT_Conf.h
        segger/RTT/SEGGER_RTT_ASM_ARMv7M.S
        segger/RTT/SEGGER_RTT_printf.c
        segger/RTT/SEGGER_RTT.c
        segger/RTT/SEGGER_RTT.h
        src/retarget_segger_rtt.h
        src/retarget_segger_rtt.cpp
)

target_include_directories(
    mbed-segger-rtt
    INTERFACE
        segger/Config
        segger/RTT
        src
)