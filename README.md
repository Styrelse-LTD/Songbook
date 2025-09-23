# The innoficial songbook for the Line associations at Mäladalens University
To compile this work we suggest using [Visual Studio Code](https://code.visualstudio.com/) and the extension [LaTeX Workshop](https://github.com/James-Yu/LaTeX-Workshop) Along with [Miktex](https://miktex.org/download).

Setup.sty contains several functions and packages used throughout the work. The important ones are shown off in either main.tex or in Example.tex

AlphaBetatoc.py orderes the subsections in main.toc. Needs to be run after the main builder and comes into effect after the next build.

To set this up automatically you can add this behaviour into the [LaTeX Workshop](https://github.com/James-Yu/LaTeX-Workshop) settings.json. 

Add the tool

{
    "name": "Python Script to Sort Table of Contect",
    "command": "python",
    "args": [
    "%DIR%/AlphaBetatoc.py",
    ],
    "env": {}
}

and the recipe (Note place this first in the list to make it default)

{
    "name": "pdfLaTeX+Python+pdfLaTeX",
    "tools": [
    "pdflatex",
    "Python Script to Sort Table of Contect",
    "pdflatex",
    ]
}

https://booksfactory.se Settings:

Utfall i inlaga: inlaga innehåller utfall - lägg utfallet till formatet
  Rygg: rak
  Inlagas trycktyp: ekonomisk färg
  Grad av färgtäckning: låg täckning: text + diagram
  Papper, svart-vita sidor: Offset 90g/m2
  Papper, färgsidor: Offset 90g/m2
  Bindning av inlaga: inlaga limmat med pur-lim
  Kapitälband: vit
  Märkband: vit
  Omslagstyp: Pärmöverdrag vid bindning
  Omslagets typ: https://panta.com.pl/okleiny-papierowe/942-geltex-reflejos-125-g-m2-kolor-amatista.html
  Tryck på pärmöverdrag: rygg och omslagets framsida
  Omslagstryck i färg: vit
  Bindningspapp: 3 mm
  Laminering: gäller ej
  UV lack på omslag: gäller ej
  Platt metallic foliering på omslag: gäller ej
  3D metallic foliering på omslag: gäller ej
  Skyddsomslag: ingen
  UV lack på skyddsomslaget: gäller ej
  Platt metallic foliering på skyddsomslag: gäller ej
  3D metallic foliering på skyddsomslag: gäller ej
  Rundade omslags hörn: nej
  Rundade hörn på inlaga: nej
  För och eftersättsblad: Standard färgpapper för att matcha inlagan
  Tryck av för och eftersättsblad: Nej
  Tryck på försättsblad: Inga
  Tryck på eftersättsblad: Inga
  Färgtryck på inlagans kanter: nej
  Parametrar:
     Bredd: 111 mm
     Höjd: 154 mm
     Antal färgsidor: 346
     Antal svart-vita sidor: 0
     Antal exemplar: 100
     Färgsidor: Samtliga
