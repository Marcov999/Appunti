AUXX = $(addprefix build/, main.toc main.aux)

all: Geometria2.pdf

Geometria2.pdf: $(AUXX) main.tex
	cp $(AUXX) .
	pdflatex main.tex
	mv *.toc build
	mv *.aux build
	mv *.log build
	mv *.out build
	mv main.pdf Geometria2.pdf

$(AUXX): main.tex
	pdflatex main.tex
	mkdir -p build
	mv *.toc build
	mv *.aux build
	mv *.log build
	mv *.out build
	rm main.pdf

.PHONY: clean
clean:
	rm -rf build
