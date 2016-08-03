all:libtest.a testabc

libtest.a:test_a.o test_b.o test_c.o
	ar crv libtest.a test_a.o test_b.o test_c.o
	mv libtest.a /home/ene/leetcode/mfln/lib
	
	
test_a.o:/home/ene/leetcode/mfln/src/test_a.cc /home/ene/leetcode/mfln/src/so_test.h
	g++ -c /home/ene/leetcode/mfln/src/test_a.cc
test_b.o:/home/ene/leetcode/mfln/src/test_b.cc /home/ene/leetcode/mfln/src/so_test.h
	g++ -c /home/ene/leetcode/mfln/src/test_b.cc
test_c.o:/home/ene/leetcode/mfln/src/test_c.cc /home/ene/leetcode/mfln/src/so_test.h
	g++ -c /home/ene/leetcode/mfln/src/test_c.cc
	
testabc:testabc.o
	g++ -o testabc /home/ene/leetcode/mfln/obj/testabc.o /home/ene/leetcode/mfln/lib/libtest.a
	mv testabc /home/ene/leetcode/mfln/bin

testabc.o:/home/ene/leetcode/mfln/src/testabc.cc
	g++ -c /home/ene/leetcode/mfln/src/testabc.cc -o testabc.o
	mv test_a.o /home/ene/leetcode/mfln/obj
	mv test_b.o /home/ene/leetcode/mfln/obj
	mv test_c.o /home/ene/leetcode/mfln/obj
	mv testabc.o /home/ene/leetcode/mfln/obj
	
clean:
	rm /home/ene/leetcode/mfln/lib/* /home/ene/leetcode/mfln/bin/* /home/ene/leetcode/mfln/obj/*
