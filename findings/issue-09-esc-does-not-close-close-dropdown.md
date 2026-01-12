## Issue: No obvious keyboard-only way to close dropdown

### Description

Pressing Enter on the "Save" button on the Search Results page opens a dropdown. The dropdown contains a Login control, which is its only focusable element. Once the User tabs to the Login control, there is no obvious way to close the dropdown. Pressing Esc will not close it. The only way to close it is to press Shift + Tab to return focus to the button and then press Esc, Space, or Return.

While the dropdown can be opened via keyboard, it cannot be dismissed using standard keyboard interaction once focus has moved inside, requiring users to perform non-obvious focus reversal to exit the component.

### Impact

This will confuse keyboard-only users since there is no obvious way to close it with only the keyboard. The dropdown when open also prevents viewing part of the first search result, so the open dropdown impacts usability adding to further frustration on the part of the user.

**WCAG 2.1:** 2.1.1 Keyboard (A)  
**Severity:** Medium  
**Affected users:** keyboard-only users

### Steps to Reproduce

1. Navigate to the Search Results page.
2. Move focus to the checkbox at the beginning of the search result controls.
3. Press Space or Enter to select the checkbox.
4. Tab to the newly visible "Save" button and press Enter or Space to open the dropdown.
5. Press tab to navigate to the Login control inside the dropdown.
6. Press Esc to exit the dropdown

Notice that the dropdown does not close.

### Suggested Remediation

Allow the dropdown to be dismissed using the Esc key while focus is on any element within the dropdown (e.g., the Login control), so that keyboard users can exit the component without needing to Shift + Tab back to the trigger.
