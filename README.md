# Mathematical Thinking

Created from the [Kibo Course Template](https://github.com/rrcobb/course-template)

A template for an [mdbook](https://rust-lang.github.io/mdBook/index.html)-powered course site.

## What's here?

```
$ tree .
.
├── README.md
├── book.toml
└── src
    ├── SUMMARY.md
    └── [chapter].md
```

### README.md

You're lookin at it.


### output/

The static site output will be built to `output/`, but that's git ignored.

To generate the static site, run:

```
mdbook build
```

Output lives here, in `output/`.
You can usually ignore the files in `output`, git will.

### book.toml

Config file for the course. Authors, title, other mdbook settings.

https://rust-lang.github.io/mdBook/format/configuration/index.html

### src/SUMMARY.md

This gets turned into the sidebar on the site. 

It's the text that should show, plus links to other md files in `src/`.

https://rust-lang.github.io/mdBook/format/summary.html

### src/*

These are the pages that actually make up the course. It's nice to put
things in folders to organize the different pages, so that's what the convert
script does by default.

## Getting Started

Install mdbook: https://rust-lang.github.io/mdBook/guide/installation.html

if you use rust:

```
cargo install mdbook
```

Or use your package manager: `brew install mdbook`, or download a release from
Github.

## Run the book locally

```
mdbook serve --open
```

## Deployment

We use `vercel` to handle deploys. This repo should be set up with a vercel 
project, assigned a production domain, and have auto-deploys set up.

* Github actions will run `mdbook build` on pushed changes
* All pushes will automatically deploy to vercel
* Vercel will notify the #tech-status channel on Slack with the deploy preview
* If you pushed to `main`, it will also deploy to the live site. Watch out!

## Previews and Drafts

If you'd like to preview changes, push to the `draft` branch. There should be a
pinned message in the #tech-status Slack channel with the permanent url, and a
message each time time there's a new preview site to view.

Remember - commits to `main` get built and deployed to the production site; others
just get previews.
