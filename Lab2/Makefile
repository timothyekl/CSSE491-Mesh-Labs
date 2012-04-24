TEXFLAGS=-shell-escape -synctex=1
AUXFILES=definitions

all : winxp
.PHONY : all

list-targets : FORCE
	@echo "winxp"
.PHONY : list-targets

winxp : Lab2-Sensing.tex FORCE
	for file in ${AUXFILES}; do echo "\input{$@/$$file}" >> $$file.tex; done
	pdflatex ${TEXFLAGS} Lab2-Sensing.tex
	pdflatex ${TEXFLAGS} Lab2-Sensing.tex
	mv Lab2-Sensing.pdf Lab2-Sensing-$@.pdf
	make clean_auxfiles

clean_auxfiles : FORCE
	for file in ${AUXFILES}; do rm -f $$file.tex; done
	rm -f Lab2-Sensing.aux Lab2-Sensing.log Lab2-Sensing.out Lab2-Sensing.pyg Lab2-Sensing.synctex.gz

clean : clean_auxfiles
	rm -f Lab2-Sensing*.pdf
.PHONY : clean

FORCE :
