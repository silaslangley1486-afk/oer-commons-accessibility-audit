### Issue: Additional search results load without a status announcement

### Description

There is a "Load More" control at the bottom of the search results on the Search Results page. Activating it causes more search results to display without a full page reload. The control is exposed to the screen reader as a link and its label indicates that more search resuts will be loaded. But no status message is announced that confirms the new search results are successfully loaded.

The focus remains on the "Load More" link when it is activated. Without any notification confirming that more search results were added, the user must continue tabbing on the page to determine whether more search results were added.

### Impact:  

Screen readers can be become confused about whether more results were successfully loaded. As a result, screen readers may keep trying to activate the "Load More" link or navigate through the page unnecessarily to determine whether more results were loaded.

**WCAG 2.1 Reference:**  4.1.3 – Status Messages (AA)
**Severity:** Medium
**Affected users:** Screen reader users

**Recommended remediation:**  

Add a status message that announces the successful loading of more search results. E.g., "20 more search results loaded." Use an appropriate ARIA live region. Then users will clearly know that more search results were loaded and focus won't be disrupted.
