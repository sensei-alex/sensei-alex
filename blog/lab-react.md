---
tags:
- resource
area: "[[lab]]"
publish: "[[blog]]"
created: 2025-06-17
updated: 2025-06-22
---

Hello, world. I've been rewriting the project in react.

## Why
- To simplify state management. In react, state lives at the top and changes can only go down. All external dependencies follow the same data model and have similar APIs.
- The logic can be naturally split into simple hooks.
- The addition of a build step gives me full typescript.

## Progress
- Scaffolded the project
- Upgraded to CodeMirror 6
- Implemented lesson fetching & rendering
- Implemented the "show solution" button
- Implemented LAN scanning
- Code sync in progress

## Lesson Data Format
The last version had a YAML file for each project with markdown strings in it. Editing it took a bit of time because I had to get my note from Obsidian, split it, add images manually, translate it, then upload to check if it works or not.

Now each *lesson* (not project) is a single markdown file that lives outside the repo (example: https://snlx.net/lab-src/lab-mockup.md) and has 3 sections:
- the frontmatter
- the body
- and the solution (optional)

The frontmatter contains links to the next & previous notes as well as the runner type (not used yet) and the language.

The switch to markdown sources helps in multiple ways:
- I can upload directly from Obsidian
- The notes repo can be licensed under creative commons instead of something created for code
- I'm already using the same type of files for [[notes]] & [[blog]]. When I make a proper website, different kinds of notes can be displayed on it in different ways. This would mean that I could link from a blogpost to a lab lesson or the other way around and have it render correctly.

## Timeline
I think I should finish the basic features by the end of the week, at which point I'll merge the react branch into main and post an update here. The week after that will be dedicated to writing the first 2 projects. See you on the 29th of June!