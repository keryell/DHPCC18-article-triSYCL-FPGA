DOCUMENT=DHPCC-2018-triSYCL-FPGA
LATEX_FLAGS=-synctex=1 -file-line-error

all:
	pdflatex $(LATEX_FLAGS) $(DOCUMENT)
	bibtex $(DOCUMENT)
	pdflatex $(LATEX_FLAGS) $(DOCUMENT)
	pdflatex $(LATEX_FLAGS) $(DOCUMENT)

clean:
	rm -f *.aux *.bbl *.blg *.dvi *.lof *.log *.lot *.out *.toc
