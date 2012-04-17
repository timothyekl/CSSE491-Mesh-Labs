TEXFLAGS=-shell-escape -synctex=1
AUXFILES=definitions

all : winxp
.PHONY : all

list-targets : FORCE
	@echo "winxp"
.PHONY : list-targets

winxp : Lab0-Setup.tex FORCE
	for file in ${AUXFILES}; do echo "\input{$@/$$file}" >> $$file.tex; done
	pdflatex ${TEXFLAGS} Lab0-Setup.tex
	pdflatex ${TEXFLAGS} Lab0-Setup.tex
	mv Lab0-Setup.pdf Lab0-Setup-$@.pdf
	make clean_auxfiles

clean_auxfiles : FORCE
	for file in ${AUXFILES}; do rm -f $$file.tex; done
	rm -f Lab0-Setup.aux Lab0-Setup.log Lab0-Setup.out Lab0-Setup.pyg Lab0-Setup.synctex.gz

clean : clean_auxfiles
	rm -f Lab0-Setup*.pdf
.PHONY : clean

FORCE :
