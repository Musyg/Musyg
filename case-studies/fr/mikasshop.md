[English](../en/mikasshop.md) · **Français**

# Mika's Shop

[Voir la boutique](https://mikasshop.com)

![Mika, le chat à l'origine de Mika's Shop](../../assets/case-studies/mikasshop-social.jpg)

_Visuel officiel de Mika's Shop récupéré sur la boutique publique le 14 août 2026._

Début du projet : 2024.

## Présentation

Mika est le vrai chat qui incarne la marque Mika's Shop. Derrière la boutique Shopify, j’ai développé un assistant conversationnel IA, des agents e-commerce et SAV, des parcours de relation client et l’analyse des événements. La navigation propose des entrées par profil de chat ou catégorie de produits ; l’assistant guide les visiteurs à partir du catalogue et des contenus du site.

## Rôle et périmètre

J’ai conçu et réalisé la boutique, du thème, de la navigation et des collections à la localisation, aux contenus éditoriaux et à la mise en ligne. J’ai aussi développé l’interface et le backend de l’assistant conversationnel, ses outils d’accès au catalogue et aux contenus du site, ainsi que l’intégration de l’agent SAV de la boutique.

Le travail comprend aussi les parcours de relation client aux couleurs de la marque, un pixel de suivi maison, la transmission de KPI à l’Analytics Hub et un parcours éditorial qui prépare des brouillons français et anglais à partir des produits, à relire avant publication.

## Problème et contraintes

La boutique devait proposer une manière claire d’associer les produits à différents comportements de chats tout en conservant un parcours e-commerce familier et localisé.

## Architecture

Shopify fournit le commerce hébergé, le catalogue, la localisation, le panier et le passage en caisse. Le thème de la vitrine organise les collections par type de produit et profil de chat, les contenus multilingues, les pages éditoriales et les informations clients.

L’assistant de la boutique s’appuie sur un service Python/FastAPI et des appels d’outils pour le conseil produit, la recherche dans le catalogue, les stocks, les politiques de la boutique et les liens de navigation. Un widget affiche les réponses via SSE. Un service SAV distinct gère les demandes d’assistance, les brouillons, les validations et les transmissions à un opérateur, avec MQTT pour relier le parcours de validation.

Le backend e-commerce apporte la recherche catalogue via FAISS, ainsi que les connaissances métier et les politiques de la boutique via Qdrant. Les prix et disponibilités proviennent d’outils dédiés de lecture Shopify. Le parcours éditorial prépare des brouillons à partir des produits ; des skills de contenu et de SEO décrivent les consignes propres aux tâches et les méthodes éditoriales.

Le pixel maison collecte les événements de la boutique, notamment les vues produit, ajouts au panier et étapes d’achat. La chaîne d’analyse stocke, agrège et attribue ces événements, puis transmet des KPI à l’Analytics Hub via MQTT. Les agents SAV et e-commerce émettent également des événements métier destinés à l’analyse.

## Choix et compromis

Shopify conserve le paiement et le commerce, tandis que les services sur mesure prennent en charge le conseil et l’assistance. Les outils de l’assistant portent sur les informations du site, pas sur le suivi de commandes ni les achats. Le SAV suit un parcours distinct, avec un mode de réponse configurable et une transmission à un opérateur ; il ne se confond pas avec l’assistant public.

## Résultats publics

La boutique publique est en ligne avec des contenus en anglais, français et allemand, des régions et devises localisées, des collections de produits, des contenus éditoriaux et un guide d’adoption téléchargeable.

## Périmètre et état actuel

La boutique est en ligne. L’assistant IA et les intégrations SAV sont développés.

## Ressources et liens

- [Présentation sur le portfolio](https://musyg.com/fr/realisations/mikasshop/)
- [Boutique publique](https://mikasshop.com)

Le code des intégrations métier est privé.
