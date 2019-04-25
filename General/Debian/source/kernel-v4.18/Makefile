obj-m := tcp_nanqinlang.o

all:
	make -C /lib/modules/${KVERSION}/build M=`pwd` modules CC=/usr/bin/gcc

clean:
	make -C /lib/modules/${KVERSION}/build M=`pwd` clean

install:
	install tcp_nanqinlang.ko /lib/modules/${KVERSION}/kernel/net/ipv4
	insmod /lib/modules${KVERSION}/kernel/net/ipv4/tcp_nanqinlang.ko
	depmod -a

uninstall:
	rm /lib/modules/${KVERSION}/kernel/net/ipv4/tcp_nanqinlang.ko
