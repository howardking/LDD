ifneq ($(KERNELRELEASE),)
    obj-m := Hello_world.o

else
    KERNELDIR ?= /lib/modules/$(shell uname -r)/build
    PWD       := $(shell pwd)

CC := arm-linux-gcc

default:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) modules
endif
