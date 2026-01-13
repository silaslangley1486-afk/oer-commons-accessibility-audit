## Issue: Search submit causes focus to be lost with no visible focus indicator

### Description
On the Search Results page, after submitting a search either by pressing Enter on the Search input textbox or on the "Search" submit button, the page correctly reloads to show the search results. But there is no longer a keyboard focus on any element, making it unclear where the focus has gone. The active element becomes the page root body element.

### Impact
Keyboard-only users will lose track of where the focus is. They will not be able to continue navigating through the page without restarting the application.

**WCAG 2.1:** 
 - 3.2.2 On Input (A)
 - 2.4.7 Focus Visible (AA)

**Severity:** Medium  
**Affected users:** keyboard-only users

### Suggested Remediation

After search submission on the Search Results page:

1. Move the focus to a logical location, such as the first search result.
2. Make sure the focused element has a visible focus indicator that is easy to distinguish from the background.