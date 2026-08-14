**English** · [Français](../fr/inaricom.md)

# Inaricom

[Visit the public site](https://inaricom.com)

![Inaricom logo](../../assets/case-studies/inaricom-logo.png)

_Official Inaricom logo retrieved from the site's public WordPress media library on 2026-08-14._

## Summary

Inaricom is a WordPress business website that combines cybersecurity service pages, packaged offers, a WooCommerce catalogue, and long-form technical publishing.

The public site presents web, infrastructure, cloud, and smart-contract services alongside commerce and articles on local AI, language models, hardware, and tutorials.

## Role and scope

Gilles Musy developed the website and its backend integration. The work covered:

- WordPress site structure and theme customization;
- navigation, service landing pages, offer presentation, and responsive page composition;
- WooCommerce catalogue, pricing, cart, checkout, account, and order paths;
- quote and contact interfaces;
- technical articles, author pages, categories, and editorial navigation;
- country-aware currency presentation;
- legal, privacy, refund, terms, acceptable-use, and cookie pages;
- production deployment and ongoing content changes.

The implementation uses WordPress and WooCommerce as the application and commerce backend. This case study does not describe a bespoke commerce engine.

## Web and backend structure

The public delivery and application structure observed during verification was:

```text
Cloudflare
`-- Caddy delivery layer
    `-- WordPress
        |-- theme, navigation, and service pages
        |-- articles, authors, and categories
        |-- contact and quote interfaces
        `-- WooCommerce catalogue and purchase paths
```

The website keeps service discovery, commercial offers, technical content, and e-commerce within one publishing and administration system.

## Selected decisions

- Separate landing pages give web, infrastructure, and smart-contract services their own scope and calls to action.
- Packaged offers provide a direct order route while custom work uses a quote path.
- The editorial section groups technical material by topic instead of mixing every article into a single feed.
- WooCommerce supports catalogue browsing, prices, cart actions, and account or order paths.
- The site can present CHF or EUR according to the visitor context and offers a manual currency choice.

## Security and operations

Public response headers identify Cloudflare and a Caddy delivery layer. The observed response also included a content security policy, HSTS, frame restrictions, a referrer policy, and a permissions policy.

This is a web-development case study. The site's descriptions of security services are first-party commercial content, not independent evidence of an audit result. No claim is made that the site itself has undergone an independent security audit.

## Public verification

Checked against current public responses and indexed site snapshots on 2026-08-14:

- public index snapshots exposed the homepage and the web-audit service page;
- the public media path, page structure, and indexed content identify WordPress;
- the indexed shop exposed WooCommerce-style sorting, prices, catalogue items, and cart controls;
- the homepage exposed three service families, packaged offers, quote links, article categories, contact, and policy navigation;
- a technical guide was publicly attributed to Gilles Musy;
- the official logo and `robots.txt` remained directly reachable.

Direct requests to the dynamic pages from the verification environment received HTTP 503 with a `Retry-After` header. Current availability was therefore not asserted, and no order or form was submitted.

## Public evidence

- [Public site](https://inaricom.com)
- [Web service page](https://inaricom.com/audit-web/)
- [WooCommerce catalogue](https://inaricom.com/shop/)
- [Technical guide by Gilles Musy](https://inaricom.com/2026/01/23/installer-un-assistant-ia-local-ollama-open-webui-guide-2025/)
- [Terms and refund policy](https://inaricom.com/refund-policy/)

## Limits

- Current availability could not be confirmed because the automated verification environment received HTTP 503 responses.
- No purchase, account creation, quote request, or contact-form submission was performed.
- Sales, conversion, traffic, and revenue figures are not public and are not claimed here.
- The site's own security-service descriptions are not treated as third-party validation.
- Public content and commercial offers can change after the verification date.
