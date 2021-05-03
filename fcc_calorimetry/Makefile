# Run this targets regardless of any file of the given existing
.PHONY: fcc_calorimetry.pdf all clean deploy

DATE := $(shell LC_ALL=en_US.UTF-8 date '+%Y_%b_%d' | tr A-Z a-z)
DEST := boltzmann:/var/www/kjvbrt.org/fcc/presentations

all: fcc_calorimetry.pdf

fcc_calorimetry.pdf: fcc_calorimetry.tex
	latexmk -xelatex -use-make fcc_calorimetry.tex
	@cp fcc_calorimetry.pdf archive/fcc_calorimetry_${DATE}.pdf

deploy:
	scp fcc_calorimetry.pdf ${DEST}/fcc_calorimetry.pdf
	scp fcc_calorimetry.pdf ${DEST}/fcc_calorimetry_${DATE}.pdf

clean:
	latexmk -CA
