# Beamer template based on OVGU visual styles

## Fork for Scientific working class

I forked [original repository](https://github.com/eriu/beamer-ovgu) for purposes of Scientific working class. Original template is based on the following files [Lehrstuhl für Elektromagnetische Verträglichkeit](http://www.emv.ovgu.de/Forschung+_+Lehre/Richtlinien+und+Vorlagen-media_id-1424.html) and should comply with a design guidelines based on [CD webpages]( http://www.cd.ovgu.de/).

## Installation


Copy folders ```styleOVGU``` and ```logosOVGU``` to the directory ```$TEXMFHOME/tex/latex/local```.

Run ```texhash``` command.

Test if the files are installed properly by issuing ```kpsewhich beamer_eit-en.sty``` that should return the path to the directory with style file.


This guide works for texlive installed under Debian following [these instructions](https://www.tug.org/texlive/debian.html).  You can find your TEXMFHOME directory by running ```kpsewhich -var-value=TEXMFHOME```. Alternatively you can copy the content of the folders *OVGU into your project directory.

### Pdflatex

For using this with pdflatex, you need to copy at least style image, i.e. ```logosOVGU/Signet_EIT_3.eps``` for the style `beamer_eit-en` to the same directory, where your main tex file lives. Otherwise you get an error that *eps file was not found.

If you just need to produce pdf output, I advise using latexmk -pdfps command which should work with files installed by the procedure described in the installation section.

## Usage
In the directory exampleProject, there is a minimal ```[OVGUPresentation.tex](https://github.com/kulvait/beamer-ovgu/blob/master/exampleProject/OVGUPresentation.tex "OVGUPresentation.tex")``` file. It can be compiled by running `make` that uses command `latexmk -bibtex -pdfps OVGUPresentation` to produce pdf presentation.  Or you can simply run `latex  OVGUPresentation`.

Individual styles can be turned on by specifying command such as `\usepackage{beamer_eit-en}` for the following organization units:

* Otto-von-Guericke-Universität (mit Überschriften im Header)
* Fakultät für Maschinenbau
* Fakultät für Verfahrens- und Systemtechnik
* Fakultät für Elektrotechnik und Informationstechnik
* Fakultät für Informatik
* Fakultät für Mathematik
* Fakultät für Naturwissenschaften
* Medizinische Fakultät
* Fakultät für Humanwissenschaften
* Fakultät für Wirtschaftswissenschaften
* Lehrstuhl für Elektromagnetische Verträglichkeit (EMV)

### Options
**Language**

For English please use the "-en" Version e.g. ```\usepackage{beamer_mb-en}```


**Aspect ratio**

* ```\documentclass[aspectratio=43]{beamer}```  4:3 Format
* ```\documentclass[aspectratio=169]{beamer}```  16:9 Format

	
### Screenshoots
Style | package | Screenshot
:---| :---| :---|
OVGU| ```\usepackage{beamer_ovgu}``` | <img src=screenshots/ovgu.png width=189 height=142/>
Maschinenbau <br> mechanical engineering|  ```\usepackage{beamer_mb}``` <br> ```\usepackage{beamer_mb-en}```  | <img src=screenshots/mb.png width=189 height=142/>
Verfahrens- und Systemtechnik <br> process and system engineering|  ```\usepackage{beamer_vst}``` <br> ```\usepackage{beamer_vst-en}```   | <img src=screenshots/vst.png width=189 height=142/>
Elektrotechnik und Informationstechnik <br> electrical engineering and information technology|  ```\usepackage{beamer_eit}``` <br>```\usepackage{beamer_eit-en}``` | <img src=screenshots/eit.png width=189 height=142/>
Informatik <br>computer science|  ```\usepackage{beamer_inf}``` <br>```\usepackage{beamer_inf-en}```  | <img src=screenshots/inf.png width=189 height=142/>
Mathematik <br> mathematics|  ```\usepackage{beamer_ma}``` <br>```\usepackage{beamer_ma-en}```  | <img src=screenshots/ma.png width=189 height=142/>
Naturwissenschaften <br> natural science|  ```\usepackage{beamer_nat}``` <br>```\usepackage{beamer_nat-en}```  | <img src=screenshots/nat.png width=189 height=142/>
Medizin <br> medicine|  ```\usepackage{beamer_med}``` <br>```\usepackage{beamer_med-en}```  | <img src=screenshots/med.png width=189 height=142/>
Humanwissenschaften <br> human science|  ```\usepackage{beamer_hw}``` <br>```\usepackage{beamer_hw-en}```  | <img src=screenshots/hw.png width=189 height=142/>
Wirtschaftswissenschaften <br> economics and management|  ```\usepackage{beamer_ww}``` <br> ```\usepackage{beamer_ww-en}```  | <img src=screenshots/ww.png width=189 height=142/>
Elektromagnetische Verträglichkeit |  ```\usepackage{beamer_emv}```  | <img src=screenshots/emv.png width=189 height=142/>

