### Issue: Keyboard navigation skips the Open Filters control on mobile

### Description

On the Search Results page on mobile, the search filters are initially open. There is an "Open Filters" control when the filters are hidden and a "Close Filters" control when the filters are visible. Tabbing through the page skips the "Open Filters" control when the filters are hidden and skips the "Close Filters" control when the filters are visible. There is therefore no way for keyboard-only users to get to the filters section.

The filter controls are not accessible via keyboard navigation because an <a> is used without an `href`. In any case, activating the controls leads to an action rather than a navigation. <a> is the wrong tag to use here.

The filters section is usable by keyboard-only users once it is opened. But there is no way for keyboard-only users to close it.

### Impact

Keyboard-only users cannot view or use the Filters section. Keyboard-only users cannot close it once it is opened via mouse.

**WCAG 2.1 Reference:**  2.1.1 Keyboard (A)
**Severity:** High
**Affected users:** keyboard-only users

### Recommended remediation

1. Use a <button> instead of an <a> for the Open Filters and Close Filters controls.
2. Ensure that the buttons have a focus indicator.
3. Ensure that an accessible focus order is preserved when activating the controls.