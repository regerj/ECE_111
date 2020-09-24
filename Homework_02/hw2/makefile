#--------------------- Makefile -------------------------------------------------------------------

FILE =  Homework_02

#look up one directory for target .pdfs
#VPATH = ../

#all figures used must be in the directory "figures", else they will not be dependencies
#if there are no figures or they are of different format, edit the line below.
#FIGS := figures/*.eps figures/*.pdf

$(FILE).pdf : $(FILE).tex $(FIGS)
	rm -f *.pdf
	pdflatex $^ -file-line-error  #make the pdf, .tex and all figs are prerequsites
	rm $(FILE).pdf
	pdflatex $^ -file-line-error  #make the pdf, .tex and all figs are prerequsites
	chmod 755 $@
	
	#use this line to move the output into the parent directory
	#mv $@ ../

#make clean
#if make clean is left in it will hinder figure numbering but that can be changed too

.PHONY  : clean     #clean up the cruff
clean   :
	rm -f *.pdf *.aux *.log *.out *.ps *.toc *.nav *.snm *.dvi *.vrb *.plt *.data *-converted-to.pdf

#---------------------------------------------------------------------------------------------------
