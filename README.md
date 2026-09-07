# dia2_data_marketing

# Nettoyage et EDA – Segmentation Clients

## Objectif

Ce projet a pour objectif d'analyser et nettoyer les données clients issues d'un CRM afin de préparer une future segmentation marketing.

## Données

Deux fichiers CSV sont utilisés :

* `customers.csv` : informations et métriques sur les clients
* `transactions.csv` : historique des transactions

Les fichiers sont placés dans le dossier `data/`.

## Travail réalisé

Le notebook contient :

* un **Data Quality Report** ;
* l'identification et le traitement des anomalies ;
* le calcul du montant des transactions (`line_total`) ;
* une analyse exploratoire des achats ;
* l'analyse de la saisonnalité ;
* une analyse géographique ;
* l'analyse des catégories de produits ;
* l'étude des données zero-party ;
* la formulation de plusieurs hypothèses marketing.

## Structure

```text
projet-segmentation/
├── data/
│   ├── customers.csv
│   └── transactions.csv
├── notebooks/
│   └── nettoyage_eda.ipynb
└── README.md
```

## Outils

* Python
* Pandas
* NumPy
* Matplotlib
* Jupyter Notebook

## Résultat

Cette première analyse permet de comprendre la qualité des données et de préparer la segmentation RFM qui sera réalisée lors de l'étape suivante.

