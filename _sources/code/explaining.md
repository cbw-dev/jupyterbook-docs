# [DEV HELP FILE]

```{important}
Ok I don't think this is should stay in the official documentation, but this may help explain things to Nia
```

First, add

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

