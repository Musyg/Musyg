[English](../en/inaricom.md) · **Français**

# Inaricom

[URL du projet, refonte en cours](https://inaricom.com)

![Logo Inaricom](../../assets/case-studies/inaricom-logo.png)

_Logo officiel d'Inaricom récupéré dans la médiathèque WordPress publique du site le 14 août 2026._

## Présentation

Inaricom est un site professionnel de services et de commerce qui fait actuellement l'objet d'une refonte. L'implémentation en cours associe un backend WordPress et WooCommerce à des interfaces React propres à chaque page, sans remplacer le système de publication et de commerce par une application autonome.

Le projet réunit des pages de services, des offres commerciales, des contenus techniques, des parcours de contact et de devis ainsi qu'une partie e-commerce. Ses contenus couvrent le Web, l'infrastructure, le cloud, l'IA, la cybersécurité et les smart contracts.

## État actuel

La refonte est en cours. L'URL publique répond actuellement en HTTP 503 pendant la construction de la nouvelle version. Elle ne doit donc pas être présentée comme une version publique terminée.

L'architecture actuelle décrite ci-dessous a été confirmée par une revue en lecture seule du dépôt de travail privé le 16 août 2026. L'ancienne version publique reste documentée séparément, car la nouvelle version ne peut pas encore être vérifiée de bout en bout depuis le site public.

## Rôle et périmètre

Gilles Musy prend en charge le développement du site et du backend. Son travail comprend :

- la structure du site WordPress, l'intégration du thème, la navigation, les pages de services et la composition responsive ;
- le catalogue WooCommerce, les prix, le panier, le passage en caisse, le compte et le suivi des commandes ;
- une extension PHP dédiée aux modèles de contenu, aux taxonomies, aux données structurées, aux thèmes visuels et à l'intégration de React ;
- des interfaces en React 19 et TypeScript construites avec Vite et Tailwind CSS 4 ;
- des points d'accès REST WordPress dédiés aux articles, aux catégories, au contact et aux contenus juridiques ;
- les interfaces de devis et de contact ;
- les contenus techniques, les auteurs, les catégories et la navigation éditoriale ;
- la présentation de la devise selon le pays ;
- les pages juridiques, de confidentialité, de remboursement, de conditions, d'utilisation acceptable et de gestion des cookies ;
- le déploiement, la migration des contenus et les évolutions en production.

WordPress et WooCommerce restent le backend applicatif et commercial. Cette étude de cas ne présente pas WooCommerce comme un moteur e-commerce développé sur mesure.

## Architecture de la refonte actuelle

```text
Diffusion par Cloudflare et Caddy
`-- WordPress
    |-- backend commercial WooCommerce
    |-- extension PHP dédiée
    |   |-- types de contenus et taxonomie
    |   |-- données structurées et thèmes visuels
    |   |-- points d'accès REST dédiés
    |   `-- points de montage et chargement conditionnel de React
    `-- îlots React
        |-- React 19 et TypeScript
        |-- Vite et Tailwind CSS 4
        `-- interfaces propres à chaque page alimentées par WordPress
```

La construction React contient actuellement des entrées distinctes pour l'accueil, le blog, le contact, les pages juridiques, l'IA, la cybersécurité et les pages d'audit Web, infrastructure et smart contracts. Vite produit des fichiers versionnés par leur empreinte ainsi qu'un manifeste que l'extension WordPress utilise pour ne charger que l'interface nécessaire à la page consultée.

L'interface du blog récupère les articles dans un espace REST WordPress dédié avec TanStack Query. La même couche backend fournit des routes adaptées au contact et aux contenus juridiques. Les pages WordPress et WooCommerce classiques restent utilisées lorsqu'une interface React n'est pas nécessaire.

## Choix backend et diffusion

- Des types de contenus dédiés séparent les ressources, les études de cas et les services des pages et articles ordinaires.
- Une taxonomie commune classe les contenus selon les piliers d'activité.
- La gestion des données structurées est intégrée à l'extension dédiée, avec un enrichissement du schéma produit lorsque l'intégration SEO concernée est active.
- Les fichiers React sont intégrés à WordPress par des points de montage et un chargement conditionnel, au lieu d'envoyer un seul ensemble frontend sur tout le site.
- Les dépendances frontend communes ou volumineuses sont placées dans des fichiers partagés ou chargés à la demande.
- L'espace REST dédié peut éviter de charger WooCommerce et d'autres extensions inutiles pour ces requêtes afin de réduire la consommation de mémoire sur l'hébergement.
- WooCommerce conserve la gestion du catalogue et des parcours d'achat, tandis que le code dédié se concentre sur la présentation, les contenus et les interactions propres aux services.

## Version publique antérieure

La version précédemment indexée comprenait déjà des pages de services distinctes, des offres structurées, des parcours de devis, un catalogue WooCommerce, des articles techniques, des pages de politiques et une présentation des prix en CHF ou en EUR selon le contexte du visiteur. Ces éléments documentent l'historique du projet, mais ne représentent pas l'interface finale après refonte.

## Sécurité et exploitation

Les en-têtes de réponse publics identifient Cloudflare et une couche de diffusion Caddy. La réponse observée comprenait également une politique de sécurité des contenus, HSTS, des restrictions d'intégration dans une page tierce, une politique de référent et une politique de permissions.

Il s'agit ici d'une étude de cas de développement Web. Les descriptions des services de sécurité présentes sur le site sont des contenus commerciaux de première partie et non des preuves indépendantes de résultats d'audit. Cette étude ne prétend pas non plus que le site a fait l'objet d'un audit de sécurité indépendant.

## Base de vérification

Les éléments concernant la refonte ont été contrôlés dans le dépôt de travail privé le 16 août 2026. La revue a confirmé les modules de l'extension PHP, l'intégration WordPress, les entrées React, la configuration de construction Vite, les échanges REST et la limite entre le code dédié et WooCommerce. Elle n'a exposé aucun code source privé, identifiant, secret d'infrastructure, donnée client ni document commercial interne.

Les contrôles publics réalisés le 14 août 2026 ont confirmé l'historique WordPress et WooCommerce, le chemin de la médiathèque publique et les contenus indexés. Un contrôle distinct effectué le 16 août 2026 a confirmé que le site public renvoyait toujours la réponse HTTP 503 correspondant à l'état de construction. Aucune commande ni aucun formulaire n'a été soumis.

## Preuves publiques

- [URL du projet](https://inaricom.com)
- [Page du service Web](https://inaricom.com/audit-web/)
- [Catalogue WooCommerce](https://inaricom.com/shop/)
- [Guide technique signé Gilles Musy](https://inaricom.com/2026/01/23/installer-un-assistant-ia-local-ollama-open-webui-guide-2025/)
- [Conditions de vente et de remboursement](https://inaricom.com/refund-policy/)

## Limites

- Ce document reste provisoire pour un projet en cours de refonte et devra être actualisé après la remise en ligne.
- La nouvelle interface ne peut pas encore être vérifiée de bout en bout depuis le site public.
- La revue du dépôt privé confirme l'implémentation décrite, mais ne rend pas le code privé reproductible publiquement.
- Les instantanés indexés peuvent décrire une version antérieure ou partielle plutôt que le site final après refonte.
- Aucun achat, aucune création de compte, aucune demande de devis ni aucun envoi de formulaire de contact n'a été effectué.
- Les chiffres de vente, de conversion, d'audience et de chiffre d'affaires ne sont pas publics et ne sont pas revendiqués ici.
- Les descriptions des services de sécurité du site ne sont pas considérées comme une validation par un tiers.
- Les contenus publics et les offres commerciales peuvent évoluer après la date de vérification.
