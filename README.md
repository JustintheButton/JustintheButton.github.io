# Personal research homepage

A single-page academic homepage. Plain HTML and CSS, no build step, no JavaScript.

```
index.html        all content
style.css         all styling; colours and widths are tokens at the top
assets/           portrait, favicon, CV
.nojekyll         tells GitHub Pages to serve the files as-is
```

## Edit

Everything to change is in `index.html`, marked with `<!-- EDIT: ... -->` comments.

- **Bio and links**: the `<header class="row intro">` block.
- **Portrait**: add a square photo to `assets/` and point the `.portrait` image at it,
  or delete the image for a text-only header.
- **Research**: copy one `<article class="paper">` block per project, newest first.
  The comment above the first one shows how to add a title link and paper or code links.
- **CV**: save a CV as `assets/cv.pdf`, then add the CV link shown in the comment
  above the links list. Check it for anything you don't want public, such as a phone number.
- **Sections**: each `<section class="row">` is self-contained. Delete or reorder freely.
- **Colours and font**: change the tokens at the top of `style.css`. The page is
  black on white only, with no dark mode. The typeface is EB Garamond, loaded from
  Google Fonts in the `<head>` of `index.html`.

The content comes from your resume. Still to add, each marked with an `EDIT`
comment in `index.html`: a photo, a Scholar link, a CV,
and links or coauthors for the research entries.

## Preview locally

```bash
python3 -m http.server 4173
```

Then open http://localhost:4173.

## Publish on GitHub Pages

1. Create a public repository named `JustintheButton.github.io`.
2. From this folder:

   ```bash
   git init -b main
   git add .
   git commit -m "Personal site"
   git remote add origin https://github.com/JustintheButton/JustintheButton.github.io.git
   git push -u origin main
   ```

3. In the repository, open Settings → Pages and set the source to
   "Deploy from a branch", branch `main`, folder `/ (root)`.

The site appears at `https://justinthebutton.github.io` within a minute or two.
