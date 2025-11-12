# "World of Adventure" campaign guide - Makefile
# Written by Christopher Thomas.


BASENAME=world-of-adv
GUIDENAME=$(BASENAME)-houserules
DMNAME=$(BASENAME)-dmhouserules

DOCBITS=\
	$(BASENAME)-over.tex		\
	$(BASENAME)-chargen.tex		\
	$(BASENAME)-classes.tex		\
	$(BASENAME)-skills.tex		\
	$(BASENAME)-feats.tex		\
	$(BASENAME)-equip.tex		\
	$(BASENAME)-spells.tex		\
	$(GUIDENAME).tex		\
	$(DMNAME).tex

# FIXME - Old version parts.
#	$(BASENAME)-indus.tex		\
#	$(BASENAME)-magic.tex		\
#	$(BASENAME)-rules.tex		\
#	$(BASENAME)-pcnotes.tex		\
#	$(BASENAME)-dmnotes.tex		\
#	$(BASENAME)-hooks.tex		\


default: force install

force: clean $(GUIDENAME).pdf $(DMNAME).pdf

clean: tclean
	rm -f $(GUIDENAME).pdf $(DMNAME).pdf

tclean:
	rm -f $(GUIDENAME).log $(GUIDENAME).aux $(GUIDENAME).toc
	rm -f $(DMNAME).log $(DMNAME).aux $(DMNAME).toc
	rm -f texput.*

install:
	mv $(GUIDENAME).pdf ../documents/
	mv $(DMNAME).pdf ../documents/

uninstall:
	rm -f ../documents/$(GUIDENAME).pdf
	rm -f ../documents/$(DMNAME).pdf


$(GUIDENAME).pdf: $(DOCBITS)
	pdflatex $(GUIDENAME).tex
	pdflatex $(GUIDENAME).tex
	make tclean

$(DMNAME).pdf: $(DOCBITS)
	pdflatex $(DMNAME).tex
	pdflatex $(DMNAME).tex
	make tclean

# This is the end of the file.
