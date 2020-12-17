# Run this targets regardless of any file of the given existing
.PHONY: upstream_corr.pdf all clean

all: upstream_corr.pdf

upstream_corr.pdf: upstream_corr.tex
	latexmk -xelatex -use-make upstream_corr.tex
	@cp upstream_corr.pdf \
		archive/upstream_corr_`date '+%Y_%b_%d' | tr A-Z a-z`.pdf

clean:
	latexmk -CA
