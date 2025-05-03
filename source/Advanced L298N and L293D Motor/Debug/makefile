################################################################################
# Automatically-generated file. Do not edit!
# Toolchain: GNU Tools for STM32 (12.3.rel1)
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

OPTIONAL_TOOL_DEPS := \
$(wildcard ../makefile.defs) \
$(wildcard ../makefile.init) \
$(wildcard ../makefile.targets) \


BUILD_ARTIFACT_NAME := Advanced L298N and L293D Motor
BUILD_ARTIFACT_EXTENSION := elf
BUILD_ARTIFACT_PREFIX :=
BUILD_ARTIFACT := $(BUILD_ARTIFACT_PREFIX)$(BUILD_ARTIFACT_NAME)$(if $(BUILD_ARTIFACT_EXTENSION),.$(BUILD_ARTIFACT_EXTENSION),)

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
Advanced\ L298N\ and\ L293D\ Motor.elf \

MAP_FILES += \
Advanced\ L298N\ and\ L293D\ Motor.map \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Advanced\ L298N\ and\ L293D\ Motor.list \

OBJCOPY_HEX += \
Advanced\ L298N\ and\ L293D\ Motor.hex \


# All Target
all: main-build

# Main-build Target
main-build: Advanced\ L298N\ and\ L293D\ Motor.elf secondary-outputs

# Tool invocations
Advanced\ L298N\ and\ L293D\ Motor.elf Advanced\ L298N\ and\ L293D\ Motor.map: $(OBJS) $(USER_OBJS) E:\stm\Advanced\ L298N\ and\ L293D\ Motor\STM32F103C6TX_FLASH.ld makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-gcc -o "Advanced L298N and L293D Motor.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"E:\stm\Advanced L298N and L293D Motor\STM32F103C6TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Advanced L298N and L293D Motor.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Advanced\ L298N\ and\ L293D\ Motor.list: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Advanced L298N and L293D Motor.list"
	@echo 'Finished building: $@'
	@echo ' '

Advanced\ L298N\ and\ L293D\ Motor.hex: $(EXECUTABLES) makefile objects.list $(OPTIONAL_TOOL_DEPS)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "Advanced L298N and L293D Motor.hex"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) Advanced\ L298N\ and\ L293D\ Motor.elf Advanced\ L298N\ and\ L293D\ Motor.hex Advanced\ L298N\ and\ L293D\ Motor.list Advanced\ L298N\ and\ L293D\ Motor.map Advanced\\ L298N\\ and\\ L293D\\ Motor.elf default.size.stdout
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX)

fail-specified-linker-script-missing:
	@echo 'Error: Cannot find the specified linker script. Check the linker settings in the build configuration.'
	@exit 2

warn-no-linker-script-specified:
	@echo 'Warning: No linker script specified. Check the linker settings in the build configuration.'

.PHONY: all clean dependents main-build fail-specified-linker-script-missing warn-no-linker-script-specified

-include ../makefile.targets
