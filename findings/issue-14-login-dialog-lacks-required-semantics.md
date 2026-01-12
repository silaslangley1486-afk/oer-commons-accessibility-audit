### Issue: Login modal dialog lacks required semantics and missing Close control on larger viewport widths

### Description

On the Search Results page, a Login control opens a modal dialog. The dialog element correctly has `role="dialog"`. But it does not include `aria-modal="true"`. As a result, users can interact with background elements behind the dialog when the nature of this dialog suggests only elements inside the dialog should be interactive.

A "Close" button exists in the markup (`aria-label="Close"`), but it is configured to display only at small viewport breakpoints (`visible-xs-block visible-sm-block`). Thus, no "Close" control is visible on medium and large viewport widths. This causes an inconsistency between the control on smaller and larger viewport widths.

### Impact

The lack of `aria-modal="true"` may cause assistive technology users to be overwhelmed by irrelevant background content when the dialog is open. Also, sighted keyboard-only users on desktop may not know how to close the dialog. This can lead to confusion, increase frustration, and increase the possibility of unintended actions. The inconsistency between the visibility of the "Close" control on different viewport widths may cause confusion for users who rely on predictable interaction patterns to identify how to dismiss modal content.

**WCAG 2.1:**
    4.1.2 – Name, Role, Value (Primary) (A)
    3.2.4 - Consistent Identification (Secondary) (AA)

**Severity:** Medium
**Affected users:** keyboard only users, assistive technology users

### Evidence / notes
- Dialog container: `<div ... role="dialog" tabindex="-1">`  
- Missing: `aria-modal="true"`  
- Close button uses `visible-xs-block visible-sm-block` (hidden on md/lg)

### Steps to Reproduce

1. Navigate to the search results page.
2. Move focus to the checkbox at the beginning of the search result controls.
3. Press Space or Enter to select the checkbox.
4. Tab to the newly visible "Save" button and press Enter or Space to open the dropdown.
5. Press tab to navigate to the Login control inside the dropdown.
6. Press Enter to open the dialog.

### Recommended remediation

1. Add `aria-modal="true"` to the dialog container.
2. Ensure a visible, focusable Close/Cancel control is available on all viewport widths (do not restrict the "Close" button to mobile-only breakpoints).
