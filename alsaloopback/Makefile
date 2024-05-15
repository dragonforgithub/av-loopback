# SPDX-License-Identifier: GPL-2.0
MODULE_NAME := alsaloopback

ARCH ?= arm64

obj-$(CONFIG_AUDIO_LOOPBACK) += $(MODULE_NAME).o
$(MODULE_NAME)-objs := alsaloopback.o

ccflags-y := $(EXTRA_CFLAGS)

all: clean modules

modules:
	$(MAKE) -C $(LINUXDIR) M=$(PWD) ARCH=$(ARCH) CROSS_COMPILE=$(CROSS_COMPILE) modules CONFIG_AUDIO_LOOPBACK=m

clean:
	rm -rf *.o *.ko *.mod.c *~ .*.cmd *.o.cmd .*.o.cmd *.mod \
	Module.symvers modules.order .tmp_versions modules.builtin
