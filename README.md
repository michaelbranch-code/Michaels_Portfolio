# Michael's Portfolio

This is a minimal Jekyll portfolio site for GitHub Pages. It uses plain HTML and CSS, with no React, no JavaScript framework, no npm setup, and no custom build step.

## Enable GitHub Pages

1. Push this repository to GitHub.
2. Open the repository on GitHub.
3. Go to Settings → Pages.
4. Under "Build and deployment", choose "Deploy from a branch".
5. Select the `main` branch.
6. Select the `root` folder.
7. Save the settings.

GitHub Pages will build the Jekyll site automatically when you push changes.

## Run Locally

To preview the site on your computer, install Jekyll and run the local server:

```bash
gem install bundler jekyll
jekyll serve
```

On some computers, especially macOS systems using the built-in Ruby, `gem install bundler jekyll` may ask for permission or appear to get stuck. If it fails with a permissions error, you may need:

```bash
sudo gem install bundler jekyll
```

If you use `sudo`, your computer will ask for your password before installing the gems.

Then open this address in your browser:

```text
http://localhost:4000
```

You can stop the server by pressing `Control + C` in the terminal.

If you want to use the same general Jekyll environment as GitHub Pages, you can install the GitHub Pages gem instead:

```bash
gem install github-pages
jekyll serve
```

## Edit Pages

The main pages are:

- `index.html`
- `about.html`
- `projects.html`
- `contact.html`

Each page uses Jekyll front matter at the top:

```html
---
layout: default
title: Page Title
---
```

Edit the HTML below the front matter to change the page content.

## Add A New Page

1. Create a new `.html` file, such as `resume.html`.
2. Add front matter at the top:

```html
---
layout: default
title: Resume
---
```

3. Add your page content using regular HTML.
4. Add a link to the new page in `_includes/nav.html`.

## Why `relative_url` Is Used

GitHub Pages sites can be published at a project URL such as:

```text
https://username.github.io/repository-name/
```

The `relative_url` filter helps links and assets work correctly when the site is published inside a repository path. For example:

```html
{{ '/assets/styles.css' | relative_url }}
```

This keeps links working both locally and on GitHub Pages.
