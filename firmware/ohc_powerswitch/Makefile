#
# This file is part of Open Home Control, http://www.open-home-control.com.
# Copyright (c) 2013 Uwe Freese
#
# Open Home Control is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by the
# Free Software Foundation, either version 3 of the License, or (at your
# option) any later version.
#
# Open Home Control is distributed in the hope that it will be useful, but
# WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General
# Public License for more details.
#
# You should have received a copy of the GNU General Public License along
# with Open Home Control. If not, see <http://www.gnu.org/licenses/>.
#

# CPU config
MCU		       = atmega168
F_CPU	       = 1000000
UART_BAUD_RATE = 4800

# Target file name (without extension).
TARGET = ohc_powerswitch

# Source files (C dependencies are automatically generated).
#   C			*.c
#   Assembler	*.S
CSRC = $(TARGET).c rfm12.c util.c uart.c aes256.c fuses.c
ASRC =
FUSES = -U hfuse:w:hfuse.hex:i -U lfuse:w:lfuse.hex:i -U efuse:w:efuse.hex:i -u

#******************************************************************************
# Include defaults
#******************************************************************************
# Compiler / Linker options
include ../makefile_common/Makefile.options
# General configuration
include ../makefile_common/Makefile.config
# Include make targets
include ../makefile_common/Makefile.targets
# Include make rules
include ../makefile_common/Makefile.rules
# Include the dependency files.
-include $(wildcard $(OBJDIR)/*.d)

