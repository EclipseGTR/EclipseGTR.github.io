# Writing Guide: How to Update Your Site

Everything on the site is plain text files. You can edit them right on
github.com: open a file, click the ✏️ pencil, then **Commit changes**. The
site rebuilds itself about a minute later.

## First things to personalize

1. **`_config.yml`**: set your `title` (your name), `tagline`, `author`, and
   social links.
2. **`about.md`**: your bio, skills, certifications, and experience.
3. Edit or delete the sample post and the two sample projects.

## Add a blog post

Create a new file in the `_posts/` folder. The name **must** follow this
pattern: `YYYY-MM-DD-short-title.md`, e.g. `_posts/2026-11-02-htb-lame-writeup.md`.

Start it with this header (called "front matter"), then write in Markdown:

```markdown
---
title: "Hack The Box: Lame Write-up"
tags: [ctf, htb, linux]
---
A short intro paragraph. This becomes the preview text.

## Enumeration

...
```

## Add a project

Create a new file in the `_projects/` folder, e.g. `_projects/phishing-analyzer.md`:

```markdown
---
title: "Phishing Email Analyzer"
summary: "One or two sentences shown on the project card."
tools: [Python, VirusTotal API]
featured: true   # true = also shown on the home page
order: 3         # lower numbers appear first on the Projects page
repo: https://github.com/EclipseGTR/phishing-analyzer   # optional
---
## Problem
## Approach
## Results
```

A good project write-up answers: *What problem? What did I build or do? What
did I learn?* Screenshots help a lot. Put them in `assets/img/` and embed them
with `![Description](/assets/img/file.png)`.

## Add images

Upload them to `assets/img/` (on github.com: **Add file → Upload files**).

## Markdown cheat sheet

| You type | You get |
| --- | --- |
| `## Heading` | A section heading |
| `**bold**` / `*italic*` | **bold** / *italic* |
| `[link text](https://example.com)` | A link |
| `` `nmap -sV` `` | Inline code |
| Three backticks + language name, on their own line | A code block (close it with three backticks) |
| `- item` | A bullet list |
| `> note` | A highlighted quote or callout |

---

# ⚠️ Infosec Publishing Checklist

Run through this before you publish anything security-related:

- [ ] **Authorization:** Was all the testing done on systems I own, or on
      platforms that allow it (HTB, TryHackMe, labs, bug bounty programs in
      scope)? Never write up testing you weren't authorized to do.
- [ ] **No employer or client details:** No company names, internal hostnames,
      IP ranges, usernames, ticket numbers, or screenshots from work systems.
      Check your employer's policy on public writing.
- [ ] **Redact screenshots:** Look for IP addresses, email addresses, API keys,
      session tokens, and browser tabs or bookmarks in the background. Blur
      or box them out **before** uploading. Cropping in some tools leaves the
      original image data behind.
- [ ] **CTF / platform rules:** Only publish write-ups for retired machines or
      challenges, or after the competition ends. Hack The Box, for example,
      prohibits write-ups of active machines.
- [ ] **Vulnerabilities:** Only publish after the vendor has fixed the issue,
      or the coordinated disclosure deadline has passed.
- [ ] **No secrets in the repo:** Everything in this repository is public,
      **including its history**. Deleting a file later does not remove it from
      past commits. Never commit passwords, keys, or `.env` files.

## Post ideas for security folks

- CTF and lab write-ups (retired HTB / TryHackMe boxes, PicoCTF)
- Home lab build logs (SIEM, Active Directory lab, honeypot)
- Detection engineering: "How I detected X with Sigma or Splunk"
- Malware or phishing analysis of public samples
- Certification study notes and what helped you pass
- Tool deep-dives: "Five Wireshark filters I use every day"
- Summaries of conference talks or news, with your own analysis
