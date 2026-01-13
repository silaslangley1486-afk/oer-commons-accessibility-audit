### Issue: Intermittent screen reader announcement of “table” near search input (observational)

## Description

On the Search Results page, the Search input is visually presented within a grid-like row layout. During testing on a prior session, the screen reader announced “table” when the search input became focused, despite the content not being a data table and not supporting table navigation. This likely resulted from grid-based layout cues being interpreted as tabular structure. This behavior was reproduced multiple times during that session but could not be reproduced in subsequent testing.

The layout uses grid-like visual and structural patterns that may trigger heuristic structural announcements in some screen reader configurations. This behavior is not consistently reproducible and therefore does not constitute a confirmed WCAG failure.

## Impact

This may impact some screen readers in specific contexts. In such cases, it may mislead screen reader users into thinking the Search input is part of a table, causing confusion and unnecessary cognitive load when navigating the page. E.g., it wrongly causes users to expect table keyboard navigation commands. This makes it harder for users to perform searches.

## Severity: Low (Informational)

## Recommendation:

1. Ensure grid layouts for form controls do not expose table semantics.
2. Prefer semantic grouping: `<form>` + `<fieldset>` + `<legend>`
    or a named region (`"aria-labelledby"`)
    to help immediate orientation and reduce cognitive dissonance when "Table" is announced.
3. Avoid CSS table display values for layout.
