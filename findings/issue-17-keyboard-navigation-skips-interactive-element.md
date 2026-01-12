## Issue: Keyboard navigation skips the Open Filters control on mobile

### Description

On the Search Results page on mobile, the search filters are initially open. There is an "Open Filters" control when the filters are hidden and a "Close Filters" control when the filters are visible. Tabbing through the page skips the "Open Filters" control when the filters are hidden and skips the "Close Filters" control when the filters are visible. There is therefore no way for keyboard-only users to get to the filters section.

The filter controls are not accessible via keyboard navigation because an `<a>` is used without an `href`. In any case, activating the controls leads to an action rather than a navigation. `<a>` is the wrong tag to use here.

The filters section is usable by keyboard-only users once it is opened. But there is no way for keyboard-only users to close it.

Also, when the filter controls are activated via mouse, the focus shifts to the Search section which is above the Filter section.

### Impact

Keyboard-only users cannot view or use the Filters section. Keyboard-only users cannot close it once it is opened via mouse. The shifting of the focus to the Search section after activating the controls via mouse confuses keyboard-only users, since it is not clear where the focus shifted and they must now tab back through the Search section to get to the Filters section.

**WCAG 2.1 Reference:**  

2.1.1 Keyboard (A) (primary)  
2.4.3 Focus Order (A) (secondary)

**Severity:** High  
**Affected users:** keyboard-only users

### Recommended remediation

1. Use a `<button>` instead of an `<a>` for the Open Filters and Close Filters controls.
2. Ensure that the buttons have a focus indicator.
3. Manage focus explicitly:
    - On open: shift focus to the filters section (e.g., section heading or first filter control).
    - On close: return focus to the triggering control.
