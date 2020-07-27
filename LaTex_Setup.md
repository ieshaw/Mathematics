# Setting Up LaTeXing for Sublime
## Why
1. LaTeX is the preferred method to create technical documents
2. Sublime is a versitle editor not only for LaTeX but for code as well
3. Skim provides quick compile when interfacing with LaTeXing Package in Sublime

## How
1. Download Sublime
2. Install Latexing
3. Link to Skim

## Install Latexing
To install Latexing, you first need to have Package Control. Fire up Sublime
```
Tools > Install Package Control
```
With this installed, open up Package control
```
Sublime Text > Preferences > Package Control
```
and type in `LaTeXing`.
This should set you up!

## Installing Latex Auto-Complete
Open up Package control
```
Sublime Text > Preferences > Package Control
```
and type in `LaTeXing-CWL`.


## Linking to Skim
[Here](https://jj09.net/latex-with-sublimetext-and-skim/) [Jakub Jedryszek](https://disqus.com/home/forums/jj09/) sets up an quick walk through. I'll re-hash what he put together.
[Skim](https://skim-app.sourceforge.io/) is a PDF renderer that will speed up compiling when writing in LaTeX; at the website, download the package.
Once downloaded, open up Skim.
Navigate to
```
Preferences > Sync > Preset > Sublime Text
```
Now every time you build (cmd + B)[on Mac], Skim will render your Tex page in a PDF rather quickly, whil also saving the new PDF and the Tex files.

## Additional Preferences
Personally my settings are set as so for Sumblime.
```
Sublime Text > Preferences > LaTeXing > Settings - User
​
{
    "log": true,
    "output_directory": true,
    "partial_build": true,
    "tikz": true,
    "tikz_create_pdf": true,
    "show_minimap": false
}
```

## Help Starting Out
Here is a little TeX to help you start out with your first Document
```
\documentclass{article}
\usepackage{graphicx,fancyhdr,amsmath,amssymb,amsthm,subfig,url,hyperref}
\usepackage[margin=1in]{geometry}
\usepackage{comment}
\usepackage{framed} 
\usepackage{hyperref}
​
​
\fancypagestyle{plain}{}
\pagestyle{fancy}
\fancyhf{}
\fancyhead[RO,LE]{\sffamily\bfseries\large University}
\fancyhead[LO,RE]{\sffamily\bfseries\large Stochastic PDE Course Name}
\fancyfoot[RO,LE]{\sffamily\bfseries\thepage}
\renewcommand{\headrulewidth}{1pt}
\renewcommand{\footrulewidth}{1pt}
​
\graphicspath{{figures/}}
​
%-------------------------------- Title ----------------------------------
​
​
\title{Class Notes}
\author{You}
​
%--------------------------------- Text ----------------------------------
​
\begin{document}
\maketitle
​
\section{Lecture 1}
​
\subsection{Administrative Info}
\begin{itemize}
    \item Teacher: Some Guy
    \item TA: Other Guy
    \item Class website with lecture notes \url{http://something.com}
    \item Books
    \begin{itemize}
        \item Evans, ``Partial Differnetial Equations'' AMS
        \item Pinchover \& Rubenstien ``Introduction to PDE''
        \item Vasy ``PDEs''. 
    \end{itemize}
​
\end{itemize}
\subsection{Intro}
The simplest PDE you can write is
​
\begin{enumerate}
\item Infinitely many solutions. Any function of the form $u(t,x)=g(x)$ is a solution. So you need to impose condition if you want a unique solution. 
\end{enumerate}
​
\end{document}
```

## Notes About Using Sublime on Mac
You may want to change your default Tex editor to Sublime (I reccomend it!). To do so click on some `.tex` file, go to `Get Info > Open With > Sublime Text > Change All`. Now every time you open a `.tex` file, Sublime will pop up and have your text in there.

## Changing Color Schemes
As noted earlier, Sublime has many cool color schemes. These can be changes at
```
Sublime Text > Preferences > Color Scheme
```
I think `Monokai` is the coolest, but obviously beauty is ine the eye of th beholder.

## Additional Links

[LaTeXing Documentation](https://github.com/LaTeXing/LaTeXing-Documentation/blob/master/intro.md)

