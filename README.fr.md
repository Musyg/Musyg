[English](./README.md) · **Français**

# Chercheur en sécurité · Développeur · Ingénieur en systèmes d’IA

Basé en Suisse.

Trois pratiques professionnelles distinctes, chacune présentée séparément ci-dessous.

---

## 🔒 Recherche en sécurité

**Chercheur en sécurité**

J’identifie et démontre des failles de sécurité dans les applications web, les smart contracts et les systèmes d’IA.
Chaque vulnérabilité confirmée est étayée par des preuves reproductibles et un impact clairement défini.

**Domaines**
- Sécurité web et applicative : applications web, API, contrôle d’accès, logique métier et intégrations
- Smart contracts : Solidity / Vyper, preuves de concept sur forks avec Foundry, vérification formelle
- ZK et cryptographie appliquée : circuits, vérificateurs et systèmes de preuve
- Sécurité des systèmes d’IA et des agents : injection indirecte de prompts, détournement d’outils, chemins d’attaque agentiques et évaluation adversariale

**Réalisations vérifiables**
- Gray Swan Arena : [GilMu](https://app.grayswan.ai/arena/user/6a3043c8221a153764c96ab5), recherche sur l’injection indirecte de prompts et évaluation adversariale de systèmes d’IA.
- [security-reviews](https://github.com/Musyg/security-reviews), un catalogue d’audits reproductibles avec un dépôt par classe de vulnérabilité. Chacun comprend une cible vulnérable, une preuve de concept d’exploitation, une branche corrigée et un rapport, le tout validé par CI.
- [erc4626-inflation-audit](https://github.com/Musyg/erc4626-inflation-audit). Inflation des parts ERC-4626 lors du premier dépôt.
- [eip712-signature-replay-audit](https://github.com/Musyg/eip712-signature-replay-audit). Malléabilité de signature ECDSA permettant une double dépense.
- [reward-accounting-drift-audit](https://github.com/Musyg/reward-accounting-drift-audit). Dérive de comptabilisation des récompenses de type MasterChef.
- [stvault-audit](https://github.com/Musyg/stvault-audit). Coffre de prêt : obsolescence de l’oracle, réentrance interfonctionnelle et arrondi des frais.
- [vyper-access-control-audit](https://github.com/Musyg/vyper-access-control-audit). Coffre Vyper : transfert de propriété non protégé.
- [circom-underconstrained-audit](https://github.com/Musyg/circom-underconstrained-audit). ZK : circuit Circom sous-contraint compromettant la solidité de Groth16.
- [formal-verification-overflow-audit](https://github.com/Musyg/formal-verification-overflow-audit). Vérification formelle : débordement dans le calcul d’une moyenne, d’abord réfuté puis démontré avec Halmos.

**Profils de compétition**
- Cantina : [@GilMu](https://cantina.xyz/u/GilMu)
- Code4rena : [@GiMu84](https://code4rena.com/@GiMu84)

---

## 💻 Développement

**Ingénieur backend et infrastructure**

Services Python résilients, conçus en priorité autour de l’asynchrone, et briques d’infrastructure qui assurent leur disponibilité.

- [production-agent-template](https://github.com/Musyg/production-agent-template). Modèle de service FastAPI pour la production : cycle de vie, état de santé, circuit breaker, auto-rétablissement, métriques et génération de structure.
- [agent-resilience](https://github.com/Musyg/agent-resilience). Circuit breaker, file de messages en échec adossée à Redis et tampon MQTT hors ligne.
- [async-api-client](https://github.com/Musyg/async-api-client). Client REST asynchrone résilient : limitation de débit, nouvelles tentatives et pagination.
- [agent-self-healing](https://github.com/Musyg/agent-self-healing). Surveillance de l’état des dépendances avec états disponible, dégradé et erreur, ainsi que récupération automatique.
- [agent-metrics](https://github.com/Musyg/agent-metrics). Compteurs, jauges et histogrammes sans dépendances, avec exposition au format texte Prometheus.
- [infra-reference](https://github.com/Musyg/infra-reference). Référence d’ingénierie de plateforme sans données sensibles : Ansible multi-architecture, systemd renforcé, builds distroless, réseau maillé et observabilité.

_Missions : API backend, intégrations, observabilité et CI._

---

## 🤖 IA et systèmes agentiques

**Ingénieur en systèmes d’IA appliqués et agentiques**

Je conçois et développe des systèmes multi-agents autonomes dotés de pipelines de construction et d’audit auto-améliorés. Ils reposent principalement sur des modèles locaux orchestrés sur une petite flotte de machines.

- [talos](https://github.com/Musyg/talos). Plateforme agentique distribuée : environ 55 agents et plus de 85 services sur une flotte de quatre nœuds, mémoire en quatre parties, assistant vocal et conversationnel en temps réel, et pipelines de construction auto-améliorés.
- [multi-agent-orchestrator](https://github.com/Musyg/multi-agent-orchestrator). Modèle de routage des tâches fondé sur les capacités.

**Stack** : Python orienté asynchrone · exploitation de LLM locaux (llama.cpp / GGUF, routage de modèles, bascule tenant compte de la VRAM) · orchestration multi-agent · mémoire graph-RAG · recherche vectorielle · bus d’événements MQTT · voix en temps réel · Prometheus / VictoriaMetrics · systemd · CI (ruff, pytest, pre-commit).

---

## Ma méthode

- Les preuves avant les affirmations : si ce n’est pas reproductible, ce n’est pas terminé.
- Une approche guidée par les métriques : chaque changement est mesuré.
- La vérification par l’exécution prime sur le résultat d’un essai unique.

## Autre réalisation

- [inaricom.com](https://inaricom.com) : j’ai développé leur site web et leur backend.
