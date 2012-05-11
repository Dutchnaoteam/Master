FILE =  WorldCupTDP

all: article

article:
	rm -f ${FILE}.pdf
	pdflatex ${FILE}
	bibtex ${FILE}
	pdflatex ${FILE}
	pdflatex ${FILE}
#	makeindex ICCS2002article156
#	latex ICCS2002article156
#	dvipdf ${FILE}

draft:
	pdflatex ${FILE}
#	dvipdf ${FILE}

tar:
	tar cvf ${FILE}.tar ${FILE}.tex ${FILE}.bib figures/*.png *.cls *.sty *.bst Makefile
	gzip ${FILE}.tar

clean:
	rm -f *.aux *.log *.dvi *.toc *.lof *.lot *.tmp *.idx *.ilg *.ind *.blg *.bbl

public:
	cp -p ${FILE}.pdf ~/public_html/publications/
