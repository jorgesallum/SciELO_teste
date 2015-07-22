all:
	rm LIVRO.pdf
	make clean
	latexmk -xelatex LIVRO.tex
scielo:
	latexmk -quiet -interaction=nonstopmode -xelatex LIVRO.tex
lua:
	lualatex  LIVRO.tex
	lualatex  LIVRO.tex
test:
	xelatex LIVRO.tex
	xelatex LIVRO.tex
	evince LIVRO.pdf
mobi:	
	tex4ebook -i -f mobi -c tex4ht EBOOK.tex 	
epub3:
	tex4ebook -i -f epub3 -c tex4ht EBOOK.tex 	
epub:	
	tex4ebook -i -c tex4ht EBOOK.tex 	
EBOOK-pdf:
	pdflatex -halt-on-error EBOOK.tex
	pdflatex -halt-on-error EBOOK.tex
EBOOK-check:
	epubcheck EBOOK.epub
clean:
	-rm *aux *log *tui *toc *.4ct *.4tc *.html *.css *.dvi *.epub *.lg *.ncx *.xref *.tmp *.idv *.opf  
	-rm -rf EBOOK-epub
	-rm -rf EBOOK-epub3
	-rm -rf EBOOK-mobi
git:
		git add .
		git commit -m "direto na linha de comando"
		git push
imageaccess:
		ssh deploy@162.243.216.130
imagepull:
		mkdir img
	  echo "senha: teste13"
		scp deploy@162.243.216.130:~/IMAGENS/1964/* img/
imagepush:
	  echo "senha: teste13"
		scp img/* deploy@162.243.216.130:~/IMAGENS/1964/
