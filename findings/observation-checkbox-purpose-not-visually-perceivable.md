## Observation: Checkbox purpose is not visually perceivable

### Description

On the Search Resources page, the purpose of the checkbox in the row of controls below the Search Results header is unclear for sighted readers. There is no visual way to perceive what the checkbox does. It can however be programmatically determined through a screen reader since it has an `aria-label`.

Selecting the checkbox also causes a "Save" button to appear, without a visible explanation of the relationship between the checkbox and the resulting action.

See /screenshots/view-controls.png for the search results controls.

### Impact

Sighted users navigating by keyboard may be unable to determine the purpose of the checkbox or anticipate the result of interacting with it. This can lead to confusion and reduced usability when interacting with the search results interface.


**Category:** Accessibility / Usability Observation  
**Severity:** Medium  
**WCAG:** Not a WCAG 2.1 failure

### Suggested Improvement

1. Provide visible text that identifies what the checkbox is for (e.g., “Select all results”).
2. Provide a visual indicator to clarify the checkbox's relationship to the resulting "Save" action. E.g., change button text to "Save selected results".

### Notes

This observation is not a WCAG 2.1 violation. Screen readers correctly announce the checkbox via an `aria-label`. However, the information conveyed programmatically is not available through visual presentation alone.
