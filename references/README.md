# references/ — source art (not in git)

This folder holds the **raw brand and course illustration source files** — the
original Eggo artwork from Maggie Appleton plus ~20 years of egghead course
illustrations (`.ai`, layered `.png`, working files, exports).

**The contents are intentionally _not_ committed to GitHub.** It's several
gigabytes of binary source art — too large for a git repo, and it's working
material rather than shippable assets. Only this README and the empty folder
structure are tracked; the `.gitignore` excludes everything else in here.

## What lives here

```
references/
  all-the-eggos-from-maggie-appleton/   the Eggo mascot source set
  course-illustrations/                 per-course illustration archives
```

## Where to get the actual files

The full source art lives on the **egghead Dropbox**. Ask in the team channel
for access if you need the originals — pull them into the matching folder here
and they'll stay out of git automatically.

> Need a specific illustration shipped on the web? Export a sized copy into the
> repo's top-level `assets/` folder (that folder _is_ committed) rather than
> committing anything from `references/`.
