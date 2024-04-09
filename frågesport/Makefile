.PHONY: all
all: slides.pdf notes.pdf

LATEXFLAGS+=	-shell-escape
USE_PYTHONTEX=true

SRC+=	frågesport.tex
SRC+=	abstract.tex
SRC+=	preamble.tex
SRC+=	fragesport.py

DEPENDS+=	didactic.sty

notes.pdf: notes.tex ${SRC} ${DEPENDS}
slides.pdf: slides.tex ${SRC} ${DEPENDS}

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
INCLUDE_BIBEDU=../bibedu
include ${INCLUDE_BIBEDU}/bibedu.mk
INCLUDE_DIDACTIC=../didactic
include ${INCLUDE_DIDACTIC}/didactic.mk
