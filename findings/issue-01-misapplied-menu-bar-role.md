## Issue: Misapplied ARIA menubar role causes misleading screen reader context in global navigation

**Evidence:**

1. Screen reader announces “submenu” instead of a top-level menu.
2. Arrow-key navigation expected for menubar is not supported.
3. Interaction follows standard tab order, not menu behavior.

**Impact:**

1. Screen reader users are misled about the menu type.
2. Keyboard users cannot navigate as expected for the announced menu type.
3. Violates proper use of ARIA roles.

This issue was initially identified via an axe DevTools scan and was manually validated using screen reader and keyboard testing.

**WCAG 2.1:** 4.1.2 Name, Role, Value (Level A)  
**Severity:** High 
**Affected users:** Screen reader users 

### Steps to Reproduce
1. Navigate to the search results page.
2. Tab to the Search icon in the header with the screen reader on.

### Expected Behavior
Search icon should not be announced as belonging to a sub-menu.

### Actual Behavior
Search icon is announced as belonging to a sub-menu.

### Suggested Remediation
1. Remove role="menubar".
2. Remove role="menuitem" from the child that has it.
3. Use a <nav> tag instead for the menu: <nav aria-label="Search and user menu">
4. Use native links and buttons.
