# Run this targets regardless of any file of the given existing
.PHONY: energy_corr.pdf all clean

all: energy_corr.pdf

energy_corr.pdf: energy_corr.tex
	latexmk -xelatex -use-make energy_corr.tex
	@cp energy_corr.pdf \
		archive/energy_corr_`date '+%Y_%b_%d' | tr A-Z a-z`.pdf

clean:
	latexmk -CA
