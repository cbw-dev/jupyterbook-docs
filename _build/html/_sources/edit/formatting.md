# Formatting Your Content

```{admonition} Preface
:class: tip
Jupyter Book has **very thorough** documentation on how to use it. There are many helpful articles and guides to edit it. The good thing is that there is plenty of different forms of documentation, such as in-depth articles and summary/reference pages. Additionally, Jupyter Book has many wonderful and helpful ways to customize wesbites built with it!

The only downside is that there is A LOT of documentation, which can make it slightly hard to get through and find exactly what you want.

However, it is very through and clear, so <a href="https://jupyterbook.org/" target="_blank">check it out</a> for more information, or if you just want to customize more!
```

## Formatting Stuff (Nia please do this)

https://jupyterbook.org/en/stable/content/index.html

## Specific CBW Styling

### PDFs

The way Jupyter Book hosts PDFs must be in the following way. 

- **The only thing you should change is the name of the PDF. Keep the file address the same!**
- You must put the PDF into _build/_images/
    - This is the only time you should be interacting with the _build folder

<!-- NIA: This is sort of a bug, but it works -->

```html
<iframe src="../_images/sample-pdf.pdf" width="100%" height="600px">
  Your browser does not support PDFs. <!-- This will appear as alt text (or at least it should) -->
</iframe>
```

<iframe src="../_images/sample-pdf.pdf" width="100%" height="600px">
  Your browser does not support PDFs. <!-- This will appear as alt text (or at least it should) -->
</iframe>

### Embedding YouTube Videos

YouTube generates HTML code to insert YouTube videos into your pages! You should specifically edit the width and height (what you edit it to is up to you). CBW recommends that {width="100%"}.

How to get the HTML Code:

1. Go to the YouTube video you want to embed.
2. Click "Share", which is below the video.
3. Click the `< > Embed` symbol. 
4. Select your desired options and press copy.
5. Paste the code into your .Rmd file.
6. Edit the width and height options.
7. Done!

An example of a YouTube video inserted into a Bookdown page is shown below!

<iframe width="100%" height="440px" src="https://www.youtube.com/embed/MwsGSgybBVU?list=PL3izGL6oi0S_e5T8qx-74WRaMR5K5U8V5" title="Infectious Disease Genomic Epidemiology 2024 | 1: Introduction to Genomic Epidemiology" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## TIP: Markdown Not Working/Not Enough? Use HTML!

Since inevitably, we end up creating HTML files, we can just put HTML code into our files instead! Use HTML/CSS formatting when MyST markdown isn't enough!

Here are some examples:

1.  Markdown has no formatting options for underlining. Hence, underline text in a .Rmd file with the following HTML syntax:

    ```         
    <u> underlined text</u>
    ```

    <u> underlined text</u>

2.  Jupyter Book currently renders to-do lists incorrectly. Instead, you can use the following HTML code:

    ```         
    <div style="list-style-type: none;">
      <label><input type="checkbox"> check box</label><br>
    </div>
    ```

    <div style="list-style-type: none;">
      <label><input type="checkbox"> check box</label><br>
    </div>


## Cheat Sheet

Here is a massive cheat sheet for MyST syntax provided by Jupyter Book: https://jupyterbook.org/en/stable/reference/cheatsheet.html