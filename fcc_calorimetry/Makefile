# Run this targets regardless of any file of the given existing
.PHONY: fcc_calorimetry.pdf all clean

all: fcc_calorimetry.pdf

fcc_calorimetry.pdf: fcc_calorimetry.tex
	latexmk -xelatex -use-make fcc_calorimetry.tex
	@cp fcc_calorimetry.pdf \
		archive/fcc_calorimetry_`date '+%Y_%b_%d' | tr A-Z a-z`.pdf

clean:
	latexmk -CA
