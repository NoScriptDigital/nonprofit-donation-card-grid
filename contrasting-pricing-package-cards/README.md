# Squarespace Contrasting Pricing Package Cards

A reusable HTML and CSS layout for presenting two pricing, accommodation, membership, or package options with contrasting visual treatments.

## What it solves

Squarespace Fluid Engine can become difficult to manage when a pricing card requires several layers of content and precise internal styling.

A complex card may include:

* Eyebrow text
* Package title
* Large pricing typography
* Supporting pricing labels
* Description copy
* Availability information
* A featured badge
* A call-to-action button
* Multiple color variations

Building each part with separate Squarespace blocks can require many individual elements and make it difficult to maintain consistent padding, spacing, alignment, and card height.

The native grid may also make it difficult to keep both cards elegant, minimal, and visually balanced.

This snippet places each package inside one structured card so all content can be controlled as a complete component.

## Layout behavior

The layout displays two equal-width cards on desktop.

Each card uses a different visual treatment:

* A light card for one package option
* A dark card for the featured or alternative package
* An optional badge for the highlighted selection

On smaller screens, the cards stack into one column.

## Key features

* Two-column desktop pricing layout
* Single-column mobile layout
* Equal-height package cards
* Contrasting light and dark card variations
* Optional featured badge
* Multiple typography sizes
* Bottom-aligned CTA buttons
* Responsive pricing typography
* Custom availability labels
* Customizable colors through CSS variables
* No JavaScript required

## Best used for

* Retreat room packages
* Service packages
* Pricing tiers
* Membership plans
* Accommodation options
* Coaching programs
* Event packages
* Course enrollment options
* Squarespace Code Blocks

## Files

* `index.html`
* `styles.css`

## Live Preview

View the demo here:

https://noscriptdigital.github.io/squarespace-code-snippets/contrasting-pricing-package-cards/

## Squarespace implementation

Place the complete card HTML inside a Squarespace Code Block.

Add the CSS through:

```text
Design → Custom CSS
```

The CSS can also be included inside a `<style>` element when the component is used on only one page.

## Card variations

Apply the light variation with:

```html
<article class="pricing-card pricing-card--light">
```

Apply the dark variation with:

```html
<article class="pricing-card pricing-card--dark">
```

## Adding a featured badge

Add the badge inside the card:

```html
<span class="pricing-card__badge">
  Most Popular
</span>
```

Remove it from cards that do not need featured treatment.

## Keeping buttons aligned

Each card uses a vertical flex layout:

```css
.pricing-card {
  display: flex;
  flex-direction: column;
}
```

The button uses:

```css
margin-top: auto;
```

This keeps the CTA aligned at the bottom even when the cards contain different amounts of copy.

## Customization

Update the reusable color variables at the top of `styles.css`.

Change package names, prices, availability labels, badges, descriptions, and CTA links inside the HTML.

## Accessibility notes

Use heading levels that fit the surrounding page structure.

Make sure button labels clearly describe the destination or action.

Do not rely only on color to identify the featured package. Include a visible badge or descriptive text.

## Notes

This is a generalized reusable example.

Client-specific names, prices, package descriptions, brand colors, links, and private implementation details have been removed or replaced.

