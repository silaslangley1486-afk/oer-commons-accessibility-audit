## Issue: Insufficient color contrast for primary header navigation text

### Description
The "Discover" nav item is selected by default on the search results page. It has a lighter background color when selected. The result is an insufficient color contrast of 3.49:1 between the text and the background. According to WCAG 2.1 AA, the contrast should be 4.5:1 for normal size text.

### Impact
Visually impaired users may have difficulty detecting that the nav item is selected.

**Note:** This issue was initially identified via an axe DevTools scan and was manually validated using WebAIM's color contrast checker.

**WCAG 2.1:** 1.4.3 Contrast (Minimum) (Level AA)  
**Severity:** Medium  
**Affected users:** low-vision users and users in low-contrast viewing conditions

### Suggested Remediation
Adjust the background color of the selected navigation state to meet the 4.5:1 contrast ratio required for normal text, while preserving visual distinction for the active state.
