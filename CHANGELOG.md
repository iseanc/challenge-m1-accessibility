# Change Log

## Summary
Documents specific changes made to code files

## Changes

FORMAT: Each heading item is an acceptance criteria, with bulleted list of changes.

*GIVEN a webpage meets accessibility standards...*

*WHEN I view the source code, THEN I find semantic HTML elements*
- Changed `<div class="header">` to `<header>` and CSS reference to element selector    
- Changed Navigation menu `<div></div>` to a <nav></nav> and updated CSS
- Enclosed all content between header and footer in `main` element.
- Changed main content dividers (`class="contents"` and `class="benefits"`) to from `div` to `section` elements.
- Rename `class=contents` to `class='services' to better represent content type.
- Change `<div class="footer"> </div>` to `<footer> </footer>`, updated CSS

*WHEN I view the structure of the HTML elements, THEN I find that the elements follow a logical structure independent of styling and positioning*

*WHEN I view the icon and image elements, THEN I find accessible alt attributes*
- No changes made to background image (`<div class="hero"`>). **Justification:** Background image is a "decorative image" and should be ignored by AT. See [Understanding WCAG 2.0 > Understanding SC 1.1.1](https://www.w3.org/TR/UNDERSTANDING-WCAG20/text-equiv-all.html#text-equiv-all-situation-f-notrequired). `div` elements are frequently ignored by AT. Chrome Dev Tools > Accessibility Tree shows this is ignored.
- Added empty `alt=""` attributes to all pictures so they're skipped by ATs.  **Justification:** these are non-text content already described by surrounding text.
- Removed heart symbol in footer text ("Made with ❤️️ by Horiseon"). Sentence now reads "Made by Horiseon".

*WHEN I view the heading attributes, THEN they fall in sequential order*
- Changes `footer > h2` tag to an `h3` so I can remove the `footer h2` CSS rule.
- Rename `.content` to `.services`

*WHEN I view the title element, THEN I find a concise, descriptive title*
- Set `<title>` to "Horiseon Marketing Services"

*Application's links all function correctly.*
- Added `id="search-engine-optimization"` to fix nav link
- All links (nav) tested successfully.

*Application's CSS selectors and properties are consolidated and organized to follow semantic structure.*
- Consolidated separate `.benefit-*` rules into a single rule for `.benefits div`
- Consolidated separate `.benefit-* h3` rules into a single rule for `.benefits h3`
- Consolidated separate `.benefit-* img` rules into a single rule for `.benefits img`
- Moved all `.benefits*` rules to end of CSS file, just before `footer` rules.
- Removed `footer h2` rule
- Consolidated separate `.services-* <div>, <img> and <h2>` rules into a single rules for each respect set of descendant elements under `section class="services">`
- Changed .benefits {background-color} to same as .services class to correct contrast warning found by WebAIM Web Accessibility Evaluation Tool (Chrome plug-in)

*Application's CSS file is properly commented.*

## Possible Future Changes

-  Consider revising h# elements.  I could not think of a better layout than it has now.