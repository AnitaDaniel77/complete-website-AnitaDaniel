# Complete Website Capstone — Portfolio Site

A personal portfolio website built to satisfy the Complete Website capstone brief: debugging and completing a partially broken starter site using only HTML and CSS.

## How to View

1. Clone this repository:

git clone https://github.com/AnitaDaniel77/complete-website-AnitaDaniel.git

2. Open the folder in VS Code (or any editor).
3. Open `index.html` directly in a browser, or use the VS Code "Live Server" extension for auto-reload while viewing.
4. Navigate between pages using the nav bar (Home, About, Projects, Contact).

No build step, server, or dependencies required this is a static HTML/CSS site.

## Overview

The starter repository was roughly 70% complete, with 25 intentional HTML errors and 16 CSS errors spread across `index.html`, `about.html`, `projects.html`, `contact.html`, and `styles.css`. The task was to identify and fix all issues, then complete the site with real personal content: my background, real projects, and working contact details.

## Issues Found

A full list of 18 identified issues is documented in `design/Issues Document.docx`, alongside the wireframe in `design/wireframe.pdf`. In summary, the starter code had:
- No semantic HTML tags anywhere (all `<div>`s)
- No navigation menu on any page
- Missing `<meta charset>` and `lang` attributes
- Missing `alt` text on all images
- A missing data table and a missing third project
- An incomplete, unlabelled contact form with no validation
- No navigation styling, poor colour contrast in the hero and footer, and missing box model usage throughout the CSS

## Fixes Implemented

- Replaced all non-semantic `<div>`s with `<header>`, `<nav>`, `<main>`, `<section>`, and `<footer>`
- Added a consistent 4-link navigation menu to all pages
- Added `<meta charset="UTF-8">` and `lang="en"` to every page
- Added descriptive `alt` text to every image
- Added a Skills table with proper `<thead>`/`<tbody>` structure
- Completed the contact form with 5 input types, linked `<label>`s, and 3 HTML5 validation attributes (`required`, `pattern`, `minlength`)
- Added the missing third project
- Styled the navigation with flexbox and a hover state
- Fixed both colour contrast failures (hero and footer) to meet the 4.5:1 WCAG minimum
- Added consistent box model styling (margin, padding, border) across sections, the table, and the form

## HTML/CSS Approach

I structured each page around a `<header>` (with nested `<nav>`), a `<main>` wrapping the page's core content in `<section>`s, and a shared `<footer>`. This keeps the semantic structure identical across all four pages, so the CSS selectors (`header`, `nav ul`, `footer`, etc.) apply consistently everywhere rather than needing page-specific overrides. For CSS, I used a mix of element, class, descendant, combination (`th, td`), and pseudo-class (`:hover`) selectors to meet the variety requirement while keeping the stylesheet readable, with comments marking each fix.

## Accessibility Improvements

- Every image has descriptive `alt` text rather than being left blank or missing
- All form inputs have associated `<label>` elements linked via matching `for`/`id` pairs, so screen readers announce each field correctly
- Both flagged colour contrast failures were corrected to meet the WCAG 4.5:1 minimum ratio
- Semantic landmarks (`<header>`, `<nav>`, `<main>`, `<footer>`) let assistive technology users jump directly to key page regions instead of reading through unlabelled `<div>`s

## Reflection

The most valuable part of this capstone was realising how much of "good HTML" is really about intent, not appearance a `<div>` and a `<nav>` can look identical in the browser but mean completely different things to a screen reader or search engine. Debugging someone else's flawed code also forced me to slow down and check every element against a checklist rather than trusting that it "looked right." The colour contrast failure in the footer was a good example: it looked fine visually, but only testing the actual ratio caught the problem. Going forward, I want to build accessibility and validation checks into my process from the start of a project, rather than as a fix-up step at the end.