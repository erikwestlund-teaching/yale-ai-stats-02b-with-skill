---
name: ggplot-style
description: House style for ggplot2 figures in this project. Use whenever creating or editing a ggplot2 chart, or writing an interpretation of one.
---

# ggplot2 house style

Follow these rules for every ggplot2 figure in this project.

## Look

- Start from `theme_minimal(base_size = 14)`.
- Put the legend at the bottom: `theme(legend.position = "bottom")`.
- For discrete colors, use `scale_color_brewer(palette = "Dark2")` (or `scale_fill_brewer`).
- When points overlap, use `alpha = 0.3` and add a smoothed trend with `geom_smooth(method = "loess", se = TRUE)`.

## Labels

- The title states the finding in plain words, not the variable names. Good: "Systolic blood pressure rises with age". Bad: "systolic_mean vs age_years".
- Axis labels include units, e.g. "Age (years)", "Systolic blood pressure (mm Hg)".
- Add a subtitle that names the data and the sample size, e.g. "Neighborhood Health Survey, adults 18+ (n = 3,412)". Compute n from the plotted data. Don't type it in.
- Add a caption that starts with "Source: ".

## Data

- Drop rows missing any plotted variable **before** plotting, and say in the text how many rows were dropped.
- Unless asked otherwise, plot adults only (`age_years >= 18`) and say so in the subtitle.

## Interpretation

- Write 2–3 sentences that describe the pattern. Don't use causal language ("causes", "leads to", "effect of").
- Mention one limitation.

## When done

List which of these rules you followed and any you couldn't follow.