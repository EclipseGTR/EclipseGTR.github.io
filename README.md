# Personal Security Portfolio

My personal website: a blog and portfolio of information security projects.

🌐 **Live site:** https://eclipsegtr.github.io/

## How it works

The site is built with [Jekyll](https://jekyllrb.com/), a tool that turns
Markdown text files into a website, and hosted for free by
[GitHub Pages](https://pages.github.com/). There's no server to run and no code
to write. You edit text files, and GitHub rebuilds the site automatically.

## Where things live

| Path | What it is |
| --- | --- |
| `_config.yml` | Site settings: your name, tagline, social links |
| `_posts/` | Blog posts, one Markdown file per post |
| `_projects/` | Projects, one Markdown file per project |
| `about.md` | About page: bio, skills, certifications |
| `assets/css/style.css` | Colors and styling |
| `assets/img/` | Images (create this folder when you add your first one) |
| `_layouts/`, `_includes/` | Page templates; you rarely need to touch these |

📖 See **[WRITING_GUIDE.md](WRITING_GUIDE.md)** for how to add posts and
projects, and an **infosec publishing checklist**.

New to GitHub? See [GITHUB_BASICS.md](GITHUB_BASICS.md).

## Preview locally (optional)

This is not required. GitHub builds the site for you. If you install Ruby,
you can preview changes on your own computer first:

```
gem install jekyll
jekyll serve
```

Then open http://localhost:4000/
