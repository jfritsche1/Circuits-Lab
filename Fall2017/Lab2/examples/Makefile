EXAMPLE_DOC=example_doc
EXAMPLE_DOC_TEX=$(EXAMPLE_DOC).tex
EXAMPLE_DOC_PREAMBLE_TEX=$(EXAMPLE_DOC)_preamble.tex
EXAMPLE_DOC_WRAP=$(EXAMPLE_DOC)_wrap
EXAMPLE_DOC_WRAP_TEX=$(EXAMPLE_DOC_WRAP).tex

EXAMPLE_DOC_OUTPUT_PDF=$(EXAMPLE_DOC_WRAP).pdf

LATEX_COMPILER=pdflatex
PDF_READER=firefox

example_build: $(EXAMPLE_DOC_TEX) $(EXAMPLE_DOC_PREAMBLE_TEX) $(EXAMPLE_DOC_WRAP_TEX)
	$(LATEX_COMPILER) $(EXAMPLE_DOC_WRAP_TEX)

example_read: example_build
	$(PDF_READER) $(EXAMPLE_DOC_OUTPUT_PDF)

# Variables omitted for readability so you can use this as an example for commands.
bandgap_build: 
	python2 bandgap_graph.py
	pdflatex bandgap_graph.tex
