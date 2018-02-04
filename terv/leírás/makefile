TARGET:=pályázat.pdf
DEPS:=$(wildcard *.tex)
TEMPORARY:=*.ind *.dvi *.glo *.lot *.idx *.lof \
	   *.log *.aux *.xdy *.idx *.ilg *.ist \
	   *.acn *.toc *.out *.pdf *.gen *.gz \
	   *.err *.txt *.backup *.*~

all: $(TARGET)

clean:
	@echo cleaning up ...
	@-rm -f $(TEMPORARY)

$(TARGET): $(DEPS)
	@echo compiling $@...
	@cd $(dir $@); pdflatex -shell-escape -synctex=1 -interaction=nonstopmode $(notdir $(basename $@)).tex >$(notdir $(basename $@)).txt# 2>$(notdir $(basename $@)).err
	@cd $(dir $@); pdflatex -shell-escape -synctex=1 -interaction=nonstopmode $(notdir $(basename $@)).tex >$(notdir $(basename $@)).txt# 2>$(notdir $(basename $@)).err
	@cd $(dir $@); pdflatex -shell-escape -synctex=1 -interaction=nonstopmode $(notdir $(basename $@)).tex >$(notdir $(basename $@)).txt# 2>$(notdir $(basename $@)).err
