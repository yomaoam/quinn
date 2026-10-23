# quinn.ie: rules for coding agents

Binding for every coding tool in this repo. `CLAUDE.md` only imports this
file. This project follows Andy's build standards, `~/.claude/BUILD-STANDARDS.md` on the Mac mini where all sessions run. This file holds the project's own rules and wins where it is more specific.
Not applicable here, by design: databases, secrets and credentials (standards
D1 to D5), tests and CI (Part B), since there is no backend and no build.

## What this is

Static one-page landing site for quinn.ie, linking to the projects on its
subdomains. Hosted on GitHub Pages; `index.html` is the whole site, with
`assets/` for images and the contour SVG. `CNAME` pins the custom domain and
`.nojekyll` skips Jekyll. See [README.md](./README.md).

## Never do these

- **Never force-push, rewrite pushed history, or delete a branch (other than
  a PR branch you just merged) without Andy's go-ahead.** Otherwise the agent
  handles git: a branch per non-trivial change, one Conventional Commit per
  logical change, push, a PR via `gh`, and merging that PR once its checks
  pass.
- No build step and no npm dependencies: `index.html` stays the whole site.
- Never remove or change `CNAME` or `.nojekyll`; the live domain depends on them.

## Verification

Serve the folder locally (`npx -y serve -l 4173 .`, as in `.claude/launch.json`)
and check the page; hand Andy a short checklist for visual changes.
