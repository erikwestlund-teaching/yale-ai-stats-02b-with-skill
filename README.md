# Exercise 2b: With a Skill

Part of the workshop **AI Tools for Statistical Programming and Analysis**.

Exercise 2 is the same project twice, with the same data, notebook, and prompt. This copy **has** a skill, `ggplot-style`: a set of house rules for ggplot2 figures. It's in `.agents/skills/` (read by Posit Assistant and Codex) and `.claude/skills/` (read by Claude Code). Folders starting with `.` are hidden; in RStudio's Files pane use **More → Show Hidden Files**. The other copy is [`yale-ai-stats-02a-without-skill`](https://github.com/erikwestlund-teaching/yale-ai-stats-02a-without-skill).

## Install packages

Run this once in the R console, from the project folder:

```r
source("setup.R")
```

It installs any of this project's packages that are missing: readr, dplyr, ggplot2, here, rmarkdown.

## Open the project

- **RStudio:** open `yale-ai-stats-02b-with-skill.Rproj`.
- **Positron or VS Code:** open this folder.
- **Claude Code or Codex:** start the tool from a terminal in this folder.

You need R and Quarto (bundled with RStudio and Positron). `setup.R` installs the packages.

## Steps

1. Give your assistant this prompt, without mentioning any skill:

   ```text
   Complete the task in notebooks/visualization.qmd and render it.
   ```

2. Do the same in the other copy.
3. Compare the two figures and interpretations: theme and colors, a title that states the finding, units, a subtitle with n, a "Source:" caption, how missing rows were handled, and whether the interpretation avoids causal language.

A skill makes certain behavior more likely. It doesn't guarantee it.

## About the folders

This project was created from a [Framework](https://framework.pub) blueprint, so it has the folder layout of a real analysis project: raw data in `inputs/raw/`, notebooks in `notebooks/`, results in `outputs/`. You don't need the framework R package; the notebooks use plain R.
