# SPDX-License-Identifier: GPL-2.0
MODULE_NAME := v4l2loopback

ARCH ?= arm64

obj-$(CONFIG_VIDEO_LOOPBACK) += $(MODULE_NAME).o
$(MODULE_NAME)-objs := v4l2loopback.o

ccflags-y := $(EXTRA_CFLAGS)

all: clean modules

modules:
	$(MAKE) -C $(LINUXDIR) M=$(PWD) ARCH=$(ARCH) CROSS_COMPILE=$(CROSS_COMPILE) modules CONFIG_VIDEO_LOOPBACK=m

clean:
	rm -rf *.o *.ko *.mod.c *~ .*.cmd *.o.cmd .*.o.cmd *.mod \
	Module.symvers modules.order .tmp_versions modules.builtin
