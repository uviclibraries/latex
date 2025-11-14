---
layout: default
title: 6-Fun with Fonts
nav_order: 7
parent: Workshop Activities
---

# Advanced Fonts with XeLaTeX
If you and your group have any questions, or get stuck as you work through this in-class exercise, please ask the instructor for assistance. Have fun!

XeLaTeX is an alternative compiler to regular LaTeX that supports Unicode text and other modern font formats. That means you can type in any language, and not just in English letters.

Let’s create a new project for this activity in Overleaf.

1.  **Create a new project in Overleaf and choose the first one (Blank paper)**

    <img src="images/act-6/menu.jpg" alt="menu button" style="float:right;width:180px;margin-left:10px;">

2.  **Change compiler**. Click the top left **Menu** button, scroll down to Settings, click the drop down next to Compiler, then select **XeLaTeX**.

<img src="images/act-6/compiler.jpg" alt="compiler" style="width:300px;">

3.  **Replace the original text with the following to set up your title page:**

```
\documentclass[pdf]{article}
\usepackage{fontspec}      

% This sets the default font of the document
\setmainfont{Times New Roman}

% This sets the sans serif font for this document
\setsansfont{Arial}

% This sets the mono font for this document. You can also choose the colour for font (coloud would also work in the above lines)
\setmonofont[Color={4CA6A6}] {Courier New} %4CA6A6 is the hex code for teal.

\title{Fun with Fonts}
\author{Your name here}
\date{\today}
   
\begin{document}
\maketitle

\end{document}
```

<img src="images/act-6/title-page.jpg" alt="title page slide" style="width:500px;">

4. **Change the font**
    Copy and paste the below line between your `\maketitle` and `\end{document}` statements.

```
 This is the default font, Times New Roman.
 % use \sffamily to switch to sans serif font
 \sffamily Here is some text in Arial, a sans serif family font.
 % use \ttfamily to switch to mono font
 \ttfamily Here is some teal text in Courier New, a mono font. 
 % use \rmfamily to go back to default font
 \rmfamily Set back to times new roman
```
<img src="images/act-6/3fonts.png" alt="compiled result with 3 fonts" style="width:600px;">

If you want to explore more fonts covered in the fontspec package, check [this](https://www.overleaf.com/learn/latex/Questions/Which_OTF_or_TTF_fonts_are_supported_via_fontspec%3F){:target="_blank"}.

5. **Add a font package for Japanese, Chinese, or Korean**
    -   Add ```\usepackage{xeCJK}``` to the top of the file with the other ```\usepackage``` statements.
    -   Add ```\setCJKmainfont{IPAMincho}``` below the other font statements
    -   Go to [Google Translate](https://translate.google.com/){:target="_blank"} and translate a phrase from English to Japanese
    -   Copy the Japanese translation into your overleaf document.
    -   Re-compile - you should now see the Japanese text in the pdf.

<img src="images/act-6/xeCJK.png" alt="compiled japanese text" style="width:600px;">

6. **Add a font from outside Overleaf**  
    <img src="images/act-6/download family.png" alt="download family" style="float:right;width:200px; margin-left:10px;">
    -   Go to [Google Fonts](https://fonts.google.com/specimen/Asap){:target="_blank"}  and download the Asap font family files by clicking the **Get Font** button on the top right.
     <img src="images/act-6/upload files.png" alt="uploading files" style="float:right;width:200px; margin-left:10px;">
    - Unzip the downloaded folder. Note that there is a folder called "static" in the downloaded files. You will need the files inside that folder.
    -  Click the top left **folder icon** to make a new folder in Overleaf. Name the folder **AsapFontFiles.** _Note: the folder name is case sensitive!_
    -  Upload the font files (extension .ttf) that are inside the folder "static" into your new Overleaf folder using the **Upload** button on the top left.
    -  Now, you need to tell the package `fontspec` where the font files are/ For that, copy and paste into your document, after the `\package{fontspec}` line.

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

- This is setting the Asap font as the sans serif font for your document. Remember to delete the line that said `\setsansfont{Arial}`, otherwise it will override the determination of Asap as sans serif font.
  
- Try writing some text in the Asap font:
```
\sffamily Now we can type in asap! The Quick Brown Fox Jumps Over the Lazy Dog
```

<img src="images/act-6/asapfont.png" alt="asap font result" style="width:600px; margin-left:10px;">

7. **Add a Unicode font**   
    -   In the top of the document, replace ```\setmainfont{Times New Roman}``` with ```\setmainfont{Doulos SIL}``` 
    -   Doulos SIL is a [Unicode](https://en.wikipedia.org/wiki/Unicode){:target="_blank"} font family.  Now you can use unicode characters in your LaTeX document!
    -   Type some IPA (International Phonetic Alphabet) characters using [this browser IPA keyboard](https://keymanweb.com/#und-latn,Keyboard_sil_ipa){:target="_blank"} and [this reference guide](https://help.keyman.com/keyboard/sil_ipa/1.8.6/sil_ipa){:target="_blank"}, then copy and paste them into your Overleaf document. 
        -  _If you have a unicode keyboard installed on your computer, you can type directly in your Overleaf document_.
    -   Type out these [SENĆOŦEN](https://www.languagegeek.com/salishan/sencoten.html){:target="_blank"} words using the [SENĆOŦEN Keyboard](https://keyman.com/keyboards/fv_sencoten){:target="_blank"}, then copy-paste them into a table like the image below.
        -   _Hint: use ' to add top accent, - for dash accent and _ for low line accent._

        <img src="images/act-6/sencoten.png" alt="sencoten words" style="width:500px;">

    <button onclick="toggle('sol')">**Show/Hide Solution**</button>
    <div id="sol" style="display: none">
    In the keyboard: SENC'OT-EN, MA'LEXEL-, SXIMEL-EL-, W_JOL-EL-P. 

    In Overleaf:
    <img src="images/act-6/sencotentable.png" alt="table in overleaf" style="width:600px;">
    </div>
        
8. **OPTIONAL: Using Tipa, a phonetic alphabet font**
    -   Tipa is an older way to use IPA symbols in LaTeX before unicode was supported - you can skip this part of the activity if you like.
    -   Make a new folder called **TipaFontFiles**
    -   Download the [tipa font files](https://ctan.org/tex-archive/fonts/tipa/tipa){:target="_blank"}. Click on "Download the contents of this package" button, then unzip the folder. You will need the files inside the folder tipa > type1.
    -   Tipa has a lot of different font options, but to keep things simple upload roman (tipa8), bold (tipab10), italic (tipasl8), and bold italic (tipasb10) to your new folder.
    -  Copy and paste:
```
\setsansfont{tipa}[
  Path=./TipaFontFiles/,
  Scale=0.9,
  Extension = .pfb,
  UprightFont=*8,
  BoldFont=*b10,
  ItalicFont=*sl8,
  BoldItalicFont=*sb10
]
```
    - Remember to delete the old text that set Asap as the sans serif font.
    - Use [pages 14 and 36-56 of the Tipa manual](https://muug.ca/mirror/ctan/fonts/tipa/tipa/doc/tipaman.pdf){:target="_blank"}  to type up some phonetic symbols.
    - Try to write out the IPA pronunciation for Lekwungen: <br>
    <img src="images/act-6/lekwungen.png" alt="asap font result" style="width:100px;">
    - Solution: 
    ```\sffamily l@\textvbaraccent{k}\textsuperscript{w}@N@n```

9.  If you want more resources, here are some helpful links:
    -   More [help on XeLaTeX]( https://www.overleaf.com/learn/latex/XeLaTeX){:target="_blank"} 
    -   More [help on font commands](https://ctan.mirror.globo.tech/macros/unicodetex/latex/fontspec/fontspec.pdf){:target="_blank"} 

**Congratulations - now you can use fonts with XeLaTeX!**

[NEXT STEP: Earn a Workshop Badge](informal-credentials.html){: .btn .btn-blue }

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
