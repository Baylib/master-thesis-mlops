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

```bash
dataops-pipeline/
├── dags/
│ ├── dag-x.py
│ ├── dag-y.py
│ ├── requirements.txt
│ └── config.yaml
├── images/ # steps
│ ├── kubeflow-pipeline/
│ │ ├── Dockerfile
│ │ ├── main.py
│ │ └── config.yml
│ └── step-x-definition/
│ ├── main.py
│ └── config.yml
└── README.md
```
```bash
model-api-helm/
├── helm/
│ ├── templates
│ ├── Chart.yaml
│ └── values.yaml
├── images/
│ ├── model-api/
│ │ ├── Dockerfile
│ │ ├── main.py
│ │ └── requirements.txt
└── README.md
```