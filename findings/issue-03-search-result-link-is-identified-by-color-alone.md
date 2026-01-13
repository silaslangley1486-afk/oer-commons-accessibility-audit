## Issue: Links within search results are distinguished from surrounding text by color alone

### Description
There are multiple links in each search result. These links are distinguished only by a blue color. They are only underlined on hover, which is not available to keyboard-only or touch users.

### Impact
Users with color vision deficiencies or users navigating without a mouse may have difficulty identifying interactive links within content.

**Note:** This issue was initially identified via an axe DevTools scan and was manually validated by viewing the links on the page and hovering over them.

**WCAG 2.1:** 1.4.1 Use of Color (Level A)  
**Severity:** Medium  
**Affected users:** users with color vision deficiencies, users without a mouse

### Suggested Remediation
Provide a persistent non-color visual indicator for links (e.g., underline) in the default state, while retaining hover and focus styling.
