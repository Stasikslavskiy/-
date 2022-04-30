FILES = $(patsubst %.md, %.docx, $(wildcard *.md))
FILES += $(patsubst %.md, %.pdf, $(wildcard *.md))

LATEX_FORMAT =

ARGS = --pdf-engine=xelatex -V 'mainfont:Times New Roman'

%.docx: %.md
	-pandoc "$<" -o "$@" $(ARGS)

%.pdf: %.md
	-pandoc "$<" $(LATEX_FORMAT) -o "$@" $(ARGS)

all: $(FILES) @echo $(FILES)

clean:
	-rm $(FILES) *~
