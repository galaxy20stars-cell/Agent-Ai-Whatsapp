# Blueprint — Réponse automatique aux questions fréquentes (WhatsApp)

*Créé : 2026-10-08 — validé par Latifa*

**Objectif :** répondre seul aux questions courantes sur SoiDoux, présenter le produit, et transférer à Latifa tout ce qui demande une personne.

**Entrées :** le message du client, l'historique de la conversation, `references/soidoux-knowledge-base.md`.

**Equipment :** pas encore construit. Il faudra un script Python qui reçoit les messages WhatsApp, appelle l'API Claude et envoie les notifications. Il sera choisi une fois l'accès WhatsApp confirmé (voir live/tasks.md).

## Étapes à chaque message

1. **Détecter la langue** : darija, arabe ou français, et répondre dans cette langue.
2. **Vérifier d'abord s'il faut passer la main** (liste ci-dessous). Si oui, aller à l'étape 5.
3. **Chercher la réponse dans la base de connaissances.** L'agent n'utilise que ce qui est marqué ✅.
4. **Répondre** sur un ton chaleureux, poli et rassurant. Messages courts, adaptés à WhatsApp. Si le client veut commander, recueillir ses informations.
5. **Passer la main** : dire au client, poliment, qu'une personne va prendre le relais. Ne rien promettre. Puis prévenir Latifa.

## Quand passer la main à Latifa

- Client en colère ou insatisfait
- Demande de remise ou de prix spécial
- Réclamation (commande, livraison, produit reçu)
- Demande de retour ou d'échange
- Santé ou peau : question médicale, réaction cutanée, allergie, grossesse, affection particulière
- Problème de paiement ou question financière inhabituelle
- Information absente de la base de connaissances, ou risque de répondre faux

## Ce que l'agent ne fait jamais

- Inventer une information (prix, délai, ville, composition…)
- Promettre un remboursement, une remise ou un geste commercial
- Donner un conseil qui ressemble à un avis médical

## Notification à Latifa

- **Canal :** WhatsApp sur son numéro personnel, avec Gmail en solution temporaire.
- **Contenu :** nom du client (si connu), son numéro, le motif du transfert, un résumé de la conversation.

## En cas d'échec

- Si l'API Claude ne répond pas : envoyer au client un message d'attente (« Nous revenons vers vous très vite »), puis prévenir Latifa.
- Si la notification WhatsApp échoue, prévenir par Gmail.

## Résultat attendu

Une réponse envoyée au client, ou un transfert propre vers Latifa avec sa notification.
