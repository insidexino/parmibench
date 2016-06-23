PROCESSORS ?= 4

CC := $(CROSS_COMPILE)gcc
CFLAGS := -lpthread -O2

PARAMS := params.h
OBJS := dijkstra_parallel_mqueue dijkstra_parallel_squeue dijkstra_allpair

all: $(OBJS)

dijkstra_parallel_mqueue: dijkstra_parallel_mqueue.c $(PARAMS)
	$(CC) $< -o $@ $(CFLAGS)

dijkstra_parallel_squeue: dijkstra_parallel_squeue.c $(PARAMS)
	$(CC) $< -o $@ $(CFLAGS)

dijkstra_allpair: dijkstra_allpair.c $(PARAMS)
	$(CC) $< -o $@ $(CFLAGS)

$(PARAMS):
	./gen_defs.sh $(PARAMS) $(PROCESSORS)

clean:
	rm -rf $(OBJS) output* $(PARAMS)

.PHONY: all clean $(PARAMS)
