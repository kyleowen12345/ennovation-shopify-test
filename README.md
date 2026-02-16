# KeeWee — Custom Shopify Sections

Custom product page sections built on the Shopify Horizon theme, pixel-perfect to the provided Figma design. All content is fully editable from the Shopify customizer using sections, snippets, and theme blocks.

## Sections

### Product Detail (`kw-product-detail`)
- Image gallery auto-pulls from product media with thumbnail navigation and arrow controls
- Quantity selector and Add to Cart via Shopify AJAX Cart API
- Collapsible "About" section with feature bullets (block-based)
- Subscription tiers with editable save badges and free shipping toggles
- Shipping accordion with icon and text per line (block-based)

### Logo Carousel (`kw-logo-carousel`)
- Infinite marquee scroll using pure CSS (no JavaScript)
- Hardware-accelerated with `translate3d` for smooth performance
- Pauses on hover, respects `prefers-reduced-motion`

### Feature Grid (`kw-feature-grid`)
- Background image with glassmorphic overlay cards
- Each card is a block with customizable icon, title, description, and colors
- Horizontal layout on desktop, stacked on mobile

### Testimonial (`kw-testimonial`)
- Combined doctor/product photo with quote, name, and title
- Lora (serif) and Public Sans (sans-serif) typography matching Figma specs
- Each testimonial is a block

### Community Gallery (`kw-community-gallery`)
- Horizontal drag-to-scroll on desktop, swipe on mobile
- Social links with customizable highlight color
- Each photo is a block with image picker

## File Structure

```
sections/
├── kw-product-detail.liquid
├── kw-logo-carousel.liquid
├── kw-feature-grid.liquid
├── kw-testimonial.liquid
└── kw-community-gallery.liquid

snippets/
├── kw-feature-item.liquid
├── kw-icon-check.liquid
├── kw-subscription-option.liquid
├── kw-ingredient-card.liquid
├── kw-testimonial-card.liquid
├── kw-gallery-photo.liquid
├── kw-logo-item.liquid
└── kw-social-link.liquid

assets/
├── kw-product-detail.css
├── kw-logo-carousel.css
├── kw-feature-grid.css
├── kw-testimonial.css
└── kw-community-gallery.css
```

## Tech Stack

- Shopify Liquid
- HTML / CSS
- JavaScript (vanilla)
- Shopify Horizon Theme (v3.3.1)

## Approach

- **Sections + Blocks pattern**: Every piece of content is managed through Shopify's native section and block system, giving the client full control from the customizer without touching code.
- **Snippets for reusability**: Repeated components (feature items, subscription options, testimonial cards, etc.) are extracted into snippets.
- **Namespaced with `kw-` prefix**: All classes, files, and selectors are prefixed to avoid conflicts with the base Horizon theme.
- **Responsive design**: All sections include mobile breakpoints and adapt to different screen sizes.
- **Performance**: CSS-only animations where possible, lazy loading on images, minimal JavaScript.

## Setup

1. Clone the repository
2. Connect to your Shopify store using [Shopify CLI](https://shopify.dev/docs/themes/tools/cli) or GitHub integration
3. Run `shopify theme dev` for local development
4. Add sections to any page via the Shopify customizer
