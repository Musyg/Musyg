**English** · [Français](../fr/inaricom.md)

# Inaricom

[Project URL, rebuild in progress](https://inaricom.com)

![Inaricom logo](../../assets/case-studies/inaricom-logo.png)

_Official Inaricom logo retrieved from the site's public WordPress media library on 2026-08-14._

## Summary

Inaricom is a WordPress business website that is currently being rebuilt. Its previously indexed public version combined cybersecurity service pages, packaged offers, a WooCommerce catalogue, and long-form technical publishing.

The documented version brought together web, infrastructure, cloud, and smart-contract services alongside commerce and articles on local AI, language models, hardware, and tutorials.

## Current status

The owner confirms that Inaricom is being rebuilt. The public URL can return HTTP 503 while the new version is under construction. Indexed pages and earlier public content therefore document the project history and an earlier public surface, not the final rebuilt release.

## Role and scope

Gilles Musy developed the website and its backend integration. The work covered:

- WordPress site structure and theme customization;
- navigation, service landing pages, offer presentation, and responsive page composition;
- WooCommerce catalogue, pricing, cart, checkout, account, and order paths;
- quote and contact interfaces;
- technical articles, author pages, categories, and editorial navigation;
- country-aware currency presentation;
- legal, privacy, refund, terms, acceptable-use, and cookie pages;
- production deployment and content changes to the documented version.

The documented implementation used WordPress and WooCommerce as the application and commerce backend. This case study does not describe a bespoke commerce engine.

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

The documented version kept service discovery, commercial offers, technical content, and e-commerce within one publishing and administration system.

## Selected decisions

- Separate landing pages gave web, infrastructure, and smart-contract services their own scope and calls to action.
- Packaged offers provided a direct order route while custom work used a quote path.
- The editorial section grouped technical material by topic instead of mixing every article into a single feed.
- WooCommerce supported catalogue browsing, prices, cart actions, and account or order paths.
- The documented version presented CHF or EUR according to the visitor context and offered a manual currency choice.

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

Direct requests to the dynamic pages received HTTP 503 with a `Retry-After` header while the rebuild was in progress. This is recorded as the current construction state, not as an availability incident. No order or form was submitted.

## Public evidence

- [Project URL](https://inaricom.com)
- [Web service page](https://inaricom.com/audit-web/)
- [WooCommerce catalogue](https://inaricom.com/shop/)
- [Technical guide by Gilles Musy](https://inaricom.com/2026/01/23/installer-un-assistant-ia-local-ollama-open-webui-guide-2025/)
- [Terms and refund policy](https://inaricom.com/refund-policy/)

## Limits

- This is interim documentation for a project under active rebuild and must be refreshed after relaunch.
- Indexed snapshots can describe an earlier or partial version rather than the final rebuilt site.
- No purchase, account creation, quote request, or contact-form submission was performed.
- Sales, conversion, traffic, and revenue figures are not public and are not claimed here.
- The site's own security-service descriptions are not treated as third-party validation.
- Public content and commercial offers can change after the verification date.
