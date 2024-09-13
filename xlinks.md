---
layout: xlinks
---

# XLinks Documentation

## Git Flows

![Logo](https://media.discordapp.net/attachments/1260271201872515132/1284177503191175268/Pastel_Colorful_Process_Flow_Graph.png?ex=66e5aeff&is=66e45d7f&hm=fbf86ff5f623490ff8cdcd1c55a616bf923434af43b797aa1e8e58d68bb0c82a&=&format=webp&quality=lossless&width=883&height=662)

## Conventional Commits Format
```bash
 - <type>(<scope>): <description>
 - feat: A new feature.
 - fix: A bug fix.
 - docs: Documentation only changes.
 - style: Make it more beauty (white-space, formatting,  missing semi-colons, etc).
```

## Deployment

To setting your VSCode
```bash
git config --global user.email "65160215@go.buu.ac.th"
git config --global user.name "Pooh_Chaimanat"
```
To checking branch
```bash
git branch
```
To switch branch
```bash
git switch <branchname>
```
## When branches has rename
If you have a local clone, you can update it by running the following commands.
```bash
git branch -m Released Release
git fetch origin
git branch -u origin/Release Release
git remote set-head origin -a
```
## Docs
Add badges from somewhere like: [github.io](https://zell3.github.io/xlinks)

* * *
