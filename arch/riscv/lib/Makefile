# SPDX-License-Identifier: GPL-2.0+
#
# (C) Copyright 2000-2006
# Wolfgang Denk, DENX Software Engineering, wd@denx.de.
#
# Copyright (C) 2017 Andes Technology Corporation
# Rick Chen, Andes Technology Corporation <rick@andestech.com>

obj-$(CONFIG_CMD_BOOTM) += bootm.o
obj-$(CONFIG_CMD_GO) += boot.o
obj-y	+= cache.o
obj-y	+= interrupts.o
obj-y	+= reset.o
obj-y   += setjmp.o

# For building EFI apps
CFLAGS_$(EFI_CRT0) := $(CFLAGS_EFI)
CFLAGS_REMOVE_$(EFI_CRT0) := $(CFLAGS_NON_EFI)

CFLAGS_$(EFI_RELOC) := $(CFLAGS_EFI)
CFLAGS_REMOVE_$(EFI_RELOC) := $(CFLAGS_NON_EFI)

extra-$(CONFIG_CMD_BOOTEFI_HELLO_COMPILE) += $(EFI_CRT0) $(EFI_RELOC)
extra-$(CONFIG_CMD_BOOTEFI_SELFTEST) += $(EFI_CRT0) $(EFI_RELOC)
extra-$(CONFIG_EFI) += $(EFI_CRT0) $(EFI_RELOC)
