###############################################################
# Program:
#     Assignment 03, QUEUE
#     Brother JonesL, CS235
# Author:
#     Maximiliano Correa, Esteban Cabrera and Tony Moraes
# Summary:
#      The files compiled in this make file allow stocks to 
#		to be purchased and sold utilizing queues.
# Time:
#     6.00 hs
###############################################################

##############################################################
# The main rule
##############################################################
a.out: queue.h assignment03.o dollars.o stock.o transaction.o portfolio.o
	g++ -o a.out assignment03.o dollars.o stock.o transaction.o portfolio.o
	tar -cf assignment03.tar *.h *.cpp makefile

dollarsTest: dollars.o dollarsTest.cpp
	g++ -o dollarsTest dollars.o dollarsTest.cpp

##############################################################
# The individual components
#      assignment03.o       : the driver program
#      dollars.o      : the Dollars class
#      stock.o        : the logic for the stock program
#      transaction.o  : the logic for the transaction program
#      portfolio.o    : the logic for the portfolio program
##############################################################
assignment03.o: queue.h assignment03.cpp
	g++ -c assignment03.cpp

dollars.o: dollars.h dollars.cpp
	g++ -c dollars.cpp

stock.o: stock.h stock.cpp queue.h
	g++ -c stock.cpp

transaction.o: transaction.h transaction.cpp dollars.h
	g++ -c transaction.cpp

portfolio.o: portfolio.h portfolio.cpp queue.h transaction.h dollars.h
	g++ -c portfolio.cpp
