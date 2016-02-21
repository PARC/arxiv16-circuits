.PRECIOUS: %.mp

DEST  = adder_2.mps
DEST += multiplier.mps

%.mps: %.mp
	mpost $<
	mv $*.0 $*.mps

%.mp: %.fig
	fig2dev -L mp $< $@

%.tex %.eps: %.gp
	gnuplot $<

%.pdf: %.eps
	epstopdf $< --outfile=$@

all: $(DEST)

clean:
	rm -f *.mp *.mpx *.bak *.log *.aux *.tex *~
