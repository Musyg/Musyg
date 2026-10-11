**English** · [Français](../fr/mikasshop.md)

# Mika's Shop

[Visit the live store](https://mikasshop.com)

![Mika, the cat behind Mika's Shop](../../assets/case-studies/mikasshop-social.jpg)

_Official Mika's Shop image retrieved from the live storefront on 2026-08-14._

Project started: 2024.

## Summary

Mika is the real cat at the heart of the Mika's Shop brand. Behind the Shopify storefront, I developed an AI store assistant, ecommerce and support agents, customer-relationship workflows and event analytics. Visitors can browse by cat profile or product category; the assistant guides them using catalogue and site information.

## Role and scope

I designed and built the storefront, from the theme, navigation and collections to localization, editorial content and launch. I also developed the store’s AI assistant interface and backend, its catalogue and site-content tools, and its customer-support agent integration.

The work also includes branded customer-relationship workflows, a custom tracking pixel, KPI delivery to Analytics Hub and an editorial workflow that prepares French and English product-based drafts for review.

## Problem and constraints

The store needed a clear way to match products to different cat behaviors while still preserving a familiar, localized e-commerce journey.

## Architecture

Shopify provides hosted commerce, catalogue, localization, cart, and checkout. The storefront theme organizes collections by product type and cat profile, multilingual content, editorial pages, and customer information.

The store’s AI assistant uses a Python/FastAPI service with tool calls for product advice, catalogue search, stock, store policies and navigation links. A browser widget displays responses over SSE. A separate customer-support service handles support requests, response drafts, operator approval and escalation pathways, with MQTT connecting the approval workflow.

The ecommerce backend supplies catalogue retrieval through FAISS and business knowledge and store policies through Qdrant. Product prices and availability come from dedicated Shopify-reading tools. The content workflow prepares product-based drafts; content and SEO skills document task-specific instructions and editorial methods.

The custom pixel collects storefront events such as product views, cart additions and purchase steps. The analytics pipeline stores, aggregates and attributes events, then sends KPI snapshots to Analytics Hub via MQTT. Support and ecommerce agents also emit business events for analysis.

## Decisions and trade-offs

Shopify retains checkout and commerce while custom services handle guidance and support. The assistant’s tool set focuses on site information rather than order lookup or purchases. Customer support follows a separate workflow with configurable response routing and operator escalation; it is not the public shopping chat.

## Public results

The public store is live with English, French, and German content, localized regions and currencies, product collections, editorial content, and a downloadable adoption guide.

## Scope and current status

The store is online. The AI assistant and customer-support integrations are developed.

## Resources and links

- [Portfolio case study](https://musyg.com/work/mikasshop/)
- [Live store](https://mikasshop.com)

Business integration source code is private.
