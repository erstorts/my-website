# emmettstorts.com

Marketing site for Emmett Storts' freelance data science practice. Jekyll on GitHub Pages.

## Local preview

```
bundle install
bundle exec jekyll serve
```

Open `http://localhost:4000`.

## Publishing a blog post

1. Create `_posts/YYYY-MM-DD-slug.md`.
2. Add front matter (`layout: post`, `title`, `date`, `excerpt`).
3. Write markdown.
4. `git push` to `main`.

See [BLOG.md](BLOG.md) for the full authoring guide.

## Headshot

Drop the headshot at `assets/img/headshot.jpg` (referenced from the hero on the home page).

## Deploy

GitHub Pages builds on push to `main`. No CI to babysit.
