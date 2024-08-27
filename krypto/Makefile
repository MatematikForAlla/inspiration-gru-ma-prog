.PHONY: all
all: slides.pdf notes.pdf

LATEXFLAGS+=	-shell-escape

SRC+=	krypto.tex
SRC+=	abstract.tex
SRC+=	preamble.tex
SRC+=	rovarspraket.py

notes.pdf: notes.tex ${SRC}
slides.pdf: slides.tex ${SRC}

krypto.tex: krypto.nw


.PHONY:
all: krypto

krypto.py: krypto.nw
krypto rovarspraket.py: krypto.py
	cp $^ $@
	chmod +x $@


.PHONY: clean
clean:
	${RM} krypto krypto.py krypto.tex
	${RM} notes.pdf slides.pdf
	${RM} __pycache__



INCLUDE_MAKEFILES=../makefiles
include ${INCLUDE_MAKEFILES}/tex.mk
include ${INCLUDE_MAKEFILES}/noweb.mk
