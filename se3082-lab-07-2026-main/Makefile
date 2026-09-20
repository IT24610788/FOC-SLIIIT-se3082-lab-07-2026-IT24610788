CC = mpicc
CFLAGS = -O3

all: Exercise02/sum_scatter Exercise03/sum_gather Exercise04/sum_reduce Exercise05/sum_allreduce Exercise06/sum_scan

Exercise02/sum_scatter: Exercise02/sum_scatter.c
	$(CC) $(CFLAGS) -o $@ $<

Exercise03/sum_gather: Exercise03/sum_gather.c
	$(CC) $(CFLAGS) -o $@ $<

Exercise04/sum_reduce: Exercise04/sum_reduce.c
	$(CC) $(CFLAGS) -o $@ $<

Exercise05/sum_allreduce: Exercise05/sum_allreduce.c
	$(CC) $(CFLAGS) -o $@ $<

Exercise06/sum_scan: Exercise06/sum_scan.c
	$(CC) $(CFLAGS) -o $@ $<

run: all
	@echo "=== Running Exercise 2: Scatter ==="
	mpirun --oversubscribe -np 4 ./Exercise02/sum_scatter
	@echo "\n=== Running Exercise 3: Gather ==="
	mpirun --oversubscribe -np 4 ./Exercise03/sum_gather
	@echo "\n=== Running Exercise 4: Reduce ==="
	mpirun --oversubscribe -np 4 ./Exercise04/sum_reduce
	@echo "\n=== Running Exercise 5: Allreduce ==="
	mpirun --oversubscribe -np 4 ./Exercise05/sum_allreduce
	@echo "\n=== Running Exercise 6: Scan ==="
	mpirun --oversubscribe -np 4 ./Exercise06/sum_scan

clean:
	rm -f Exercise02/sum_scatter Exercise03/sum_gather Exercise04/sum_reduce Exercise05/sum_allreduce Exercise06/sum_scan
