## Issue: Selected radio button option is distinguished by color only

### Description

On the Search Results page, there is a radio button group that has a "view detail" option and a "view list" option. See /screenshots/view-controls.png. The selected option is indicated only through a change in color/lightness (blue to gray). No non-color visual indicator (such as a checkmark, radio dot, shape change, or text) is provided to convey selection state. The difference is distinguishable in grayscale due to a change in the lightness of the gray, and thus may not impact users with a color impairment. However, the contrast between the two shades of gray is 1.94:1 which is less than the required contrast of 3:1.


### Impact

Not everyone sees color in the same way. So only using a color indicator makes it difficult for users with color impairments to determine which option is selected. Color-impaired users may still be able to tell which one is selected by the difference in lightness between the selected and unselected otpion. However, the contrast is slight and users with color and vision impairments may still struggle to tell which option is selected.

**WCAG 2.1:** 1.4.1 Use of Color (A)  
**Severity:** Medium  
**Affected users:** color and vision impaired users

### Suggested Remediation

1. Provide another visual indicator to distinguish between the selected and unselected options. Make both options look like radio buttons and place a dot in the middle for the selected option, or add some other visual indicator that would work for both the circle option and the list icon option.

2. Increase the contrast between the selected and non-selected options so that it is easier to distinguish them in grayscale.