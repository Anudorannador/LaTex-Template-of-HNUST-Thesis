# Created by Anudorannador, Mar 9th, 2016

TEXBINDIR=

.PHONY: all tex bib clean

all: clean
	make tex
	make bib
	make tex
	make tex

tex:
	$(TEXBINDIR)xelatex -synctex=1 -interaction=nonstopmode "main".tex

bib:
	$(TEXBINDIR)bibtex main

clean:
	rm -rf *.aux *.log main.pdf *.syntex.gz *.synctex.gz *.toc *.bak~ *.bak *.swap *.bbl *.blg
	cd texs && rm -rf *.aux *.log *.syntex.gz *.synctex.gz *.toc *.bak~ *.bak *.swap
