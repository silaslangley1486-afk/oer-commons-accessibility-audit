### Issue: The Search button is missing a label on mobile viewports

### Description

On the Search Results page on mobile, the "Search" button has a magnifiying glass icon instead of text. It does not have an "aria-label". As a result, screen readers read the button as simply "Button".

### Impact

Assisted Technology users will not know what the button is for.

**WCAG 2.1 Reference:**  4.1.2 – Name, Role, Value (A)
**Severity:** Medium
**Affected users:** assistive technology users

### Recommended remediation

Add `aria-label="search"` to the <button> tag.
