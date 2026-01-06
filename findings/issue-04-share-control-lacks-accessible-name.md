## Issue: Share button lacks accessible name due to misplaced aria-label

## Description:**
The Share button does not provide an accessible name to screen readers because its aria-label is applied to a non-interactive ancestor element rather than the button itself. As a result, assistive technologies fail to announce the purpose of the control. The Report button has the same issue.

This issue was initially identified via an axe DevTools scan and was manually validated by testing with a NVDA screen reader.

**WCAG 2.1:** 4.1.2 Name, Role, Value (Level A)
**Severity:** Medium
**Affected users:** screen reader users

### Suggested Remediation
For both the Share button and the Report button, move the aria-label attribute directly onto the <button> element so that the control exposes a correct accessible name.
