HEADERS = storage_mgr.h dberror.h test_helper.h buffer_mgr_stat.h
CC = gcc
CFLAGS = -I

default: test_1

test_1: test_case_1.o buffer_mgr.o storage_mgr.o dberror.o buffer_mgr_stat.o
	$(CC) -o test_1 test_case_1.o buffer_mgr.o storage_mgr.o dberror.o buffer_mgr_stat.o

test_case_1.o: test_assign2_1.c $(HEADERS)
	$(CC) -o test_case_1.o -c test_assign2_1.c -lm

buffer_mgr.o: buffer_mgr.c $(HEADERS)
		$(CC) -c buffer_mgr.c -o buffer_mgr.o
    
storage_mgr.o: storage_mgr.c $(HEADERS)
		$(CC) -c storage_mgr.c -o storage_mgr.o

dberror.o: dberror.c dberror.h
		$(CC) -c dberror.c

buffer_mgr_stat.o: buffer_mgr_stat.c $(HEADERS)
		$(CC) -c buffer_mgr_stat.c

clean:
	$(RM) test_1 *.o *~
run_test_1:
	./test_1
