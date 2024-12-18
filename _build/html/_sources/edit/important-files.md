# What Do You Need to Edit?

There are 2 main files that control your website:

#### 1. `_config.yml`

The `_config.yml` file defines a lot of actions that Jupyter Book does when building your website.

Before starting to customize your website, update the following things:

- repository > url [RC]
- title
- author

Feel free to add more options as you customize your website. 

A thorugh summary of many options in a `_config.yml` is summarized <a href="https://jupyterbook.org/en/stable/customize/config.html" target="_blank">here</a>.

#### 2. `_toc.yml`

TOC, or the Table of Contents, is how the primary sidebar is defined.

```{warning}
You may run into errors trying to change your landing page (`root:`) so that it is not called "intro.extension"!
```

Our sidebars are broken up into parts (using `part:`). The title of each part is determined by `caption:`. `chapters:` defines which pages follow this part, and are written as `parent_folder/file_name`. Write these addresses relative to where your project folder (since _toc.yml is usually kept there). **The extension is not included** and there may be errors if the extention is included. Hence, no 2 files can have the same name in the same folder, even if they have different extentions. (Ensure no files are named "intro.extension", since this is reserved for the landing page.) Similairly, the same file can not be referenced twice across the table of contents.

```{important}
Note that the indentation of _toc.yml is important and may cause your website to not build if it is incorrect.
```

To create a dropdown sidebar title, we use <a href="https://jupyterbook.org/en/stable/structure/configure.html" target="_blank">sections</a>.

<!-- NIA: Clarify and add more options? -->

For more customization documentation for the table of contents, visit the official Jupyter Book documentation pages: <a href="https://jupyterbook.org/en/stable/structure/toc.html" target="_blank">Structure the Table of Contents</a> and <a href="https://jupyterbook.org/en/stable/structure/configure.html" target="_blank">Configure the Table of Contents</a>.

## Other Files

Your other files can consist of .Rmd, .md and .ipynb files. <!-- and more file types? -->

<!-- NIA: Please add on here -->