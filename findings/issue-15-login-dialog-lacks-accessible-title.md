## Issue: Login modal dialog lacks accessible title

### Description

On the Search Results page, a Login control opens a modal dialog. Screen readers announce it as a "dialog" but do not announce the visible dialog title (“Sign in / Register”). The visible title is not not programmatically associated with the dialog container.

As a result, the dialog does not have an accessible name, and thus its purpose is unclear to assistive technology users.

### Impact

Assistive technology users may be confused about what the dialog is for. This increases cognitive load and makes it harder to decide whether to keep the dialog open.

**WCAG 2.1 Reference:**  4.1.2 – Name, Role, Value  
**Severity:** Medium
**Affected users:** assistive technology users

### Evidence / notes
    - Screen reader announcement: “dialog” (title not announced)  
    - Visible title present: `<div class="login-title">Sign in / Register</div>`  
    - Dialog container lacks `aria-label` or `aria-labelledby`

### Recommended remediation

1. Give the dialog title an `id`.
2. Reference it from the dialog container with `aria-labelledby`.
