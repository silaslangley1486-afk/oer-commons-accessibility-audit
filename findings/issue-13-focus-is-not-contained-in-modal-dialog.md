### Issue: Modal dialog does not trap keyboard focus (focus can escape the dialog)

### Description

A Login control on the Search Results page opens a modal dialog. But the focus is not contained inside the dialog. Tabbing past the last focusable element in the dialog moves focus outside the modal dialog to browser UI controls. Using Shift + Tab on the first focusable element in the modal dialog sometimes but not always closes the modal dialog. It also shifts focus to the last focusable element on the page where the modal is opened.

The focus movement is unpredictable and confusing. It is difficult for keyboard users to understand where the focus is located and to reliably interact within the dialog.

## Impact

It is easy for keyboard users and assistive technology users to lose their place, become confused, accidentally exit the modal dialog, or reliably complete the task in the dialog. 

**WCAG 2.1:**
    2.4.3 – Focus Order (Primary) (A)
    2.1.1 – Keyboard (Secondary) (A)

**Severity:** High
**Affected users:** keyboard only users, assistive technology users

**Evidence / notes:**  
- Dialog container includes `role="dialog"` and `tabindex="-1"`, but focus is not trapped within the dialog while open.

### Steps to Reproduce

1. Navigate to the search results page.
2. Move focus to the checkbox at the beginning of the search result controls.
3. Press Space or Enter to select the checkbox.
4. Tab to the newly visible "Save" button and press Enter or Space to open the dropdown.
5. Press tab to navigate to the Login control inside the dropdown.

### Recommended remediation:

1. Implement focus management consistent with modal dialog behavior:
    - Trap focus within the modal dialog while it is open. Tab and Shift+Tab should cycle through focusable elements inside the modal dialog.
    - Ensure ESC consistently closes the modal dialog.
    - When the modal dialog closes, return focus to the Login control that opened the dialog.
