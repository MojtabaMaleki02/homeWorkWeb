sources = $(wildcard *.Rmd)
targets = $(sources:.Rmd=.md)

.PHONY: all
all: $(targets)

%.md: %.Rmd
	Rscript -e 'rmarkdown::render("$<")'

.PHONY: clean
clean:
	rm -f $(targets)
	rm -f $(targets:.md=.html)
	rm -f wordcloud*.png
