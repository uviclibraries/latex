---
layout: default
title: 2-Inserting Tables & Figures
nav_order: 3
parent: Workshop Activities
customjs: http://code.jquery.com/jquery-1.4.2.min.js
---

# Inserting Tables and Figures

If you and your group have any questions, or get stuck as you work through this in-class exercise, please ask the instructor for assistance. Have fun!

1.  Immediately below `\end{enumerate}` type `\newpage`

2.  **Using Chapter 4 (pg. 17-18)** [https://goo.gl/MFp45A](https://goo.gl/MFp45A){:target="_blank"} for reference, write code below your most recent `\newpage` line to produce the tables below:**

    <img src="images/act-2/table1.png" alt="table 1" style="width:500px;">
    
    <button onclick="toggle('sol')">**Show/Hide Solution**</button>
    <div id="sol" style="display: none">
    <img src="images/act-2/solution1.png" alt="table solution" style="width:480px;">
    </div>
3.  Immediately below the last `\end{tabular}` type another `\newpage`

4.  **Insert and refer figures**<br>
    Download the figure first: [https://goo.gl/YH3R4n](https://goo.gl/YH3R4n){:target="_blank"}. Upload the picture by clicking “PROJECT” on the top of the page, and then “Files... → Computer”. Then, at the top of your document, type `\usepackage{graphicx}` directly after the `\documentclass[a4paper,12pt]{article}` and above the `\begin{document}`. Type the following codes below your most recent `\newpage`<br>
    
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
    
    <img src="images/act-2/refer-fig.png" alt="refer figures" style="width:600px;">

5.  Immediately below the line referring the figure, type another `\newpage`

6.  **Create a three-line table (research paper style)**<br>
    
    <img src="images/act-2/refer-table.png" alt="refer table" style="float:right;width:240px;">
    
    First type: `\usepackage{booktabs}` and `\usepackage{graphicx}` at the top of your document after the `\documentclass[a4paper,12pt]{article}` and above the `\begin{document}`. Then type the following codes below the most recent `\newpage`<br>

    ```
    \begin{table}[htbp]
    \centering
     \caption{\label{tab:test}Caption for table}
     \begin{tabular}{lcl} 
      \toprule
      Model & Adjusted $R^2$ & p-value \\
      \midrule
     Model1 & 0.6 & 0.01 \\
     Model2 & 0.7 & 0.02 \\
     Model3 & 0.8 & 0.03 \\
      \bottomrule
     \end{tabular}
    \end{table}
    ```
    
    <img src="images/act-2/3line-table.png" alt="three line table" style="width:600px;">

    **Note:** in the `\begin{tabular}{lcl}`, it should type the "**l**" (in short for left) rather than digital number 1 and ‘c’ (in short for center).  {lcl} is used for the column alignment in the table. There are three options for column alignment, namely l (left), c (center) and r (right). You can change this part as you like.

7.  Ensure that the following codes are inserted into your main body, anywhere below the \begin{document} but above the \end{document}.

- **Reference a table** <br>
    Type the following in your paragraph to refer the table: 
    `Please see Table~\ref{tab:test}.`

- **Insert a footnote**<br>
    Type the following:
    `This is the footnote.\footnote{Footnote text.}`

- **Add Verbatim text**

    ```
    Type Quote: Single `Quote', Double ``Quotes''
    \begin{verbatim}
    The verbatim environment
     reproduces every input,
    including  s p a c e s!
    \end{verbatim}
    ```
    
    <img src="images/act-2/verbatim.png" alt="verbatim" style="width:600px;">

[NEXT STEP: Typing Math Equations](act-3.html){: .btn .btn-blue }

<script>  
    function toggle(input) {
        var x = document.getElementById(input);
        if (x.style.display === "none") {
            x.style.display = "block";
        } else {
            x.style.display = "none";
        }
    }
</script>