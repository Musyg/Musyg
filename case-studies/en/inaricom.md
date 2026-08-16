**English** · [Français](../fr/inaricom.md)

# Inaricom

[Project URL, rebuild in progress](https://inaricom.com)

![Inaricom logo](../../assets/case-studies/inaricom-logo.png)

_Official Inaricom logo retrieved from the site's public WordPress media library on 2026-08-14._

## Summary

Inaricom is a business, services, and commerce website under active rebuild. The current implementation combines a WordPress and WooCommerce backend with page-specific React interfaces, rather than replacing the publishing and commerce system with a standalone application.

The project brings together service pages, commercial offers, technical publishing, contact and quote paths, and e-commerce. Its content covers Web, infrastructure, cloud, AI, cybersecurity, and smart-contract services.

## Current status

The rebuild is in progress. The public URL currently returns HTTP 503 while the new version is under construction, so it should not be treated as a completed public release.

The current architecture below was confirmed through a read-only review of the private working repository on 2026-08-16. The earlier public surface remains documented separately because the rebuilt version cannot yet be verified end to end from the public site.

## Role and scope

Gilles Musy is responsible for the website and backend development. The work includes:

- WordPress site structure, theme integration, navigation, service pages, and responsive composition;
- WooCommerce catalogue, pricing, cart, checkout, account, and order paths;
- a custom PHP plugin for content models, taxonomies, structured data, theme mapping, and React integration;
- React 19 and TypeScript interfaces built with Vite and Tailwind CSS 4;
- custom WordPress REST endpoints for articles, categories, contact handling, and legal content;
- quote and contact interfaces;
- technical publishing, author pages, categories, and editorial navigation;
- country-aware currency presentation;
- legal, privacy, refund, terms, acceptable-use, and cookie pages;
- deployment, content migration, and production changes.

WordPress and WooCommerce remain the application and commerce backend. This case study does not describe a bespoke commerce engine.

## Current rebuild architecture

```text
Cloudflare and Caddy delivery
`-- WordPress
    |-- WooCommerce commerce backend
    |-- custom PHP plugin
    |   |-- content types and taxonomy
    |   |-- structured data and theme mapping
    |   |-- custom REST endpoints
    |   `-- conditional React mount points and bundle loading
    `-- React islands
        |-- React 19 and TypeScript
        |-- Vite and Tailwind CSS 4
        `-- page-specific interfaces using WordPress data
```

The React build currently contains separate entry points for the homepage, blog, contact, legal, AI, cybersecurity, and Web, infrastructure, and smart-contract audit pages. Vite produces hashed assets and a manifest that the WordPress plugin reads to load only the interface required by the current page.

The blog interface retrieves posts through a dedicated WordPress REST namespace with TanStack Query. The same backend layer provides purpose-specific routes for contact and legal content. Classic WordPress and WooCommerce pages remain available where a React interface is not required.

## Backend and delivery decisions

- Custom post types separate resources, case studies, and services from ordinary pages and posts.
- A shared taxonomy groups content by business pillar.
- Structured-data handling is implemented in the custom plugin, including product schema enrichment when the relevant SEO integration is active.
- React bundles are integrated into WordPress through page mount points and conditional loading instead of shipping one frontend bundle across the entire site.
- Shared and heavy frontend dependencies are split into reusable or on-demand chunks.
- The custom REST namespace can avoid loading WooCommerce and other non-required plugins for those requests, reducing memory pressure on the hosting environment.
- WooCommerce continues to own catalogue and purchase workflows, while the custom code focuses on presentation, content, and service-specific interactions.

## Earlier public version

The previously indexed version already included separate service landing pages, packaged offers, quote paths, a WooCommerce catalogue, technical articles, policy pages, and CHF or EUR presentation according to visitor context. These elements document the project history but do not represent the final rebuilt interface.

## Security and operations

Public response headers identify Cloudflare and a Caddy delivery layer. The observed response also included a content security policy, HSTS, frame restrictions, a referrer policy, and a permissions policy.

This is a Web-development case study. The site's descriptions of security services are first-party commercial content, not independent evidence of an audit result. No claim is made that the site itself has undergone an independent security audit.

## Verification basis

The current rebuild details were checked against the private working repository on 2026-08-16. The review confirmed the PHP plugin modules, WordPress integration, React source entries, Vite build configuration, REST data flow, and WooCommerce boundary. It did not expose private source code, credentials, infrastructure secrets, customer data, or internal commercial documents.

Public checks performed on 2026-08-14 confirmed the WordPress and WooCommerce history, the public media path, and indexed content. A separate check on 2026-08-16 confirmed that the public site still returned the construction-state HTTP 503 response. No order or form was submitted.

## Public evidence

- [Project URL](https://inaricom.com)
- [Web service page](https://inaricom.com/audit-web/)
- [WooCommerce catalogue](https://inaricom.com/shop/)
- [Technical guide by Gilles Musy](https://inaricom.com/2026/01/23/installer-un-assistant-ia-local-ollama-open-webui-guide-2025/)
- [Terms and refund policy](https://inaricom.com/refund-policy/)

## Limits

- This is interim documentation for a project under active rebuild and must be refreshed after relaunch.
- The rebuilt interface cannot yet be verified end to end from the public site.
- Private-repository verification supports the described implementation, but does not make the private source publicly reproducible.
- Indexed snapshots can describe an earlier or partial version rather than the final rebuilt site.
- No purchase, account creation, quote request, or contact-form submission was performed.
- Sales, conversion, traffic, and revenue figures are not public and are not claimed here.
- The site's own security-service descriptions are not treated as third-party validation.
- Public content and commercial offers can change after the verification date.
