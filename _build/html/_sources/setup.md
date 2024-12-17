# Setup

If you have Python, skip to [link]().

## Python Setup

Install python here.

Check that python was correctly installed by running the following in terminal (MacOS) or Command Prompt/Powershell (Windows).

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

## Jupyter book setup