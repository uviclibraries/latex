---
layout: default
title: 2-Inserting Tables and Figures
nav_order: 3
parent: Workshop Activities
---

# Inserting Tables and Figures

If you and your group have any questions, or get stuck as you work through this in-class exercise, please ask the instructor for assistance. Have fun!

1.  Using Chapter 4 (pg. 17-18) [https://goo.gl/MFp45A](https://goo.gl/MFp45A){:target="_blank"} for reference, write code to produce the tables below:
2.  Insert and refer figures
    Download the figure first: [https://goo.gl/YH3R4n](https://goo.gl/YH3R4n){:target="_blank"}. Upload the picture by clicking “PROJECT” on the top of the page, and then “Files... → Computer”. Then, type `\usepackage{graphicx}` directly after the `\documentclass[a4paper,12pt]{article}` and above the `\begin{document}`. Type the following codes below the `\begin{document}` :-).
    Insert a figure:

    ```
    \begin{figure}[h!]
    \centering
    \includegraphics[width=1\textwidth]{uvic.png}
    \caption{This is caption}
    \label{fig:uvic}
    \end{figure}
    ```
    Type the following to refer the figure.
    Example: `Please see Figure~\ref{fig:uvic}`.

3.  Create a three-line table (research paper style)
    First type: `\usepackage{booktabs}` after `\usepackage{graphicx}` after the \documentclass[a4paper,12pt]{article} and above the \begin{document}. Then type the following codes below the \begin{document}:

    ```
    asdf
    ```

4.  asdf
5.  asdf
6.  asdf

    ```
    asdf
    ```

7.  asdf

    ```
    asdf
    ```

[NEXT STEP: Typing Math Equations](act-3.html){: .btn .btn-blue }
