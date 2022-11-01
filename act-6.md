---
layout: default
title: 6 - Fun with Fonts [UNDER CONSTRUCTION]
nav_order: 7
parent: Workshop Activities
---

# Advanced Fonts with XeLaTeX
If you and your group have any questions, or get stuck as you work through this in-class exercise, please ask the instructor for assistance. Have fun!

XeLaTeX is an alternative compiler to regular LaTeX that supports Unicode text and other modern font formats.

Let’s create a new project for this activity in Overleaf.

1.  **Create a new project and choose the first one (Blank paper)**

<img src="images/act-6/menu.jpg" alt="menu button" style="float:right;width:180px;margin-left:10px;">

2.  **Change compiler**. Click the top left **Menu** button, scroll down to Settings, click the drop down next to Compiler, then select **XeLaTeX**.

    <img src="images/act-6/compiler.jpg" alt="compiler" style="width:300px;">

3.  **Replace the original text with the following to set up your title page:**

    ```
    \documentclass[pdf]{article}
    \usepackage{fontspec}       
    \setmainfont{Times New Roman}
    \setsansfont{Arial}
    \title{Fun with Fonts}
    \author{Your name here}
    \date{\today}
   
    \begin{document}
    \maketitle

    \end{document}
    ```

    <img src="images/act-6/title-page.jpg" alt="title page slide" style="width:600px;">
4. **Change the font**
    Type some text in a different font:
    ```
    \sffamily Here is some text in Arial, a sans serif family font.
    ```

[NEXT STEP: Earn a Workshop Badge](informal-credentials.html){: .btn .btn-blue }
