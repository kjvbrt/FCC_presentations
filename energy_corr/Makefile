# Run this targets regardless of any file of the given existing
.PHONY: energy_corr.pdf all clean deploy

DATE := $(shell LC_ALL=en_US.UTF-8 date '+%Y_%b_%d' | tr A-Z a-z)
DEST := boltzmann:/var/www/kjvbrt.org/fcc/presentations

all: energy_corr.pdf

energy_corr.pdf: energy_corr.tex
	latexmk -xelatex -use-make energy_corr.tex
	@cp energy_corr.pdf archive/energy_corr_${DATE}.pdf

deploy:
	scp energy_corr.pdf ${DEST}/energy_corr.pdf
	scp energy_corr.pdf ${DEST}/energy_corr_${DATE}.pdf

clean:
	latexmk -CA
