# Build instructions

```shell
xelatex -interaction=nonstopmode 'ace.tex'
biber 'ace.bcf'
xelatex -interaction=nonstopmode 'ace.tex'
xelatex -interaction=nonstopmode 'ace.tex'
```
