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

**Sources et periode (faits 1 a 5)**
- Faits 1, 2, 5 : source = transactions.csv (+ customers.csv pour le fait 1). Periode = 07/01/2022 au 30/06/2026 (~4,5 ans)
- Faits 3, 4 : source = touchpoints.csv (+ RFM calcule sur transactions.csv/customers.csv). Periode = 16/06/2025 au 29/06/2026 (~1 an)
- Limite a mentionner : les deux sources ne couvrent pas la meme fenetre temporelle (4,5 ans vs 1 an). Les faits 3 et 4 ne portent que sur la derniere annee de donnees, contrairement aux faits 1, 2 et 5.

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

---

## TP Storytelling - Partie 2 (les 5 slides)

**Slide 1 - Problematique business**
(rien d'autre a l'ecrit, contexte + tension dits a l'oral)
"Comment orienter le budget d'acquisition vers des canaux qui apportent des clients a forte valeur, alors qu'un quart du chiffre d'affaires echappe totalement au suivi qui permettrait de le mesurer ?"

**Slide 2 - Insights cles**
- Affiliate ramene 2x plus de clients que search_paid, mais avec 4 points de Champions en moins -> le canal le plus performant en volume n'est pas le plus qualitatif
- 22,77% des transactions n'ont pas de customer_id -> une part significative du CA est generee par des clients qu'on ne peut jamais faire progresser vers le statut Champion, faute de suivi

**Slide 3 - Preuve data (2 graphes)**
1. Barres : part de Champions par canal (affiliate 15,4% vs search_paid 19,5%)
2. Repartition transactions avec / sans customer_id (22,77% invisibles)

**Slide 4 - Recommandation**
- Action : ponderer le budget d'acquisition entre canaux selon la part de Champions generes, pas seulement le CPA/volume
- Cible : budget marketing acquisition (arbitrage affiliate <-> search_paid en priorite)
- KPI : part de clients Champions generes par canal, suivie par trimestre

**Slide 5 - Impact**
- Impact estime : en reorientant une partie du budget vers les canaux a plus forte part de Champions, on augmente la proportion de clients a haute valeur acquis (les Champions, 6% de la base, generent a eux seuls 43% du CA)
- Decision demandee : valider un test de reallocation (~10-15% du budget) d'affiliate vers search_paid sur le prochain trimestre, et mesurer l'impact sur la part de Champions generes


---

## Conclusion (reponse directe a la question du CMO)

Question du CMO (Jour 3, sujet fil rouge) : *"On a lance plusieurs campagnes, on a depense un budget consequent, mais on ne sait pas ce qui fonctionne vraiment. Le social nous dit que tout marche tres bien. Google nous dit la meme chose. Mais je m'attendais a plus de ventes."*

**Reponse :** oui, une partie du budget est mal placee, et ce n'est pas visible si on ne regarde que le volume de conversions par canal (ce que font le social et Google en interne, ce qui explique qu'ils se donnent tous les deux raison).

- **Ce qu'on observe (What) :** affiliate ramene 2x plus de clients que search_paid, mais avec 4 points de Champions en moins (15,4% vs 19,5%). Et 22,77% des transactions n'ont pas de customer_id, donc 22,77% du CA est genere par des clients qu'on ne peut jamais suivre ni faire progresser.
- **Pourquoi ca compte (So What) :** juger un canal seulement sur son nombre de conversions (comme le fait chaque plateforme en interne) revient a ignorer la qualite des clients acquis. Un canal peut sembler tres performant en volume tout en ramenant des clients qui ne reviendront jamais. Et un quart du CA echappe totalement a toute optimisation faute de tracking.
- **Ce qu'on recommande (Now What) :** reponderer le budget d'acquisition entre canaux selon la part de Champions generes (pas seulement le CPA/volume brut), en testant un transfert de 10 a 15% du budget d'affiliate vers search_paid ce trimestre ; et inciter a la creation de compte au moment du paiement pour reduire la part de CA invisible au suivi.

En une phrase : ce n'est pas qu'aucune campagne ne marche, c'est qu'on les compare avec le mauvais critere -- corriger ca permet de reorienter le budget sans en depenser plus.
