set(BinName "pico-test")
add_executable(${BinName}
	main.cpp
)

pico_enable_stdio_usb(${BinName} 1)
pico_enable_stdio_uart(${BinName} 1)

target_link_libraries(${BinName}
	pico_stdlib
	hardware_spi
	pico-tflmicro
)

pico_add_extra_outputs(${BinName})
