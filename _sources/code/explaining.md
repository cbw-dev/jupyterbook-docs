# [DEV HELP FILE]

```{important}
Ok I don't think this is should stay in the official documentation, but this may help explain things to Nia
```

## SEE JULIA_LABNOTES PAGES 27 - 30

Install stuff for jupytext:

```
pip3 install jupytext
pip3 install --upgrade pip
```

Add

```yaml
sphinx:
  config:
    nb_custom_formats:
        .Rmd:
            - jupytext.reads
            - fmt: Rmd
```

to the bottom of the _config.yml file. 

See here (https://jupyterbook.org/en/stable/file-types/jupytext.html) for more explanation?

Code for installing a R kernel:

- do this in R terminal

```
install.packages("devtools")
devtools::install_github("IRkernel/IRkernel")
IRkernel::installspec()
```


Initialize the md file as a Jupytext MyST Markdown with this command 

```
jupyter-book myst init mymarkdownfile.md --kernel kernelname
```