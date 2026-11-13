---
name: ggplot-style
description: House style for ggplot2 figures in this project. Use whenever creating or editing a ggplot2 chart, or writing an interpretation of one.
---

# ggplot2 house style

Follow these rules for every ggplot2 figure in this project.

## Look

- Start from `theme_minimal(base_size = 14)`.
- Put the legend at the bottom: `theme(legend.position = "bottom")`.
- Color gender or sex with fixed colors: Female = `#7B3294`, Male = `#008837`. Name the values by the codes in the data and add readable labels, for example `scale_color_manual(values = c(female = "#7B3294", male = "#008837"), labels = c(female = "Female", male = "Male"))`. Use the same colors for fills.
- For other discrete colors, use `scale_color_brewer(palette = "Dark2")` (or `scale_fill_brewer`).
- When points overlap, use `alpha = 0.15` and `size = 1`, and add a smoothed trend with `geom_smooth(method = "loess", se = TRUE)`.

## Labels

- The title states the finding in plain words. Good: "Income rises with years of schooling". Bad: "income vs educ_years".
- Axis labels include units, e.g. "Age (years)", "Household income (US$)".
- Add a subtitle that names the data, the population, and the sample size, e.g. "County Health Survey, adults 18+ (n = 2,105)". Compute n from the plotted data. Don't type it in.
- Add a caption in this form: "Source: <data name>, <years>. Unweighted." Add "(simulated)" after the data name when the data are simulated. Write "Weighted" when the estimates use survey weights.

## Data

- Drop rows missing any plotted variable **before** plotting, and say in the text how many rows were dropped.
- For data on people, plot adults only (age 18 or older) unless asked otherwise, and say so in the subtitle.
- Check the codebook for top-coded variables. Describe a top-coded value as that value "or older" (or "or more"). For example, an age top-coded at 80 means "80 or older."

## Interpretation

- Write 2–3 sentences that describe the pattern. Don't use causal language ("causes", "leads to", "effect of").
- Mention at least one limitation. Always say whether the estimates are weighted or unweighted.

## Final check

List which of these rules you followed and any you couldn't follow.
