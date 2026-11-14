---
name: ui-restraint
description: User interface rules for Perigee. Use when you review, plan or discuss Svelte components, CSS, layout, colour, fonts, icons, motion or the globe display. The rules prevent the generic look of AI-made interfaces.
---

# User interface rules

Perigee is a control room display for a second monitor.
The user looks at it from a distance of about 2 m and sometimes operates it.
The display is dark, dense and quiet. Data has priority over decoration.

The tutor rule in `CLAUDE.md` applies. Explain and review. Do not write the components.

## Before UI work

1. State the purpose of the element in one sentence.
2. State which data the element shows and how old the data can be.
3. Use the design tokens that exist. Add a token only if no token fits.

## Not permitted

- Emojis as icons or in labels.
- Colour gradients as backgrounds, on text or on buttons.
- Purple and blue "AI" colour schemes.
- Glass effects: background blur and transparent panels.
- Glow, neon and bloom effects on panels and text.
- Shadows that make panels float. Use a 1 px border.
- Large corner radii. The maximum radius is 4 px.
- Cards inside cards.
- A hero section with a slogan.
- Motion for decoration: pulse, bounce, shimmer, parallax, animated backgrounds.
- Loading skeletons that move. Show the last data with its age.
- Tooltips as the only place for necessary information.
- Remote fonts, icon fonts from a CDN and all other third-party requests.
- A UI kit, a CSS framework or an icon package without a decision record.

## Colour

- Define all colours as CSS custom properties in one file.
- Use one background colour, one panel colour, two text colours and one accent colour.
- Status colours have a fixed meaning: go, hold, scrub, unknown.
- Use a status colour only for status.
- Do not show information with colour only. Add a text or a shape.
- Text contrast is 4.5:1 or more.

## Type

- Use one font family for text and one monospace family for numbers.
- Include the font files in the app. The alternative is the system font stack.
- Use tabular figures for countdowns, times and coordinates. The digits must not move.
- The smallest text size is 14 px. The countdown must be readable from 2 m.
- Use two font weights.
- Use upper case only for short labels of 3 words or less.

## Layout

- Use CSS grid for the panel layout.
- Use a spacing scale with steps of 4 px: 4, 8, 12, 16, 24, 32.
- Align numbers to the right or on the decimal point.
- Each panel has a title, the data and the age of the data.
- An empty state says what is missing and why.

## Data display

- Show the unit with each value.
- Show times in UTC and in local time. Label the two.
- Show the age of data when the data is not live.
- Show a clear state for offline operation and for rate limits.

## Motion

- Motion occurs only for two reasons: the data changes, or the user operates the app.
- A transition is 200 ms or less.
- Obey `prefers-reduced-motion`.
- The globe draws no frame when the camera and the data do not change.
- The ambient rotation has a maximum of 30 frames each second. It stops when the window is hidden.

## Icons

- Use one set of local SVG icons with one line width.
- An icon has a text label. An exception is a standard control, for example "close".

## Interaction

- All functions operate with the keyboard.
- The focus state is visible.
- A click target is 32 px or more.
- A drag on the globe is not a click. Compare the pointer position at the start and at the end.

## Review checklist

1. Does each element have a purpose?
2. Is there an item from the "Not permitted" list?
3. Do all colours and sizes come from tokens?
4. Is the text in agreement with the `plain-language` skill?
5. Does the display stay idle when no data changes?
