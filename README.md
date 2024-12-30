# CSS Specificity Issue with :has() Pseudo-class in Media Query

This repository demonstrates a subtle bug related to CSS specificity when using the `:has()` pseudo-class within a media query.  The problem arises from how the browser resolves specificity conflicts between selectors in different media query contexts.  The solution provides a way to resolve this issue.

## Bug Description

The provided CSS code intends to apply a red background to the `.container` element only when it contains an `.item` element and the screen width is less than 768px. However, due to specificity conflicts, the expected behavior might not occur in all cases.  The blue background might persist despite the presence of the `.item` element within the container.

## Solution

The solution involves increasing the specificity of the selector within the media query to ensure it overrides the default `.container` styles.  This is achieved by making the selector more precise.