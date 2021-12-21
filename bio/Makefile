.PHONY: all
all: notes.pdf slides.pdf

LATEXFLAGS+=	-shell-escape

SRC+=		preamble.tex
SRC+=		abstract.tex contents.tex

DEPENDS+=	fig/laggarbergs-skola.png
DEPENDS+=	fig/laggarberg-sweden.png
DEPENDS+=	fig/laggarberg-close.png
DEPENDS+=	fig/mariedalsskolan.png
DEPENDS+=	fig/mariedal-laggarberg.png
DEPENDS+=	fig/tigy.png
DEPENDS+=	fig/tigy-map.png
DEPENDS+=	fig/miun.jpg
DEPENDS+=	fig/miun-map.png
DEPENDS+=	fig/kth.jpg
DEPENDS+=	fig/kth-map.png
DEPENDS+=	fig/kth-flyg.jpg
DEPENDS+=	fig/inria-rennes.jpg
DEPENDS+=	fig/inria-map.png

notes.pdf: notes.tex
notes.pdf: ${SRC} ${DEPENDS}

slides.pdf: slides.tex
slides.pdf: ${SRC} ${DEPENDS}

fig/%:
	${MAKE} -C $(dir $@) $(notdir $@)


.PHONY: clean
clean:
	${RM} notes.pdf slides.pdf


INCLUDE_MAKEFILES=../makefiles
include ${INCLUDE_MAKEFILES}/tex.mk
