TEXFLAGS=-shell-escape -synctex=1
AUXFILES=definitions

all : winxp
.PHONY : all

list-targets : FORCE
	@echo "winxp"
.PHONY : list-targets

winxp : Lab1-nesC.tex FORCE
	for file in ${AUXFILES}; do echo "\input{$@/$$file}" >> $$file.tex; done
	pdflatex ${TEXFLAGS} Lab1-nesC.tex
	pdflatex ${TEXFLAGS} Lab1-nesC.tex
	mv Lab1-nesC.pdf Lab1-nesC-$@.pdf
	make clean_auxfiles

clean_auxfiles : FORCE
	for file in ${AUXFILES}; do rm -f $$file.tex; done
	rm -f Lab1-nesC.aux Lab1-nesC.log Lab1-nesC.out Lab1-nesC.pyg Lab1-nesC.synctex.gz

clean : clean_auxfiles
	rm -f Lab1-nesC*.pdf
.PHONY : clean

FORCE :
