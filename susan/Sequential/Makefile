CC := $(CROSS_COMPILE)gcc
CFLAGS := -lm -O2 

OBJS := susan

all: $(OBJS)

susan: susan.c
	$(CC) $^ -o $@ $(CFLAGS)

clean:
	rm -rf $(OBJS) output*

.PHONY: clean all
