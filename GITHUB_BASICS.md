# GitHub Basics: A Beginner's Guide

## The big picture

- **Git** is a tool that tracks changes to files. It keeps a full history, so
  you can always go back.
- **GitHub** is a website that stores your Git projects online, so you can back
  them up, share them, and work with others.
- A **repository** (or "repo") is one project folder, plus its full history.

## Key words

| Term | Meaning |
| --- | --- |
| **Commit** | A saved snapshot of your changes, with a short message describing what changed. |
| **Branch** | A separate line of work. `main` is the official version. You make changes on other branches so you can't break `main` while you work. |
| **Push** | Upload your commits from your computer to GitHub. |
| **Pull** | Download the latest commits from GitHub to your computer. |
| **Clone** | Download a full copy of a repo to your computer for the first time. |
| **Pull request (PR)** | A request to merge one branch into another (usually into `main`). You can review the changes before accepting them. |
| **Merge** | Combine the changes from one branch into another. |
| **Issue** | A to-do item, bug report, or idea, tracked on GitHub. |

## The everyday workflow

```
1. Make a branch      →  git switch -c my-new-feature
2. Edit some files
3. Stage the changes  →  git add .
4. Commit them        →  git commit -m "Describe what you changed"
5. Push to GitHub     →  git push -u origin my-new-feature
6. Open a pull request on GitHub, review it, and merge it into main
```

Useful commands to see what's going on:

```
git status     # What has changed? What's staged?
git log        # Show the history of commits
git diff       # Show exactly what changed in each file
```

## Doing it all on the website (no command line)

You can do most of this in your browser on github.com:

- **Edit a file:** open it, click the ✏️ pencil icon, make changes, then click
  **Commit changes**.
- **Add a file:** click **Add file → Create new file** or **Upload files**.
- **Merge a pull request:** go to the **Pull requests** tab, open it, and click
  **Merge pull request**.

## Tips

- Commit little and often, with clear messages. "Fix typo in README" is better
  than "stuff".
- Never commit passwords, API keys, or other secrets. The `.gitignore` file
  helps with this.
- Use **Issues** as a to-do list for your project.
- Keep your `README.md` up to date. It's the first thing people see.

## Learn more

- GitHub's official tutorial: https://docs.github.com/en/get-started/start-your-journey/hello-world
- Interactive Git practice: https://learngitbranching.js.org/
