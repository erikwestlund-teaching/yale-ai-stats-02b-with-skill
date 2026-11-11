---
name: ggplot-style
description: House style for ggplot2 figures in this project. Use whenever creating or editing a ggplot2 chart, or writing an interpretation of one.
---

# ggplot2 house style

Follow these rules for every ggplot2 figure in this project.

## Look

- Start from `theme_minimal(base_size = 14)`.
- Put the legend at the bottom: `theme(legend.position = "bottom")`.
- Color gender with fixed colors: Female = `#7B3294`, Male = `#008837`. The data code gender as `female` and `male`, so use `scale_color_manual(values = c(female = "#7B3294", male = "#008837"), labels = c(female = "Female", male = "Male"))`. Use the same colors for fills.
- For other discrete colors, use `scale_color_brewer(palette = "Dark2")` (or `scale_fill_brewer`).
- When points overlap, use `alpha = 0.15` and `size = 1`, and add a smoothed trend with `geom_smooth(method = "loess", se = TRUE)`.

## Labels

- The title states the finding in plain words. Good: "Systolic blood pressure rises with age". Bad: "systolic_mean vs age_years".
- Axis labels include units, e.g. "Age (years)", "Systolic blood pressure (mm Hg)".
- Add a subtitle that names the data and the sample size, e.g. "Neighborhood Health Survey, adults 18+ (n = 3,412)". Compute n from the plotted data. Don't type it in.
- Use this caption, word for word: "Source: Neighborhood Health Survey (simulated), 2021–2023. Unweighted."

## Data

- Drop rows missing any plotted variable **before** plotting, and say in the text how many rows were dropped.
- Unless asked otherwise, plot adults only (`age_years >= 18`) and say so in the subtitle.
- `age_years` is top-coded at 80: a value of 80 means 80 or older. Describe the oldest ages as "80 or older."

## Interpretation

- Write 2–3 sentences that describe the pattern. Don't use causal language ("causes", "leads to", "effect of").
- Mention at least one limitation. Always note that the estimates are unweighted.

## Final check

List which of these rules you followed and any you couldn't follow.
