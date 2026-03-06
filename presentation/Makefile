.PHONY: all clean

all: main.pdf main-notes.pdf

main.pdf: main.tex references.bib
	pdflatex -interaction=nonstopmode main.tex
	bibtex main
	pdflatex -interaction=nonstopmode main.tex
	pdflatex -interaction=nonstopmode main.tex

main-notes.pdf: main.tex references.bib
	pdflatex -interaction=nonstopmode -jobname=main-notes "\def\shownotes{1}\input{main.tex}"
	bibtex main-notes
	pdflatex -interaction=nonstopmode -jobname=main-notes "\def\shownotes{1}\input{main.tex}"
	pdflatex -interaction=nonstopmode -jobname=main-notes "\def\shownotes{1}\input{main.tex}"

clean:
	rm -f *.aux *.bbl *.blg *.log *.nav *.out *.snm *.toc *.vrb main-notes.pdf
