all:libtest.a testabc

libtest.a:test_a.o test_b.o test_c.o
	ar crv libtest.a test_a.o test_b.o test_c.o 
	
test_a.o:test_a.cc so_test.h
	g++ -c test_a.cc
test_b.o:test_b.cc so_test.h
	g++ -c test_b.cc
test_c.o:test_c.cc so_test.h
	g++ -c test_c.cc
	
testabc:testabc.o
	g++ -o testabc testabc.o libtest.a

testabc.o:testabc.cc
	g++ -c testabc.cc
	
clean:
	rm *.o *.a
