all : GUISimple CourbeCarre

GUISimple : gui_simple.o
	g++ -lQtGui -lQtCore $^ -o $@

CourbeCarre : carre.o
	g++ -lQtGui -lQtCore -L/net/cremi/cte/M2/TP1/qcustomplot/sharedlib/compilation -lqcustomplot $^ -o $@

gui_simple.o : gui_simple.cpp
	g++ -I/usr/include/qt4/ -I/usr/include/qt4/QtGui/ -I/usr/include/qt4/QtCore/ -c  $^ -o $@ 

carre.o : carre.cpp
	g++ -I/net/cremi/cte/M2/TP1/qcustomplot -I/usr/include/qt4/ -I/usr/include/qt4/QtGui/ -I/usr/include/qt4/QtCore/ -c  $^ -o $@ 

clean :
	rm -f *~ *.o
mrproper : clean
	rm -f GUISimple CourbeCarre

