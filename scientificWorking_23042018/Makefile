FILE=OVGUPresentation

.PHONY: clean all compile

all: compile

compile:
	latexmk -bibtex -pdfps $(FILE).tex

clean:
	latexmk -c
	rm -f *.nav *.snm *.dvi *.ps *.pdf
