- Use release profile
- Tuning the features
- Remove:
--> Slicing block device (if using only internal memory)
--> targets.device_has_remove : ["STDIO_MESSAGES"]
--> target.console_uart
--> disable mbed-trace
--> disable: platform.callback-comparable, platform.minimal-printf-enable-64-bit
--> stub out/overwrite mbed_die (removes 1.5kB! Pulls in GPIO drivers)
--> disable mbed fault handler (define: "MBED_FAULT_HANDLER_DISABLED")

