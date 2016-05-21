# Created by Anudorannador, Mar 9th, 2016

TEXBINDIR=
AUXFILETYPE= *.log *.aux *.dvi *.lof *.lot *.bit *.idx *.glo *.bbl *.bcf *.ilg *.toc *.ind *.out *.blg *.fdb_latexmk *.fls

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
	rm -rf $(AUXFILETYPE)
	cd texs && rm -rf $(AUXFILETYPE)
