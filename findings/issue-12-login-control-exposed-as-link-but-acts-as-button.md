## Issue: login control exposed as link but acts as button

### Description

On the Search Results page, there is a Login control that screen readers read as a "Same page link" and is implemented using an `<a>` tag. Yet clicking the Control instead opens a dialog. It function as an action and not a link.

### Impact

This misleads assisted technology users to expect page navigation when instead a dialog is opened. The mismatch between semantics and behavior and the unexpected context change may cause confusion and increase cognitive load.

**WCAG 2.1:** 4.1.2 – Name, Role, Value (A)  
**Severity:** Medium  
**Affected users:** assisted technology users

### Reproduction Steps

1. Navigate to the Search Results page with a screen reader activated.
2. Move focus to the checkbox at the beginning of the search result controls.
3. Press Space or Enter to select the checkbox.
4. Tab to the newly visible "Save" button and press Enter or Space to open the dropdown.
5. Press tab to navigate to the Login control inside the dropdown.

### Recommended remediation

Use a `<button>` element for the Login control, or otherwise ensure the exposed role and accessible name accurately convey that the control opens a dialog rather than navigating.
