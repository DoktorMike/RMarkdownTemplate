# RMarkdownTemplate

My RMarkdown base template which is so far targeted towards producing automated reports in RMarkdown using ioslides. This has been a hassle for me for a couple of years and that's why I created this now for my own peace of mind. Please feel free to use it. Pull requests are also welcome.

## How to use it

1. clone this repository
2. make a folder somewhere on your machine where you want to keep your new document
3. copy template.Rmd, styles.css and logo.png from the repository you cloned into your newly created folder
4. fire up RStudio and make a new project in that folder
5. press knit and enjoy

## Doing a two column layout

Although ioslides in RMarkdown shoule work with two column layouts by adding the ".columns-2" attribute next to the header it has never worked for me when printing the HTML to PDF which is a certain requirement in many consultancy and reporting businesses. The recommendation is to do the following:

```markdown
## Hello {.columns-2}

- My first column

- My second column

```

However, in this template to make sure we produce correct HTML that prints like you would expect it to we instead do this:

```markdown
## Hello {.columns-2}

<div style="float: left; width: 50%;">
- My first column
</div>

<div style="float: right; width: 50%;">
- My second column
</div>
```
