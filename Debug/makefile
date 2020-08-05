################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
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
G4\ blinky.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
G4\ blinky.list \

OBJCOPY_BIN += \
G4\ blinky.bin \


# All Target
all: G4\ blinky.elf secondary-outputs

# Tool invocations
G4\ blinky.elf: $(OBJS) $(USER_OBJS) D:\git\STM32_blinky_task_ru\STM32G431RBTX_FLASH.ld
	arm-none-eabi-gcc -o "G4 blinky.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"D:\git\STM32_blinky_task_ru\STM32G431RBTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="G4 blinky.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

G4\ blinky.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "G4 blinky.list"
	@echo 'Finished building: $@'
	@echo ' '

G4\ blinky.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "G4 blinky.bin"
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
