.PHONY: all
all: notes.pdf slides.pdf

LATEXFLAGS+=	-shell-escape

SRC+=		preamble.tex
SRC+=		abstract.tex contents.tex

DEPENDS+=	fig/teens.png
DEPENDS+=	fig/listening-assistants.png
DEPENDS+=	fig/analytica.png
DEPENDS+=	fig/Automating-Inequality.jpg
DEPENDS+=	fig/Algorithms-of-Oppression.jpg
DEPENDS+=	fig/hacking-jeep.png
DEPENDS+=	fig/Weapons-of-Math-Destruction.jpg
DEPENDS+=	fig/The-Age-of-Surveillance-Capitalism.jpg
DEPENDS+=	fig/tay.ai.png
DEPENDS+=	fig/adint.png

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
