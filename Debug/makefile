################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F0xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
stm32f030_uart_overrun.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
stm32f030_uart_overrun.list \

OBJCOPY_BIN += \
stm32f030_uart_overrun.bin \


# All Target
all: stm32f030_uart_overrun.elf secondary-outputs

# Tool invocations
stm32f030_uart_overrun.elf: $(OBJS) $(USER_OBJS) C:\Workspace\_Demo\stm32f030_uart_overrun\STM32F030R8TX_FLASH.ld
	arm-none-eabi-gcc -o "stm32f030_uart_overrun.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0 -T"C:\Workspace\_Demo\stm32f030_uart_overrun\STM32F030R8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="stm32f030_uart_overrun.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

stm32f030_uart_overrun.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "stm32f030_uart_overrun.list"
	@echo 'Finished building: $@'
	@echo ' '

stm32f030_uart_overrun.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "stm32f030_uart_overrun.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
