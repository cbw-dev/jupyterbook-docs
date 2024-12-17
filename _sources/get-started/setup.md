(installations)=
# Installations

If you have Python, skip to [](content:references:jupyter-book-setup).

`````{admonition} Notebook Execution Incompatibility for Windows
:class: warning

There is an incompatiablity when using **Python 3.8. Click <a href="https://jupyterbook.org/en/stable/advanced/windows.html#working-on-windows" target="_blank">here</a> for more information.

`````

## Python Setup

Install Python <a href="https://www.python.org/downloads/" target="_blank">here</a>.

Check that python was correctly installed by running the following in Terminal (Linux/MacOS) or Command Prompt/Powershell (Windows).

```
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

```
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
## Jupyter Book Installation

Run the following command (and if you needed `pip3` before, use pip3 here):

```
pip install -U jupyter-book
```