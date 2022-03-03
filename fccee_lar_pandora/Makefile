# Run this targets regardless of any file of the given existing
.PHONY: fccee_lar_pandora.pdf all clean deploy

DATE := $(shell LC_ALL=en_US.UTF-8 date '+%Y_%b_%d' | tr A-Z a-z)
DEST := boltzmann:/var/www/kjvbrt.org/fcc/presentations

all: fccee_lar_pandora.pdf

fccee_lar_pandora.pdf: fccee_lar_pandora.tex
	latexmk -xelatex \
		-xelatex="xelatex -shell-escape %O %S" \
		-use-make \
		fccee_lar_pandora.tex
	@cp fccee_lar_pandora.pdf archive/fccee_lar_pandora_${DATE}.pdf

deploy:
	scp fccee_lar_pandora.pdf ${DEST}/fccee_lar_pandora.pdf
	scp fccee_lar_pandora.pdf ${DEST}/fccee_lar_pandora_${DATE}.pdf

clean:
	latexmk -CA
