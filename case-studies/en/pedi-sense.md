**English** · [Français](../fr/pedi-sense.md)

# Pedi-Sense

[Visit the live store](https://pedi-sense.com)

![Pedi-Sense toe separator socks presented in an evening setting](../../assets/case-studies/pedi-sense-storefront.jpg)

_Official Pedi-Sense storefront image retrieved from the live site on 2026-08-14._

Project started: Late 2022.

## Summary

Pedi-Sense combines a Shopify storefront with ecommerce and support agents, branded email workflows, catalogue retrieval and event analytics. The work covers the customer-facing store and the business workflows behind it.

## Role and scope

I designed and implemented the storefront, from theme composition and product options to localization, content and launch. I also developed Pedi-Sense’s business integrations, including customer-support workflows, branded emails and storefront event collection.

I built the store’s tracking-pixel integration and the event-to-KPI path into Analytics Hub. The agent workflows also connect to semantic catalogue retrieval and ecommerce knowledge, with content and SEO workflows developed for the store.

## Problem and constraints

A focused catalogue needs enough structure for product variants, bundle options, practical information, customer support, localization, and editorial content without obscuring the purchase path.

## Architecture

Shopify handles the catalogue, accounts, cart and checkout. Python services connect ecommerce and support agents to product, stock and order information. The support workflow prepares responses for review and escalation; branded email workflows cover order confirmations, abandoned carts and shipping through Listmonk.

Catalogue retrieval uses FAISS, while Qdrant provides ecommerce knowledge and store-specific policies and FAQs. The content and SEO workflow includes task instructions documented as skills. This separates catalogue facts, support documents and editorial methods.

The store’s custom pixel integration collects navigation and purchase-path events. Analytics services store, aggregate and attribute them, then publish KPI snapshots to Analytics Hub over MQTT. Events emitted by the business agents feed the analysis pipeline too.

## Decisions and trade-offs

I kept checkout within Shopify while developing business workflows separately. Support includes draft responses for review and escalation to an operator. Email templates cover order confirmations, abandoned carts and shipping notifications.

## Public results

The live store presents a complete purchase journey in French, English, German, Italian, and Spanish, with localized regions, currencies, product choices, customer information, and editorial content.

## Scope and current status

The store is online. The agent services and backend integrations are developed.

## Resources and links

- [Portfolio case study](https://musyg.com/work/pedi-sense/)
- [Live store](https://pedi-sense.com)

Business integration source code is private.
