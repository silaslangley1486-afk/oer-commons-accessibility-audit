## Methodology

Automated scanning using the axe DevTools browser extension was performed on representative pages.
Results were grouped by issue type, and representative instances were manually validated.
Repeated or low-impact findings were not individually documented.

Medium severity issues significantly affect usability or comprehension but do not fully block task completion.

## Notes on Semantic Assessment

Some interactive controls in this audit use anchor (`<a>`) elements rather than buttons. Where anchors include valid `href` attributes and represent navigational or pagination behavior, they were not treated as violations of WCAG 2.1 4.1.2 (Name, Role, Value). In these cases, accessibility findings focused instead on status communication, e.g, WCAG 2.1 4.1.3 (Status Messages).
