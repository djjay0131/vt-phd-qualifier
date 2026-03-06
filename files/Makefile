.PHONY: all clean

all: slides.pdf

slides.pdf: slides.tex
	pdflatex -interaction=nonstopmode slides.tex
	pdflatex -interaction=nonstopmode slides.tex

clean:
	rm -f *.aux *.log *.nav *.out *.snm *.toc *.pdf *.bbl *.blg *.xml *.bcf