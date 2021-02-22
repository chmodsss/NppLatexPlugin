# NppLatexPlugin for Windows
A hack to build latex files from Notepad++ in Windows

* Clone this repo in a directory of your choice, we will be needing the folder `NppExec` and `miktex_to_latex.bat` file.
* Install [MiKTeX](https://miktex.org/download). (MiKTeX is for building LaTeX files)
* Install [Sumatra PDF](https://www.sumatrapdfreader.org/download-free-pdf-viewer.html). (A light-weight pdf that helps us in preview)
* Copy the `NppExec` folder to Notepad++\plugins directory. (This plugin helps to run our own script)
* Copy the `miktex_to_latex.bat` file to Notepad++ installation directory. (This script helps us to run latex from Npp using miktex)
  * Pay attention to the Sumatra pdf installation path (change the path to where your sumatra pdf has been installed. line 24)
  * Make sure there are NO spaces in the path (Use Progra~2, not Program Files (X86))

Setup is almost done. 
* Now, open the .tex file you wanna run and press F6 to execute.

In the popup box, enter the follow lines

``` 
NPP

"C:\Progra~2\Notepad++\miktex_to_latex.bat" "$(CURRENT_DIRECTORY)" "$(NAME_PART)" "$(NAME_PART).pdf"
```
Change the path of `miktex_to_latex.bat` if its different for you.

* Click on `Save` and enter a name for this script `PdfLatex`
* In Notepad++, go to Plugins->NppExec->Advanced Options. In Associated scripts tab, click on `PdfLatex` and select on Add/Modify to add it.
* Go to Settings-> Shortcut Mapper. Under `plugin commands` tab, search `PdfLatex` and assign a shortcut of your choice like `Shift+Esc`.
* That's it. Now you can save the .tex file and build the .tex file using the shortcut. The built pdf file is generated and previewed using Sumatra Pdf.

## Source Credits: [Nimal's weblog](http://nimal.info/blog/2010/latex-on-windows-with-miktex-and-notepad)
