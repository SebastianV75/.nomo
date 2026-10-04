# Set up a Nomo page

This repo is a Nomo page. `human.md` is the whole page at `https://nomo.md/username`, where `username` owns the repo. The full guide is https://nomo.md/AGENTS.md. Read it if you can.

## The repo

The repo must be named `.nomo`, be public, and belong to the person. If this is still `adnfng/.nomo`, don't edit it. Create their own copy:

```bash
gh repo create .nomo --public --clone --template adnfng/.nomo
```

## Draft from their GitHub profile

Ask before you use it. Then:

```bash
gh api user --jq '{login, name, bio, blog, company, location, twitter_username}'
gh api user/social_accounts
```

Ask two or three short questions to fill the gaps. Do not invent a biography.

## Syntax

```md
![Their Name](assets/me.jpg)

# Their Name

One line about what they do.

[GitHub](https://github.com/them) · [Email](mailto:them@example.com)

## Work

- 2024 – now · [Company](https://example.com) · Role
- 2021 · Earlier role

## Projects

<!-- github:pinned -->
```

- An image at the very top is the header photo. Replace `assets/me.jpg`, or use `https://github.com/theirusername.png`.
- `# Their Name` is the home tab. Each `##` starts another tab. `###` is a heading inside a tab.
- In a list item, ` · ` mutes what follows, on the same line. A second line in the item sits underneath, muted. Items that start with a year line up in a date column.
- `<!-- github:pinned -->` lists their pinned GitHub repos and stays current.
- Two or more images in one paragraph become a gallery.
- A blank line is a paragraph. No YAML frontmatter.

## Voice

Write as them, in the first person. Short sentences. No marketing words.

## Done

Show them the draft and ask before you push. Then push to the default branch. The page is `https://nomo.md/theirusername`, live within about a minute.
