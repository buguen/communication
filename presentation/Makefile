all: pres report odf html

pres: content.md
	cat entete-beamer > pres.md
	cat content.md >> pres.md 
	multimarkdown -t latex pres.md -o pres.tex
	filter pres.tex
	pdflatex pres.tex 

report: content.md		
	cat entete-memoir > report.md
	cat content.md >> report.md 
	multimarkdown -t latex report.md -o report.tex
	filter report.tex
	pdflatex report.tex 

html: content.md 
	cat entete-html > web.md
	cat content.md >> web.md
	multimarkdown web.md 

odf: content.md 
	multimarkdown -t odf content.md > content.odt
