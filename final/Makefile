DOC=pandoc
DOCFLAGS=--filter pandoc-citeproc --csl=./ieee-with-url-and-doi.csl --self-contained --listing
DOCNAME=CSC450-SEN-dedominica
DOCTYPE=pdf
DOCOBJ=final.md
DOCHEAD=head.md
DOCTAIL=tail.md

all: pdf
	
doc:
	$(DOC) $(DOCHEAD) $(DOCOBJ) $(DOCTAIL) -o $(DOCNAME).$(DOCTYPE) $(DOCFLAGS)

# changes figure to figure* so figures break two column layout
pdf:
	$(DOC) $(DOCHEAD) $(DOCOBJ) $(DOCTAIL) $(DOCFLAGS) --to latex \
		| sed 's/figure/figure\*/' | pdflatex --jobname=$(DOCNAME)
	rm *.aux *.log *.out

# for professor
docx:
	$(DOC) $(DOCHEAD) $(DOCOBJ) $(DOCTAIL) -o $(DOCNAME).docx $(DOCFLAGS)

json:
	@$(DOC) $(DOCHEAD) $(DOCOBJ) $(DOCTAIL) $(DOCFLAGS) --to json

clean:
	rm $(DOCNAME).*
