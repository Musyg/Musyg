[English](../en/inaricom.md) · **Français**

# Inaricom

[URL du projet, refonte en cours](https://inaricom.com)

![Logo Inaricom](../../assets/case-studies/inaricom-logo.png)

_Logo officiel d'Inaricom récupéré dans la médiathèque WordPress publique du site le 14 août 2026._

## Présentation

Inaricom est un site professionnel sous WordPress qui fait actuellement l'objet d'une refonte. Sa version publique précédemment indexée réunissait des pages de services en cybersécurité, des offres structurées, un catalogue WooCommerce et des contenus techniques détaillés.

La version documentée rassemblait des services consacrés au Web, à l'infrastructure, au cloud et aux smart contracts, ainsi qu'une partie commerciale et des articles sur l'IA locale, les modèles de langage, le matériel et les tutoriels.

## État actuel

Le propriétaire confirme qu'Inaricom est en cours de refonte. L'URL publique peut répondre en HTTP 503 pendant la construction de la nouvelle version. Les pages indexées et les anciens contenus publics documentent donc l'historique et une version publique antérieure, et non la version finale après refonte.

## Rôle et périmètre

Gilles Musy a développé le site et son intégration backend. Son intervention a couvert :

- la structure du site WordPress et la personnalisation du thème ;
- la navigation, les pages de services, la présentation des offres et la composition responsive ;
- le catalogue WooCommerce, les prix, le panier, le passage en caisse, le compte et le suivi des commandes ;
- les interfaces de devis et de contact ;
- les articles techniques, les auteurs, les catégories et la navigation éditoriale ;
- la présentation de la devise selon le pays ;
- les pages juridiques, de confidentialité, de remboursement, de conditions, d'utilisation acceptable et de gestion des cookies ;
- la mise en production et l'évolution des contenus de la version documentée.

L'implémentation documentée utilisait WordPress et WooCommerce pour l'application et le backend commercial. Cette étude de cas ne décrit pas un moteur e-commerce développé sur mesure.

## Structure Web et backend

La chaîne de diffusion et la structure applicative observées pendant la vérification étaient les suivantes :

```text
Cloudflare
`-- couche de diffusion Caddy
    `-- WordPress
        |-- thème, navigation et pages de services
        |-- articles, auteurs et catégories
        |-- interfaces de contact et de devis
        `-- catalogue WooCommerce et parcours d'achat
```

La version documentée regroupait la découverte des services, les offres commerciales, les contenus techniques et l'e-commerce dans un même système de publication et d'administration.

## Choix principaux

- Des pages distinctes donnaient aux services Web, infrastructure et smart contracts leur propre périmètre et leurs propres appels à l'action.
- Les offres structurées disposaient d'un parcours de commande direct, tandis que les missions sur mesure passaient par une demande de devis.
- La partie éditoriale classait les contenus techniques par thème au lieu de les réunir dans un flux unique.
- WooCommerce prenait en charge le catalogue, les prix, les actions du panier ainsi que les parcours de compte et de commande.
- La version documentée présentait les prix en CHF ou en EUR selon le contexte du visiteur et proposait un choix manuel de devise.

## Sécurité et exploitation

Les en-têtes de réponse publics identifient Cloudflare et une couche de diffusion Caddy. La réponse observée comprenait également une politique de sécurité des contenus, HSTS, des restrictions d'intégration dans une page tierce, une politique de référent et une politique de permissions.

Il s'agit ici d'une étude de cas de développement Web. Les descriptions des services de sécurité présentes sur le site sont des contenus commerciaux de première partie et non des preuves indépendantes de résultats d'audit. Cette étude ne prétend pas non plus que le site a fait l'objet d'un audit de sécurité indépendant.

## Vérification publique

Éléments contrôlés à partir des réponses publiques actuelles et des instantanés indexés du site le 14 août 2026 :

- les instantanés publics indexés présentaient l'accueil et la page consacrée au service d'audit Web ;
- le chemin de la médiathèque publique, la structure des pages et les contenus indexés identifient WordPress ;
- la boutique indexée présentait le tri, les prix, les éléments du catalogue et les commandes de panier caractéristiques de WooCommerce ;
- l'accueil présentait trois familles de services, des offres structurées, des liens de devis, les catégories d'articles, le contact et les pages de politiques ;
- un guide technique était publiquement attribué à Gilles Musy ;
- le logo officiel et le fichier `robots.txt` restaient accessibles directement.

Les requêtes directes vers les pages dynamiques ont reçu une réponse HTTP 503 avec un en-tête `Retry-After` pendant la refonte. Cette réponse est consignée comme l'état actuel du chantier et non comme un incident de disponibilité. Aucune commande ni aucun formulaire n'a été soumis.

## Preuves publiques

- [URL du projet](https://inaricom.com)
- [Page du service Web](https://inaricom.com/audit-web/)
- [Catalogue WooCommerce](https://inaricom.com/shop/)
- [Guide technique signé Gilles Musy](https://inaricom.com/2026/01/23/installer-un-assistant-ia-local-ollama-open-webui-guide-2025/)
- [Conditions de vente et de remboursement](https://inaricom.com/refund-policy/)

## Limites

- Ce document est provisoire pour un projet en cours de refonte et devra être actualisé après la remise en ligne.
- Les instantanés indexés peuvent décrire une version antérieure ou partielle plutôt que le site final après refonte.
- Aucun achat, aucune création de compte, aucune demande de devis ni aucun envoi de formulaire de contact n'a été effectué.
- Les chiffres de vente, de conversion, d'audience et de chiffre d'affaires ne sont pas publics et ne sont pas revendiqués ici.
- Les descriptions des services de sécurité du site ne sont pas considérées comme une validation par un tiers.
- Les contenus publics et les offres commerciales peuvent évoluer après la date de vérification.
