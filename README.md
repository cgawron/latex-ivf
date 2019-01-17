ifv.sty ist ein LaTeX-Paket zur Erzeugung von Lehrbriefen für das Institut für Verbundstudien NRW

## Installation unter OpenSuse Leap 42.3:

```
sudo su
zypper in texlive-latex
zypper in texlive-sidecap texlive-bytefield texlive-mnsymbol texlive-background texlive-comicneue texlive-idxlayout texlive-menukeys texlive-adjmulticol 
```

Get "Menlo.ttc" and "Courier New.ttf" (e.g. from a Mac) and copy them to the tex directory

change following line:

```
\usepackage{ifv}
```
->
```
\usepackage[localMenloFont]{ifv}
```

## Installation unter Debian 9
```
sudo apt install texlive texlive-sidecap texlive-bytefield texlive-mnsymbol texlive-background texlive-comicneue texlive-idxlayout texlive-menukeys texlive-adjmulticol 
mkdir ~/.fonts
cp tex/fonts/* ~/.fonts
luaotfload-tool -u
```

Übersetzen eines Lehrbriefs mit 
```
latexmk -quiet -pdflatex=lualatex -pdf lehrbrief-vorlage.tex
```