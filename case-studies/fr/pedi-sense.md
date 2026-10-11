[English](../en/pedi-sense.md) · **Français**

# Pedi-Sense

[Voir la boutique](https://pedi-sense.com)

![Chaussettes séparatrices d'orteils Pedi-Sense présentées dans une ambiance de soirée](../../assets/case-studies/pedi-sense-storefront.jpg)

_Visuel officiel de Pedi-Sense récupéré sur la boutique publique le 14 août 2026._

Début du projet : Fin 2022.

## Présentation

Pedi-Sense associe une boutique Shopify à des agents e-commerce et SAV, des emails aux couleurs de la marque, une recherche catalogue et l’analyse des événements. Le travail couvre la boutique visible par les clients et les parcours métier qui l’accompagnent.

## Rôle et périmètre

J’ai conçu et réalisé la boutique, de la composition du thème et des options produit à la localisation, aux contenus et à la mise en ligne. J’ai aussi développé les intégrations métier de Pedi-Sense, notamment les parcours SAV, les emails aux couleurs de la marque et la collecte des événements de la boutique.

J’ai développé l’intégration du pixel de suivi et le parcours des événements jusqu’aux KPI de l’Analytics Hub. Les agents sont aussi reliés à la recherche sémantique du catalogue et aux connaissances e-commerce, avec des parcours de contenu et de SEO développés pour la boutique.

## Problème et contraintes

Un catalogue ciblé a besoin d’une structure suffisante pour les variantes, les offres par lot, les informations pratiques, l’assistance, la localisation et les contenus éditoriaux sans masquer le parcours d’achat.

## Architecture

Shopify prend en charge le catalogue, les comptes, le panier et le paiement. Des services Python relient les agents e-commerce et SAV aux informations de produit, de stock et de commande. Le SAV prépare les réponses à valider et les transmissions à un opérateur ; les automatisations email couvrent confirmations de commande, paniers abandonnés et expéditions via Listmonk.

La recherche catalogue utilise FAISS, tandis que Qdrant apporte les connaissances e-commerce, les politiques et les FAQ de la boutique. Le parcours de contenu et de SEO comprend des consignes de tâche documentées sous forme de skills. Les faits du catalogue, les documents SAV et les méthodes éditoriales restent ainsi distincts.

L’intégration du pixel maison collecte les événements de navigation et du parcours d’achat. Les services d’analyse les stockent, les agrègent et leur attribuent des canaux, puis publient des KPI vers l’Analytics Hub via MQTT. Les événements émis par les agents métier alimentent aussi la chaîne d’analyse.

## Choix et compromis

J’ai conservé le paiement dans Shopify tout en développant les parcours métier séparément. Le SAV comprend des brouillons à valider et une transmission à un opérateur. Les modèles d’emails couvrent les confirmations de commande, les paniers abandonnés et les expéditions.

## Résultats publics

La boutique en ligne présente un parcours d’achat complet en français, anglais, allemand, italien et espagnol, avec des régions, devises, choix de produits, informations clients et contenus éditoriaux localisés.

## Périmètre et état actuel

La boutique est en ligne. Les services d’agents et les intégrations backend sont développés.

## Ressources et liens

- [Présentation sur le portfolio](https://musyg.com/fr/realisations/pedi-sense/)
- [Boutique publique](https://pedi-sense.com)

Le code des intégrations métier est privé.
