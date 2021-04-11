SECS := $(wildcard secs/*.tex)

all: Geometria2.pdf

Geometria2.pdf: main.tex $(SECS) mstyle.sty
	pdflatex main.tex
	pdflatex main.tex
	mkdir -p build
	mv *.toc build
	mv *.aux build
	mv *.log build
	mv *.out build
	mv main.pdf Geometria2.pdf
	rm -rf build
