# Build both CVs and copy the PDFs to the website's files/ folder
all: CV_long.pdf CV_short.pdf
	mkdir -p ../files/cv
	cp CV_long.pdf ../files/cv/CV_Robin_Uhrich_long.pdf
	cp CV_short.pdf ../files/cv/CV_Robin_Uhrich.pdf

%.pdf: %.tex
	latexmk -pdf -interaction=nonstopmode -halt-on-error $<

clean:
	latexmk -c

.PHONY: all clean
