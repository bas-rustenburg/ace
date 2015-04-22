# Build instructions
[![PDF Status](https://www.sharelatex.com/github/repos/bas-rustenburg/ace/builds/latest/badge.svg)](https://www.sharelatex.com/github/repos/bas-rustenburg/ace/builds/latest/output.pdf)
```shell
xelatex -interaction=nonstopmode 'ace.tex'
biber 'ace.bcf'
xelatex -interaction=nonstopmode 'ace.tex'
xelatex -interaction=nonstopmode 'ace.tex'
```
