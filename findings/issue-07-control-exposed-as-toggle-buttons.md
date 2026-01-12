## Issue: View selector options are exposed as toggle buttons instead of a radio group

### Description

On the Search Results page, the interface includes a “View” selector that allows users to choose between two mutually exclusive display options (e.g., Detail view and List view). Conceptually, this control functions as a radio group where only one option can be selected at a time. The HTML also identifies the options as intended to be radio buttons.

See /screenshots/view-controls.png for the controls.

However, screen readers announce each option as a **toggle button** (e.g., “View Detail Toggle Button”, “View List Toggle Button”) rather than as radio buttons within a group. Thus, the toggle role suggested by screen readers doesn't match the intended radio button role.

Although the selected state is announced correctly, the screen reader announcements misrepresent the nature of the control and may confuse screen reader users.

### Impact

Assisted technology users may misunderstand how the control operates, including whether multiple options can be selected simultaneously. This increases cognitive load and reduces predictability when interacting with the controls.

**WCAG 2.1:** 4.1.2 Name, Role, Value (A)
**Severity:** Medium
**Affected users:** assisted technology users

### Steps to Reproduce

1. Navigate to the search results page.
2. Move focus to the “View” selector controls with a screen reader running.
4. Notice that the screen reader announces each option as a toggle button rather than as part of a radio group.

### Expected Behavior

Controls where there is a mutually exclusive choice should be read by screen readers as radio buttons, (e.g., “View, radio group, 2 options”). It should be clear that only one option may be selected at a time.

### Actual Behavior

Each option is announced as an independent toggle button. The screen reader does not announce the mutually exclusive nature of the options.

### Suggested Remediation

Implement the control using a single, consistent interaction pattern:

- Preferably use `<fieldset>` and `<legend>` to group the native radio buttons **or**
- Use `role="radiogroup"` to group the radio buttons and use `role="radio"` with `aria-checked` on the options.

Avoid mixing button and radio semantics, and ensure the programmatic role matches the intended user interaction.

### Notes

This issue is not about announcing whether the option is selected, which is currently conveyed. Instead, the issue is the mismatch between the screen reader's announcement of it as a toggle and the actual radio button semantics.
