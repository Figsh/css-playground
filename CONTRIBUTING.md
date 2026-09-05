# Contributing

This is a beginner-friendly project. That means the bar to contribute is low on purpose, and questions in your PR description are welcome, not a problem.

## Adding a component

1. Fork the repo and clone it locally.
2. Create a new branch:
   ```bash
   git checkout -b add-my-component
   ```
3. Open `index.html`. Find the `<!-- COMPONENT GALLERY -->` section near the bottom of the `<main>`.
4. Copy one of the existing `<div class="component">` blocks and change it into your own. Give it a `<h3>` with a short name for what it is.
5. Open `css/style.css`. Find the `/* COMPONENT STYLES */` section at the bottom of the file. Add your own comment header and your CSS underneath it, following the pattern already there.
6. Save both files, open `index.html` in your browser, and check that your component looks right and doesn't break anything above or below it.
7. Commit and push:
   ```bash
   git add .
   git commit -m "Add [your component name]"
   git push origin add-my-component
   ```
8. Open a pull request. In the description, a sentence or two on what you made and, if you want, what you learned making it. A screenshot is welcome but not required.

## Ground rules

- Plain HTML and CSS only. No frameworks, no build step, no JavaScript required (a little JS is fine if your component genuinely needs it, but it should still work if someone just opens the HTML file directly).
- Keep your component visually contained. It shouldn't rely on styles from somewhere else in the file, or break the layout around it.
- Don't remove or rewrite someone else's component to add yours. Add alongside.
- Comment your CSS a little. Not a lot, just enough that someone reading it for the first time can follow what each rule is doing.

## Reporting a bug or suggesting an idea

Open an issue. "This looks broken on mobile" or "it would be cool if there was a form example" are both completely fine issues to open.
