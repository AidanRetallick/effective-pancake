PDFTOPNG = pdftoppm -png 
TEX = pdflatex -shell-escape -interaction=nonstopmode -file-line-error

.PHONY: all view

all : rectangular_sheet.pdf rectangular_sheet.png

view :	open rectangular_sheet.pdf

rectangular_sheet.png : rectangular_sheet.pdf
	$(PDFTOPNG) rectangular_sheet.pdf out
	mv out-1.png rectangular_sheet.png
 
rectangular_sheet.pdf : rectangular_sheet.tex
	$(TEX) rectangular_sheet.tex

rectangular_sheet.aux : rectangular_sheet.tex
	$(TEX) rectangular_sheet.tex

clean:
	rm rectangular_sheet.aux
	rm rectangular_sheet.pdf
	rm rectangular_sheet.log
	rm rectangular_sheet.png
