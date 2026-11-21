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

- **Bio and links**: the `<header class="row intro">` block. The email, GitHub and
  LinkedIn links are icons; change where one goes by editing its `href`.
- **Portrait**: add a square photo to `assets/` and point the `.portrait` image at it,
  or delete the image for a text-only header.
- **Research**: copy one `<article class="paper">` block per project, newest first.
  The title and the "PDF" link both point at the write-up.
- **CV**: save a CV as `assets/cv.pdf`, then add the CV link shown in the comment
  above the links list. Check it for anything you don't want public, such as a phone number.
- **Sections**: each `<section class="row">` is self-contained. Delete or reorder freely.
- **Colours and font**: change the tokens at the top of `style.css`. The page is
  black on white only, with no dark mode. The typeface is EB Garamond, loaded from
  Google Fonts in the `<head>` of `index.html`.

The content comes from your resume. Still to add: a photo, a Scholar link,
a CV, and coauthors for the research entries.

## Preview locally

```bash
python3 -m http.server 4173
```

Then open http://localhost:4173.

## Publish on GitHub Pages

1. On GitHub, create a public repository named `JustintheButton.github.io`.
   Leave it empty: no README, licence or .gitignore.
2. This folder is already a git repository with that remote set, so from here run:

   ```bash
   git push -u origin main
   ```

3. In the repository, open Settings → Pages and set the source to
   "Deploy from a branch", branch `main`, folder `/ (root)`.

The site appears at `https://justinthebutton.github.io` within a minute or two.
