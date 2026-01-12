# OER Commons Accessibility Audit (WCAG 2.1 AA)

This repository contains a scoped, independent accessibility audit of a public education technology platform, conducted for professional development and portfolio purposes.

## Executive Summary

This repository documents an independent WCAG 2.1 Level AA accessibility audit of key user flows on OER Commons. The audit is primarily based on manual accessibility evaluation, including keyboard navigation, screen reader checks, and DOM inspection. Axe-based automated scans were used as a diagnostic aid to surface potential issues, with all relevant findings manually verified. Identified accessibility barriers are mapped to WCAG success criteria and accompanied by remediation guidance.

## Scope
- Site: OER Commons, https://oercommons.org/ (public pages only)
- Flow audited:
  - Search results
  - Filter interactions
  - Resource detail page
- Viewports:
  - Desktop (1280x800)
  - Mobile (375x667)
- Standards: WCAG 2.1 Level AA

Note: This audit includes the opening and closing of the Login Modal on the Resource detail page, but not the modal's content.

## Methodology
- Automated scanning was performed using the axe DevTools browser extension. Results were manually reviewed and validated as part of the audit process.

- Automated scanning using axe-core
- Manual keyboard-only testing
- Screen reader spot checks (NVDA)
- Responsive accessibility verification

Automated tools were used as an initial signal only. All reported issues were manually validated.

## Deliverables
- Full audit report (PDF)
- Individual issue documentation with remediation guidance
- Sample Playwright + axe-core test

## Disclaimer
This audit was conducted independently for educational purposes.
