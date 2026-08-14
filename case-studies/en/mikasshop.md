**English** · [Français](../fr/mikasshop.md)

# Mika's Shop

[Visit the live store](https://mikasshop.com)

![Mika, the cat behind Mika's Shop](../../assets/case-studies/mikasshop-social.jpg)

_Official Mika's Shop image retrieved from the live storefront on 2026-08-14._

## Summary

Mika's Shop is a Shopify store for cat and pet products. Its main merchandising choice is to group toys by the cat they suit, including kittens, easy-going cats, hunters, and sensitive cats, rather than relying only on product categories.

The storefront combines a product catalogue, localized shopping, editorial content, and a free adoption guide.

## Role and scope

Gilles Musy designed and implemented the Shopify store end to end. The work covered:

- store structure and storefront configuration;
- theme customization and page composition;
- collections, navigation, product pages, and product variants;
- English, French, and German storefronts;
- country, region, and currency selection through Shopify Markets;
- cart, checkout, shipping, returns, policy, and contact pages and flows;
- the blog, the brand story, and the downloadable guide;
- launch of the public store.

He was the sole implementer for this scope.

## Commerce and content structure

Shopify provides the hosted commerce layer, catalogue, localization, cart, and checkout. The storefront adds the customer-facing structure:

```text
Shopify
|-- theme and page composition
|-- product catalogue and variants
|-- collections by product type and cat profile
|-- Markets, languages, regions, and currencies
|-- cart, checkout, shipping, and returns
`-- blog, guide, policies, and contact pages
```

The platform was kept deliberately hosted rather than introducing a custom backend. This reduces operational overhead while retaining Shopify's standard commerce workflow.

## Selected decisions

- Products can be discovered by cat profile as well as by conventional category.
- Noise sensitivity is part of the product-selection language for sensitive cats.
- Editorial content supports the catalogue without hiding the store behind a content site.
- The adoption guide is available as an 18-page PDF without a sign-up requirement.
- Localization uses three storefront languages and a country or region selector with local currencies.

## Security and operations

Checkout and payment handling use Shopify's managed commerce flow. This case study does not claim a custom payment implementation or an independent security audit.

The public storefront exposes shipping, returns, privacy, terms, legal notice, contact information, and cookie-preference pages. Their presence is recorded here without making a legal-compliance claim.

## Public verification

Verified against the live storefront on 2026-08-14:

- the home, About, product, blog, and guide pages were reachable;
- English, French, and German were offered in the language selector;
- the country or region selector exposed local currencies;
- a sample product page exposed variants, quantity, cart, shipping, returns, and secure-checkout information;
- the free guide was linked as an 18-page PDF with no sign-up.

No test purchase was made during this verification.

## Public evidence

- [Live store](https://mikasshop.com)
- [Brand and product-selection rationale](https://mikasshop.com/pages/about-us)
- [New cat checklist and downloadable guide](https://mikasshop.com/blogs/news/new-cat-checklist-welcoming-guide)
- [Sample product page](https://mikasshop.com/products/quick-drying-pet-towel)

## Limits

- Sales, conversion, traffic, and revenue figures are not public and are not claimed here.
- Product availability, prices, markets, and storefront content can change after the verification date.
- The commerce backend is Shopify, not a bespoke application backend.
