
all: conf.pdf rep.pdf

%.pdf: %.tex body.tex
	pdflatex -interaction nonstopmode $<

watch:
	while inotifywait -e delete_self -e modify *.tex Makefile ; do \
		echo "============ at `date` ==========" ; \
		make all ; \
	done

.PHONY: all


