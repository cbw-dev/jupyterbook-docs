(installations)=
# Installations

## VSCode

If you have VSCode, skip to [installing Python](python-install).

Download Visual Studio Code (VSCode) <a href="https://code.visualstudio.com/download" target="_blank">here</a>. CHoose the download package according to your operating system.

Install with default settings.
<!-- Not sure if default settings work, but they probably should, need to test -->

(python-install)=
## Install Python

If you have Python, skip to [](content:references:jupyter-book-setup).

```{admonition} Notebook Execution Incompatibility for Windows
:class: warning

There is an incompatiablity when using **Python 3.8**. Click <a href="https://jupyterbook.org/en/stable/advanced/windows.html#working-on-windows" target="_blank">here</a> for more information.
```

Install Python <a href="https://www.python.org/downloads/" target="_blank">here</a>.

Check that python was correctly installed by running the following in Terminal (Linux/MacOS) or Command Prompt/Powershell (Windows).

```bash
python --version
```

The output should look like:

```
Python 3.13.0
```

`````{admonition} command not found: python
:class: warning
You might be running a very recent version of python. [ADD MORE DETAILS]

Try running ```python3 --version``` instead and you should get the above output.
`````

Jupyter Book specifically requires pip, the package installer for Python, which will install the Jupyter Book package. Check that you have pip installed by running the following command.

```bash
pip --version
```
`````{admonition} command not found: pip
:class: warning
If ```python3 --version``` worked for you, you also need to run ```pip3 --version``` to check your pip!
`````

Your output should look something like:
```
pip 24.3.1 from /Library/Frameworks/Python.framework/Versions/3.13/lib/python3.13/site-packages/pip (python 3.13)
```

Now that we have Python and pip properly installed, we can download and install Jupyter Book!

(content:references:jupyter-book-setup)=
## Install Jupyter Book

Run the following command (and if you needed `pip3` before, use `pip3` here):

```bash
pip install -U jupyter-book
```

Check that you installed Jupyter Book correctly by running:
```bash
jupyter-book --help
```
which will help explain the `jupyter-book` command to you if it was downloaded properly!

You should see:
```
Usage: jupyter-book [OPTIONS] COMMAND [ARGS]...

  Build and manage books with Jupyter.

Options:
  --version   Show the version and exit.
  -h, --help  Show this message and exit.

Commands:
  build   Convert your book's or page's content to HTML or a PDF.
  clean   Empty the _build directory except jupyter_cache.
  config  Inspect your _config.yml file.
  create  Create a Jupyter Book template that you can customize.
  myst    Manipulate MyST markdown files.
  toc     Command-line for sphinx-external-toc.
```

If you are having some difficulty downloading, try restarting your Terminal/Command Prompt/Windows PowerShell and ensuring your previous installations were done properly.

## Install ghp-import 

ghp-import is a Python library that makes creating a website using GitHub pages super easy! We'll explain this more later, for now, run the command:

```
pip install ghp-import
```

Again, run `pip3` if you had to before.

## Install Git

Git is a tool that will help us with version control when editing your workshop. Linux and macOS computers tend to have Git installed. Windows computers must install Git. However, make sure to double check if you already have Git, so that you don't have to install it again! **Check if you have Git** by running this command in terminal/command prompt:

```bash
git --version
```

If your output looks like `git version X.X.X ...`, you already have git! Move onto step 4!

However, if your output says "Git is not recognized" or a similar statement (such as the one provided below), you do not have Git, so you must install it as well.

```
'git' is not recognized as an internal or external command,
operable program or batch file.
```
    
<a href="https://github.com/git-guides/install-git#install-git-on-mac" target="_blank">**Installing Git on macOS**</a>
    
- When you ran `git --version`, it will have prompted you to install Git. Follow these instructions.
    
<a href="https://github.com/git-guides/install-git#install-git-on-windows" target="_blank">**Installing Git on Windows**</a>

- Go to the <a href="https://posit.co/download/rstudio-desktop/#:~:text=AND%20INSTALL%20R-,2%3A%20Install%20RStudio,-DOWNLOAD%20RSTUDIO%20DESKTOP" target="_blank">Git for Windows installer</a> and download Git. Then, install it with all the default settings.

Click here for instructions on <a href="https://github.com/git-guides/install-git#install-git-on-windows" target="_blank">**installing Git on Linux**</a>.
    

```{note}
Check that your install worked! Re-run "git -\-verison" and check that you get your git version! (On Windows, this may look like "git version 2.47.1.windows.1").
```

```{tip}
If you installed Git while having a Command Prompt/Windows PowerShell window open, close this window and open a new one to run "git -\-version". This acts as a refresher to Command Prompt/Windows PowerShell.
```