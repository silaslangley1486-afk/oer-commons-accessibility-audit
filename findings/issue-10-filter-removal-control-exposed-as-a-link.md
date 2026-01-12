## Issue: Filter removal control exposed as a link with misleading semantics

### Description

If the User has previously selected search filters, then they are listed on the Search Results page after the label: "Selected filters". Each filter has a clickable control in front of it that will remove it when it is clicked and then update the search results list accordingly. See /screenshots/search-filters.png for a screenshot.

The control is implemented as an anchor (`<a>`) element and announced by screen readers as a “same page link.” But selecting it does not cause any navigation. It instead removes the filter and updates the results.

Also, when the filter's control has focus, the screen reader does not name the filter that is to be removed, nor is there any indication that selecting the control will update the search results. Assisted technology users are therefore given the wrong role for the control and not enough information about what it's for.

### Impact

Assisted technology users will wrongly expect navigation when selecting the control. This can lead to confusion, accidental filter removal, and difficulty understanding why search results have changed.

**WCAG 2.1:** 4.1.2 – Name, Role, Value (A)  
**Severity:** Medium  
**Affected users:** assisted technology users

**Recommended remediation:**  

1. Use a `<button>` element instead of an `<a>` element for the control.
2. Provide an accessible name that clearly indicates the action and target (e.g., “Remove filter: High School”).
3. Ensure the control’s role and behavior align with user expectations.
