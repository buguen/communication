all: pres report odf html

pres: content.mkd
	cat entete-beamer > pres.mkd
	cat content.mkd >> pres.mkd 
	multimarkdown -t latex pres.mkd -o pres.tex
	filter pres.tex
	pdflatex pres.tex 

report: content.mkd		
	cat entete-memoir > report.mkd
	cat content.mkd >> report.mkd 
	multimarkdown -t latex report.mkd -o report.tex
	filter report.tex
	pdflatex report.tex 

html: content.mkd 
	cat entete-html > web.mkd
	cat content.mkd >> web.mkd
	multimarkdown web.mkd 

odf: content.mkd 
	multimarkdown -t odf content.mkd > content.fodt
