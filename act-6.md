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
5. **Add a font package for Japanese, Chinese, or Korean**
    -   Add \usepackage{xeCJK} to the top of the file
    -   Add \setCJKmainfont{IPAMincho} below the other font statements
    -   Go to [Google Translate](https://translate.google.com/) and translate a phrase from english to Japanese
    -   Copy the Japanese translation into your overleaf document.
    -   Re-compile - you should now see the Japanese in the pdf.

5. **Add a font from outside Overleaf**  
    -   Go to [Google Fonts](https://fonts.google.com/specimen/Asap) and download the Asap font files
    -  Make a new folder in Overleaf called "AsaFontFiles"
    -  Upload the font files into the new folder
    -  Copy and paste into your document:

```

\setsansfont{Asap}[
    Path=./AsapFontFiles/,
    Scale=0.9,
    Extension = .ttf,
    UprightFont=*-Regular,
    BoldFont=*-Bold,
    ItalicFont=*-Italic,
    BoldItalicFont=*-BoldItalic
    ]
```

6. Using a phonetic font
    -   Make a new folder called **TipaFontFiles**
    -   Download the [tipa font files](https://ctan.org/tex-archive/fonts/tipa/tipa/type1)
    -   tipa has a lot of different options, but to keep things simple upload roman (tipa8), bold (tipab10), italic (tipasl8), and bold italic (tipasb10) to your new folder.
    -  Copy and paste:
    ```
    \setromanfont{tipa}[
    Path=./TipaFontFiles/,
    Scale=0.9,
    Extension = .pfb,
    UprightFont=*8,
    BoldFont=*b10,
    ItalicFont=*sl8,
    BoldItalicFont=*sb10
    ]
    ```
    - Use [pages 14 and 36-56 of this reference document](https://muug.ca/mirror/ctan/fonts/tipa/tipa/doc/tipaman.pdf) to type up some phonetic symbols.

**Congratulations - now you know about fonts and LaTeX!**

[NEXT STEP: Earn a Workshop Badge](informal-credentials.html){: .btn .btn-blue }
