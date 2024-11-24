# master-thesis-mlops

## Install latex
```bash
sudo apt install texlive
sudo apt install texlive-latex-extra
mkdir ~/texmf 
cd ~/texmf
tlmgr init-usertree
tlmgr install minted 
# tlmgr install ...
sudo apt-get install python3-pygments 
sudo apt-get install texlive-bibtex-extra biber
```

## Compile pdf
```bash
mkdir ./out
pdflatex -file-line-error -interaction=nonstopmode -synctex=1 -output-format=pdf -output-directory=./out -shell-escape main.tex
biber out/main
pdflatex -file-line-error -interaction=nonstopmode -synctex=1 -output-format=pdf -output-directory=./out -shell-escape main.tex
```