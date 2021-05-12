
TEX=pdflatex
TEXFLAGS='-interaction=nonstopmode'

RM=rm -rf

TARGETS=Anfangsplenum_Folien.tex StAPF_Bericht.tex

%.pdf: %.tex
	$(TEX) $(TEXFLAGS) $< > /dev/null
	$(TEX) $(TEXFLAGS) $< > /dev/null

all: version $(TARGETS:%.tex=%.pdf)

version:
	$(TEX) -version

clean:
	@$(RM) $(TARGETS:%.tex=%.log) $(TARGETS:%.tex=%.aux) $(TARGETS:%.tex=%.out) $(TARGETS:%.tex=%.nav) $(TARGETS:%.tex=%.toc) $(TARGETS:%.tex=%.synctex.gz) $(TARGETS:%.tex=%.snm)

clean-all: clean
	@$(RM) $(TARGETS:%.tex=%.pdf)
