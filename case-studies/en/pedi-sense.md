**English** · [Français](../fr/pedi-sense.md)

# Pedi-Sense

[Visit the live store](https://pedi-sense.com)

![Pedi-Sense toe separator socks presented in an evening setting](../../assets/case-studies/pedi-sense-storefront.jpg)

_Official Pedi-Sense storefront image retrieved from the live site on 2026-08-14._

## Summary

Pedi-Sense is a Shopify store focused on toe separator socks. The storefront explains a single core product through its intended moments of use, colour and pack options, localized content, and a complete purchasing journey.

The site combines commerce, brand content, customer-support information, and editorial articles in five languages.

## Role and scope

Gilles Musy designed and implemented the Shopify store end to end. The work covered:

- store architecture and Shopify configuration;
- theme customization, visual composition, and navigation;
- the product catalogue, product page, colour variants, and pack options;
- French, English, German, Italian, and Spanish storefronts;
- country, region, and currency selection through Shopify Markets;
- cart, checkout, customer-account, order-tracking, shipping, and return flows;
- the brand story, FAQ, contact, policy, and editorial pages;
- canonical and language-alternate metadata for the localized storefront;
- launch of the public store.

He was the sole implementer for this scope.

## Commerce and content structure

Shopify provides the hosted commerce layer, catalogue, localization, cart, and checkout. The public storefront organizes the customer journey:

```text
Shopify
|-- theme, navigation, and page composition
|-- product catalogue, colours, and pack options
|-- Markets, five languages, regions, and currencies
|-- cart, checkout, accounts, shipping, and returns
|-- brand story, FAQ, policies, and contact
`-- blog and localized search metadata
```

The store uses Shopify's hosted backend instead of a bespoke commerce service. This keeps product, order, localization, and checkout operations within the platform's standard workflow.

## Selected decisions

- A focused catalogue gives the main product enough room for clear use, material, sizing, and care information.
- Colour selection and one, two, or three-pair options are integrated into the product journey.
- Five storefront languages share the same commercial structure while keeping localized routes.
- The homepage declares a canonical URL plus French, English, German, Italian, Spanish, and default language alternates.
- The brand story, FAQ, contact flow, policies, and blog support both purchase decisions and after-sales questions.

## Security and operations

Checkout and payment handling use Shopify's managed commerce flow. This case study does not claim a custom payment implementation or an independent security audit.

The public storefront exposes shipping, returns, privacy, terms, legal notice, contact, and cookie-preference pages. Their presence is recorded without making a legal-compliance claim.

This case study documents the store implementation. It does not independently validate product or health claims made in the storefront content.

## Public verification

Verified against the live storefront on 2026-08-14:

- the home, product, brand story, FAQ, contact, policy, and blog pages were reachable;
- French, English, German, Italian, and Spanish were offered in the language selector;
- the country or region selector exposed local currencies;
- the product page exposed eight colour options, one, two, or three-pair choices, cart and buy-now controls, shipping details, and returns information;
- the homepage exposed a canonical URL and matching language-alternate metadata.

No test purchase was made during this verification.

## Public evidence

- [Live store](https://pedi-sense.com)
- [Product page](https://pedi-sense.com/products/chaussettes-separatrices-orteils)
- [Brand story](https://pedi-sense.com/pages/notre-histoire)
- [FAQ](https://pedi-sense.com/pages/faq-questions-frequentes)
- [Editorial articles](https://pedi-sense.com/blogs/articles-de-pedi-sense)

## Limits

- Sales, conversion, traffic, and revenue figures are not public and are not claimed here.
- Product effects and customer statements are not treated as independently verified evidence.
- Products, prices, markets, and storefront content can change after the verification date.
- The commerce backend is Shopify, not a bespoke application backend.
