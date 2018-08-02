Fuse testing
========

Build
-----
	apt-get install libacl1-dev git
	git clone https://github.com/billziss-gh/secfs.test.git
	make

Tests cases
-----
	python fsrand.py /dir/ -c 1000 -v

	./fs_racer.sh 60 /dir/

	./fsstress -d /dir/ -l 2 -n 100000 -p 4 -r -X -v

	./bonnie++ -x 60 -d /dir/ -u root

	./iozone -R -b /shared/tests/bench_u02_test.xls -r 8k -s 10m -t 1 -F /dir/testing

	./iozone -R -b /shared/test/bench_u01_test.xls -r 8k -s 100m -l 2 -u 10

	./iozone -l 2 -u 2 -r 16k -s 512M -F /dir/t1 /dir/t2

