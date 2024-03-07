.PHONY: all
all: slides.pdf notes.pdf

LATEXFLAGS+=	-shell-escape

SRC+=	frågesport.tex
SRC+=	abstract.tex
SRC+=	preamble.tex
SRC+=	fragesport.py

notes.pdf: notes.tex ${SRC}
slides.pdf: slides.tex ${SRC}

frågesport.tex: frågesport.nw


.PHONY:
all: frågesport

frågesport.py: frågesport.nw
frågesport fragesport.py: frågesport.py
	cp $^ $@
	chmod +x $@


.PHONY: clean
clean:
	${RM} frågesport frågesport.py frågesport.tex
	${RM} notes.pdf slides.pdf
	${RM} -R __pycache__



INCLUDE_MAKEFILES=../makefiles
include ${INCLUDE_MAKEFILES}/tex.mk
include ${INCLUDE_MAKEFILES}/noweb.mk
