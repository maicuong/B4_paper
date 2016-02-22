# tex makefile

TARGET = my_thesis
ENCODE = utf8

all:
	ebb ./fig/*.pdf
	ebb ./fig/*.png
	ebb ./fig/*.jpg
	platex   -kanji=$(ENCODE) -shell-escape $(TARGET)
	pbibtex  -kanji=$(ENCODE) $(TARGET)
	platex   -kanji=$(ENCODE) -shell-escape $(TARGET)
	platex   -kanji=$(ENCODE) -shell-escape $(TARGET)
	dvipdfmx -p a4 $(TARGET)
	open $(TARGET).pdf
nobib:
	platex   -kanji=$(ENCODE) $(TARGET)
	platex   -kanji=$(ENCODE) $(TARGET)
	platex   -kanji=$(ENCODE) $(TARGET)
	dvipdfmx -p a4 $(TARGET)
	open $(TARGET).pdf
clean:
	/bin/rm -f *~ *.log *.dvi *.blg *.aux *.out *.bbl *.toc *.lof $(TARGET).pdf
