# Projet 3 : BioSphere Analytics, dashboard de pilotage commercial et logistique

Dashboard Power BI de suivi d'une activité internationale de distribution de produits botaniques (E-commerce et Retail) : performance commerciale, supply chain et portefeuille clients (2023 à 2024).

> 📚 **Projet d'apprentissage** réalisé pour consolider mes compétences Power BI. Le jeu de données d'entraînement provient du cours LinkedIn Learning « L'essentiel de Power BI ». J'ai conçu le modèle de données, les mesures DAX, les pages du rapport et l'analyse présentés ici.

## 🎯 Contexte et objectifs
La direction souhaitait sortir des rapports statiques Excel pour disposer d'un pilotage centralisé et interactif. Le dashboard s'articule autour de trois piliers :
1. **Performance commerciale** : suivre le chiffre d'affaires, la saisonnalité et la contribution des familles de produits.
2. **Performance supply chain** : mesurer les volumes expédiés, le nombre de commandes et la répartition entre fournisseurs.
3. **Portefeuille clients** : suivre l'activité, le panier moyen et la répartition géographique du chiffre d'affaires.

## 📊 Chiffres clés
- 📦 1 536 unités vendues · 🧾 522 commandes · 🏭 20 fournisseurs
- 💶 75 095 € de chiffre d'affaires
- 👤 188 clients actifs sur 200 clients enregistrés
- 🛒 Panier moyen par client : 399 €

## Ce que j'ai réalisé
- **Power Query** : normalisation des types, nettoyage de la casse et des espaces, masquage des clés techniques dans la vue rapport.
- **Modèle en étoile** : 1 table de faits (ventes 2023-2024), 4 dimensions (Clients, Produits, Fournisseurs, Calendrier) et une table dédiée aux mesures.
- **Gestion des dates** : une table Calendrier avec deux relations vers la table de faits, l'une active (date de commande), l'autre inactive (date de livraison).
- **10 mesures DAX** : CA, Quantité vendue, Nombre de commandes, Clients actifs, Clients enregistrés, Moyenne mensuelle, Panier moyen par client, Panier min, Panier max et Écart de panier (avec SUMX, AVERAGEX, MAXX, MINX, DISTINCTCOUNT et KEEPFILTERS).
- **Rapport de 4 pages** : accueil de navigation, 3 pages d'analyse, filtres par pays et par année, interactions croisées paramétrées.

## Aperçu du dashboard

### Page 1 : Accueil
![Accueil](Images/page1-accueil.png)

### Page 2 : Performance commerciale
![Performance commerciale](Images/page2-performance-commerciale.png)

### Page 3 : Performance supply chain
![Performance supply chain](Images/page3-performance-supply-chain.png)

### Page 4 : Analyse du portefeuille clients
![Analyse du portefeuille clients](Images/page4-analyse-du-portefeuille-clients.png)

## 💡 Principaux constats
- **Concentration géographique** : la Chine génère 48 376 € sur 75 095 € de chiffre d'affaires, soit près des deux tiers.
- **Familles les plus rentables** : les Fabaceae (7 466 €) et les Asteraceae (6 660 €) arrivent en tête du chiffre d'affaires.
- **Fournisseurs répartis** : le premier fournisseur représente environ 10 % des unités (148 sur 1 536), sans dépendance marquée.
- **Clientèle active** : 188 clients actifs sur 200 inscrits, soit un faible nombre de comptes dormants.
- **Paniers très hétérogènes** : un écart de 1 317 € entre le plus petit et le plus gros panier, signe d'une coexistence de petites commandes (E-commerce) et de gros volumes (Retail).

## 🔭 Perspectives d'évolution
1. Intégrer les coûts d'achat et de transport pour analyser la marge brute par produit et par pays.
2. Ajouter des alertes visuelles (rouge/vert) sur les volumes fournisseurs.
3. Ajouter une prévision de la saisonnalité à partir de l'historique.

## 📘 Documentation complète
Le rapport détaillé (modèle, formules DAX, analyse page par page, choix de design et d'interactions) est disponible ici :
👉 [Rapport de projet (PDF)](BioSphereAnalyticsDoc.pdf)

## 📁 Fichiers
- [Rapport Power BI (.pbix)](RapportBioSphere.pbix)
- [Données de ventes (Excel)](04_01_ventes.xlsx)

## 🧰 Outils
Power BI Desktop · DAX · Power Query · Excel
