**English** · [Français](../fr/inaricom.md)

# Inaricom

[Visit Inaricom](https://inaricom.com)

![Inaricom logo](../../assets/case-studies/inaricom-logo.png)

_Official Inaricom logo retrieved from the site's public WordPress media library on 2026-08-14._

Project started: 2023.

## Summary

Inaricom brings together services, technical publishing and commerce. I develop its WordPress/WooCommerce backend and React interfaces, alongside agents for ecommerce operations, customer support and sales workflows.

## Role and scope

I develop the website and backend: WordPress content models, custom PHP plugins and REST endpoints, React interfaces, contact flows and deployment tooling. I also built a DigiKey integration to search and import product references into WooCommerce, enrich product information and update prices and availability.

I also develop Inaricom’s business services: ecommerce tools, document-grounded support and a sales-agent chain for prospecting, qualification, negotiation, closing and follow-up. The work includes quote and contract preparation, client acceptance and PDF invoicing modules linked to WooCommerce orders. I built a WooCommerce tracking pixel and the event-to-KPI pipeline feeding Analytics Hub.

## Problem and constraints

The goal is to combine service content, technical publishing, contact and quote paths, and e-commerce while retaining the established content and commerce backend.

## Architecture

A custom PHP plugin defines content models, taxonomies, structured data, REST endpoints, and conditional React mount points. Vite builds page-specific React 19 and TypeScript interfaces while WooCommerce retains catalogue and purchase flows.

A separate supplier integration connects the DigiKey API to WooCommerce products. It maps descriptions, images and technical attributes, with manual updates and a scheduled price and stock synchronisation mechanism. A custom contact endpoint connects the website form to WordPress mail handling.

Python/FastAPI services connect the ecommerce agent to WooCommerce catalogue, stock and order information. Catalogue retrieval uses FAISS; Qdrant provides ecommerce knowledge and store-specific support documents. These sources inform the support workflow and response preparation.

The sales-agent chain connects prospecting, qualification, negotiation and closing. The commercial case retains the quote, contract, operator approval and client acceptance. Dedicated PHP modules link PDF invoice generation and archiving to the accepted quote, WooCommerce order and payment receipt.

The tracking pixel collects storefront events; analytics services aggregate and attribute them before publishing KPI snapshots to Analytics Hub over MQTT. Business-agent events provide a second input to the analysis pipeline.

## Decisions and trade-offs

React is loaded only where an interface needs it. Classic WordPress and WooCommerce pages remain available, and the custom layer focuses on services, content, structured data, and interactions rather than reimplementing commerce.

I separate catalogue retrieval, store documents and sales context so each workflow uses the appropriate source. Qualification and document preparation are distinct from approval, signature and payment.

## Scope and current status

The supplier and contact-backend integrations are developed. The sales-agent chain and its quote-to-invoice workflow are being integrated.

## Resources and links

- [Portfolio case study](https://musyg.com/work/inaricom/)
- [Visit Inaricom](https://inaricom.com)

Business integration source code is private.
