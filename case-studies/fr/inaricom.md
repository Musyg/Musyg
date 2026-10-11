[English](../en/inaricom.md) · **Français**

# Inaricom

[Voir Inaricom](https://inaricom.com)

![Logo Inaricom](../../assets/case-studies/inaricom-logo.png)

_Logo officiel d'Inaricom récupéré dans la médiathèque WordPress publique du site le 14 août 2026._

Début du projet : 2023.

## Présentation

Inaricom réunit services, publication technique et commerce. Je développe son backend WordPress/WooCommerce et ses interfaces React, ainsi que les agents destinés aux opérations e-commerce, au SAV et aux parcours commerciaux.

## Rôle et périmètre

Je développe le site et son backend : modèles de contenu WordPress, extensions PHP et points d’accès REST dédiés, interfaces React, parcours de contact et outils de déploiement. J’ai également créé une intégration DigiKey pour rechercher et importer des références dans WooCommerce, enrichir les fiches produits et mettre à jour les prix et disponibilités.

Je développe aussi les services métier d’Inaricom : outils e-commerce, assistance fondée sur les documents et chaîne d’agents commerciaux pour la prospection, la qualification, la négociation, le closing et le suivi. Le travail comprend la préparation des devis et contrats, l’acceptation client et les modules de facturation PDF reliés aux commandes WooCommerce. J’ai créé un pixel de suivi WooCommerce et la chaîne d’événements et de KPI destinée à l’Analytics Hub.

## Problème et contraintes

L’objectif est de réunir les contenus de services, la publication technique, les parcours de contact et de devis ainsi que l’e-commerce en conservant le backend éditorial et commercial existant.

## Architecture

Une extension PHP dédiée définit les modèles de contenu, les taxonomies, les données structurées, les points d’accès REST et les points de montage conditionnels de React. Vite construit des interfaces React 19 et TypeScript propres à chaque page, tandis que WooCommerce conserve le catalogue et les parcours d’achat.

Une intégration fournisseur distincte relie l’API DigiKey aux produits WooCommerce. Elle associe descriptions, images et caractéristiques techniques, avec des mises à jour manuelles et un mécanisme de synchronisation programmé des prix et stocks. Un point d’accès dédié relie le formulaire de contact à l’envoi de courriels WordPress.

Des services Python/FastAPI relient l’agent e-commerce aux informations de catalogue, de stock et de commande de WooCommerce. La recherche dans le catalogue utilise FAISS ; Qdrant apporte les connaissances e-commerce et les documents SAV du site. Ces sources alimentent le parcours d’assistance et la préparation des réponses.

La chaîne d’agents commerciaux relie prospection, qualification, négociation et closing. Le dossier commercial conserve le devis, le contrat, la validation opérateur et l’acceptation du client. Des modules PHP dédiés relient la génération et l’archivage des factures PDF au devis accepté, à la commande WooCommerce et au reçu de paiement.

Le pixel collecte les événements du site ; les services d’analyse les agrègent et leur attribuent des canaux avant de transmettre les KPI à l’Analytics Hub via MQTT. Les événements des agents métier constituent une seconde entrée de la chaîne d’analyse.

## Choix et compromis

React n’est chargé que lorsqu’une interface en a besoin. Les pages WordPress et WooCommerce classiques restent disponibles et la couche dédiée se concentre sur les services, les contenus, les données structurées et les interactions plutôt que de réimplémenter le commerce.

Je distingue recherche catalogue, documents du site et contexte commercial pour fournir les bonnes sources à chaque parcours. La qualification et la préparation documentaire restent des étapes distinctes de la validation, de la signature et du paiement.

## Périmètre et état actuel

Les intégrations fournisseur et backend de contact sont développées. La chaîne d’agents commerciaux et son parcours devis-facturation sont en cours d’intégration.

## Ressources et liens

- [Présentation sur le portfolio](https://musyg.com/fr/realisations/inaricom/)
- [Voir Inaricom](https://inaricom.com)

Le code des intégrations métier est privé.
