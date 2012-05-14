TEXFLAGS=-shell-escape -synctex=1
AUXFILES=definitions

all : winxp
.PHONY : all

list-targets : FORCE
	@echo "winxp"
.PHONY : list-targets

winxp : Lab3-MoteMap.tex FORCE
	for file in ${AUXFILES}; do echo "\input{$@/$$file}" >> $$file.tex; done
	pdflatex ${TEXFLAGS} Lab3-MoteMap.tex
	pdflatex ${TEXFLAGS} Lab3-MoteMap.tex
	mv Lab3-MoteMap.pdf Lab3-MoteMap-$@.pdf
	make clean_auxfiles

clean_auxfiles : FORCE
	for file in ${AUXFILES}; do rm -f $$file.tex; done
	rm -f Lab3-MoteMap.aux Lab3-MoteMap.log Lab3-MoteMap.out Lab3-MoteMap.pyg Lab3-MoteMap.synctex.gz

clean : clean_auxfiles
	rm -f Lab3-MoteMap*.pdf
.PHONY : clean

FORCE :
