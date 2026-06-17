# Squarespace Dropdown Navigation Redirect Fix

A reusable JavaScript snippet for improving Squarespace 7.1 dropdown navigation behavior when folder-style navigation items need to redirect to actual landing pages.

## What it solves

Squarespace dropdown folders are often used to organize top-level navigation items such as Programs, About, Services, or Resources.

In some Squarespace 7.1 setups, these folder-style navigation items behave mainly as dropdown triggers instead of regular clickable links. This can create a UX issue where users can open the dropdown, but clicking the parent navigation label does not reliably send them to the intended main landing page.

For example:

* `/programs-hub` can redirect to `/programs`
* `/about-hub` can redirect to `/about`

This is useful when the website structure depends on clear primary navigation paths and the top-level navigation label should behave like a real landing page link.

## How it works

The script listens for clicks on selected Squarespace navigation links and folder title elements. When a matching item is clicked, it prevents the default folder behavior and redirects the user to the correct landing page URL.

It checks multiple possible Squarespace attributes and selectors, including:

* `href`
* `data-href`
* `.header-nav-folder-title[data-href]`

This helps the snippet work across different Squarespace header states and responsive layouts.

## Additional functionality

The script also initializes simple reveal animations for elements using the `.reveal-card` class.

When a `.reveal-card` element enters the viewport, the script adds the `.is-visible` class once. This allows cards or content blocks to animate into view without affecting the navigation redirect behavior.

## How to customize

Update the redirect pairs inside the `redirects` array:

```js
const redirects = [
  { old: "/old-folder-url", new: "/new-landing-page-url" }
];
```

Add more redirect pairs as needed.

## Best used for

* Squarespace 7.1 websites
* Dropdown folder navigation
* Parent navigation labels that need to redirect
* Program, About, Services, Resources, or Donate navigation structures
* Nonprofit and service business websites with deeper navigation

## Notes

This is a generalized reusable snippet. Client-specific content, project names, private URLs, and implementation details have been removed or generalized.

