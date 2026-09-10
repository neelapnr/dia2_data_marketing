# Hypotheses pour la presentation (a completer)

## 1. Champions = forte concentration du CA
- Fait : 3068 clients (6,21% de la base) generent 43% du CA total
- Insight : une petite minorite de clients porte quasiment la moitie du business
- Recommandation : programme de fidelisation VIP priorise sur ce segment

## 2. Clients invites (sans compte)
- Fait : 22,77% des transactions n'ont pas de customer_id (22,7% du CA)
- Insight : pres d'un quart du chiffre d'affaires echappe totalement au suivi client, impossible de savoir si ce sont des nouveaux ou des habitues, donc impossible de les cibler ou mesurer leur fidelite
- Recommandation : inciter a la creation de compte au moment du paiement (offre, avantages fidelite) pour mieux suivre ces clients



## 3. Arbitrage volume vs qualite entre canaux
- Fait : sur les clients uniques ayant converti (dernier clic, touchpoints.csv), affiliate ramene le plus de clients (16 693) mais la plus faible part de Champions (15,4%). Search_paid ramene le moins de clients (10 323) mais la part de Champions la plus elevee (19,5%)
- Insight : le canal le plus performant en volume n'est pas forcement le plus qualitatif en valeur client. Juger un canal seulement sur son nombre de conversions (comme le CPA classique) fait passer a cote de cet arbitrage
- Recommandation : ponderer l'allocation budgetaire par la qualite du client acquis (part de Champions, potentiel CLTV) en plus du CPA/ROAS pur, pas seulement sur le volume brut de conversions

---
(a completer au fur et a mesure du TP2 et TP3)

---

## TP Storytelling - Partie 1 (analyser et faire emerger un insight)

**Etape 1 - 5 faits marquants**
1. 3068 clients (6,21% de la base) generent 43% du CA total
2. 22,77% des transactions n'ont pas de customer_id (22,7% du CA)
3. Affiliate ramene le plus de clients uniques convertis (16 693) mais la plus faible part de Champions (15,4%)
4. Search_paid ramene le moins de clients (10 323) mais la part de Champions la plus elevee (19,5%)
5. La base clients est tres polarisee : Champions (6,2%) et Perdus (6,3%) sont minoritaires, 83,3% des clients se situent entre ces deux extremes

**Etape 2 - Variable a expliquer**
La probabilite qu'un client acquis devienne un client a forte valeur (Champion)

**Etape 3 - Hypotheses**
- "Je pense que le canal d'acquisition influence la probabilite qu'un client devienne Champion"
- "Je pense que l'absence de compte client (customer_id manquant) limite la capacite a faire progresser un client vers le statut Champion"

**Etape 4 - Patterns identifies**
- Volume et qualite de client ne vont pas de pair selon le canal (affiliate vs search_paid)
- Un quart du CA est genere par des clients totalement invisibles au suivi

**Etape 5 - Insights**
- Insight 1 : affiliate ramene 2x plus de clients que search_paid mais avec 4 points de moins de Champions -> le canal le plus performant en volume n'est pas le plus qualitatif -> allouer le budget uniquement sur le volume/CPA risque de privilegier des clients moins fideles sur le long terme
- Insight 2 : 22,77% des transactions n'ont pas de customer_id -> une part significative du CA est generee par des clients qu'on ne peut jamais faire progresser vers le statut Champion, faute de suivi -> le potentiel de fidelisation sur ce quart du CA est structurellement invisible

**Etape 6 - Problematique**
"Comment orienter le budget d'acquisition vers des canaux qui apportent des clients a forte valeur, alors qu'un quart du chiffre d'affaires echappe totalement au suivi qui permettrait de le mesurer ?"

**Hypothese de recommandation**
Prioriser le budget marketing en ponderant volume et qualite de client acquis (CPA/ROAS + part de Champions), et mettre en place un systeme d'identification (compte client) au moment du paiement pour reduire la part de clients invites non trackes.

