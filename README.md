# Agent IA WhatsApp

Agent IA qui répond automatiquement aux clients de **SoiDoux** sur WhatsApp : questions fréquentes, présentation du produit, prise d'informations de commande. Il transfère les cas sensibles à une personne.

**Stack :** Python + API Claude. WhatsApp est l'unique canal client.

## Où en est le projet

| Étape | Statut |
|---|---|
| Organisation du projet et règles de travail | ✅ Fait |
| Base de connaissances produit (prix, livraison, paiement, retours) | ✅ Fait |
| Procédure de l'agent : réponses et transferts vers un humain | ✅ Fait |
| Connexion à WhatsApp (API Meta) | ⏳ En cours de décision |
| Script Python de l'agent | 🔜 À construire |

## Ce que fait l'agent

- Répond seul aux 10 questions les plus fréquentes : prix, livraison, délai, paiement, utilisation…
- Répond dans la langue du client : darija, arabe ou français.
- Transfère à un humain : client mécontent, remise, réclamation, retour, question de santé ou de peau, information inconnue.
- N'invente jamais d'information et ne promet ni remboursement ni remise.

## Organisation des dossiers

| Dossier | Contenu |
|---|---|
| `blueprints/` | Procédures de l'agent. Commencer par `whatsapp-faq-auto-reply.md` |
| `references/` | Base de connaissances produit (`soidoux-knowledge-base.md`) et méthode de travail |
| `equipment/` | Scripts Python (à venir) |
| `decisions/ledger.md` | Registre des décisions prises, à ne pas remettre en question |
| `intel/` | Contexte du projet : objectifs, outils, priorités |
| `live/` | État d'avancement et tâches ouvertes |
| `.claude/rules/` | Règles de ton, de permissions et de relation client |
| `templates/` | Modèles de documents |

## Méthode

Le projet suit le **Three Engine Model** : une procédure écrite (Blueprint) guide chaque tâche, et des scripts (Equipment) exécutent les parties techniques. Détails dans `references/three-engine-model.md`.

## Sécurité

Les clés API et les identifiants vont uniquement dans un fichier `.env`, qui n'est jamais envoyé sur GitHub. Un modèle est fourni : `.env.example`.
