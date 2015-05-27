export STAGING_DIR=/home/nichola/workspace/openwrt/wrtnode/staging_dir
export TARGET_DIR=$(STAGING_DIR)/target-mipsel_24kec+dsp_uClibc-0.9.33.2
export CC=mipsel-openwrt-linux-uclibc-gcc
export LD=mipsel-openwrt-linux-uclibc-ld
export CFLAGS:=-I$(TARGET_DIR)/usr/include
export LDFLAGS:=-L$(TARGET_DIR)/usr/lib -ldl
# Top level makefile, the real shit is at src/makefile

TARGETS=noopt 32bit

all:
	cd src && $(MAKE) $@

install:
	cd src && $(MAKE) $@

$(TARGETS):
	cd src && $(MAKE) $@

doc:
	cd doc && $(MAKE)

test:
	cd test && $(MAKE)

TAGS:
	find . -type f -name "*.[ch]" | xargs etags -

clean:
	cd src && $(MAKE) $@
	cd test && $(MAKE) $@
	cd doc && $(MAKE) $@
	rm -f TAGS

distclean: clean

dummy:

.PHONY: doc install test TAGS
