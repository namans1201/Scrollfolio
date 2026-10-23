# Scrollfolio

A scroll-animated portfolio built with React, TypeScript and Vite.

Scroll through a subgrid photo wall of projects that transitions from a
full-viewport hero image down to a 5x3 grid of project cards. Each card links to
its GitHub repository. The animation is driven entirely by CSS scroll-driven
animations (`animation-timeline`, `view-timeline`, `animation-range`), with GSAP
ScrollTrigger as a fallback for browsers that do not yet support the spec.

## Stack

- React 19 with TypeScript
- Vite
- CSS scroll-driven animations and subgrid
- GSAP ScrollTrigger, fallback only

## Structure

```
src/
  App.tsx
  data.ts          project list and metadata
  components/
  hooks/           including usePlaybook
  styles/          including playbook.css
public/images/     project thumbnails
```

## Dev

```bash
npm install
npm run dev
```

## Build

```bash
npm run build
```

## Branches

This repository has 11 branches, but only `main` carries current work. Every
other branch is a historical checkpoint: each is **0 commits ahead** of `main`
and between 12 and 31 commits behind it. Nothing is stranded on any of them.

| Branch | Head | Last commit | Behind `main` | What it was |
| --- | --- | --- | --- | --- |
| `main` (default) | `035c9a14` | 2026-06-23 | baseline | Latest. 33 commits. Tip commit "Update data.ts". Most recent substantive change replaced the water-logger project entry with nourishcue and refreshed its thumbnail. |
| `prod-final` | `5b57cb00` | 2026-06-16 | 12 | Closest checkpoint to `main`, differing in only 3 files (6 insertions, 6 deletions). Tip commit "Card label". This is the branch that was repeatedly merged into `main` through pull requests 5 through 8. |
| `prod3` | `28e0cd89` | 2026-06-13 | 20 | Checkpoint at "Images fix". Differs by 16 files. |
| `vercel/install-vercel-speed-insights-t5b3bp` | `c29416cd` | 2026-06-13 | 21 | Vercel bot branch, 1 commit ahead of its base, adding Vercel Speed Insights configuration across 3 files (42 insertions). Never merged. Differs from `main` by 19 files. |
| `prod2` | `547b5b68` | 2026-06-13 | 23 | Checkpoint at "Prod-ready". Differs by 19 files. |
| `prod` | `3488722c` | 2026-06-13 | 24 | Checkpoint at "Tab fix". Differs by 47 files. |
| `best5` | `6365405d` | 2026-06-13 | 26 | Checkpoint at "Almost". Differs by 49 files. |
| `best4` | `9104b81e` | 2026-06-13 | 27 | Checkpoint at "Fixed". Differs by 53 files. |
| `scroll-best3` | `76fca8c3` | 2026-06-13 | 28 | Scroll-animation iteration at "Fixed". Differs by 53 files. |
| `scroll-best2` | `d8ea55fc` | 2026-06-12 | 29 | Scroll-animation iteration at "Curves". Differs by 53 files. |
| `scroll-best1` | `5739a99b` | 2026-06-12 | 31 | Earliest scroll-animation iteration, at "Fixed". Differs by 53 files. |

**Latest branch: `main`**, 2026-06-23, and it is a strict superset of every
branch except the Vercel bot branch.

The naming records the development order: `scroll-best1` through `scroll-best3`
were scroll-animation experiments, `best4` and `best5` continued the tuning,
then `prod` through `prod-final` were release candidates. All of that work landed
in `main`.

Because every one of these branches is fully contained in `main`, the nine
`scroll-best*`, `best*` and `prod*` branches can be deleted without losing
anything. The only branch holding unique commits is the Vercel bot branch, whose
sole contribution is Speed Insights configuration; either merge that or delete it
too.
