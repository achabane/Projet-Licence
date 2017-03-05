Compilation du rapport
 Commande personnalisé de compilation. %.tex est à remplacer par le nom de fichier si la compilatation se fait en ligne de commande.

pdflatex -shell-escape -synctex=1 -interaction=nonstopmode %.tex| makeindex -s %.ist -t %.glg -o %.gls %.glo|makeindex %.glo -t %.glg -s %.ist -o %.gls | pdflatex -shell-escape -synctex=1 -interaction=nonstopmode %.tex|evince %.pdf
