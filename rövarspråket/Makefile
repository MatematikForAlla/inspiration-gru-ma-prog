.PHONY: all
all: slides.pdf notes.pdf

LATEXFLAGS+=	-shell-escape
NOWEAVEFLAGS.tex=	-n -delay -t2

SRC+=	rövarspråket.tex
SRC+=	abstract.tex
SRC+=	preamble.tex
SRC+=	rovarspraket.py

notes.pdf: notes.tex ${SRC}
slides.pdf: slides.tex ${SRC}

rövarspråket.tex: rövarspråket.nw


.PHONY:
all: rövarspråket

rövarspråket.py: rövarspråket.nw
rövarspråket rovarspraket.py: rövarspråket.py
	cp $^ $@
	chmod +x $@


.PHONY: clean
clean:
	${RM} rövarspråket rövarspråket.py rövarspråket.tex
	${RM} notes.pdf slides.pdf



INCLUDE_MAKEFILES=../makefiles
include ${INCLUDE_MAKEFILES}/tex.mk
include ${INCLUDE_MAKEFILES}/noweb.mk
