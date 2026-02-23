# Département Mathématiques

## MASTER Mathématiques et Ingénierie Numérique

# Business Intelligence (BI)

## Mini-projet Power BI

**Réalisé par :** Ridwan ES-SBAI\
**Sous la supervision de :** Pr. Aicha Oussous\
**Année Universitaire :** 2025--2026

------------------------------------------------------------------------

# Introduction

## Objectif : Mission AdventureWorks 2019

L'objectif central de cette mission est de transformer le système
d'information de l'entreprise AdventureWorks en un outil de pilotage
stratégique interactif à l'aide de Power BI.

### Axes prioritaires

-   **Centralisation et modélisation** : Conception d'un schéma en
    étoile.
-   **Performance commerciale** : Développement des KPI.
-   **Intelligence géographique** : Analyse mondiale des ventes.
-   **Analyse temporelle** : Étude sur la période 2011--2014.

------------------------------------------------------------------------

# Description des Données : L'Écosystème AdventureWorks

## Départements

1.  Sales (Ventes)\
2.  HumanResources (Employés)\
3.  Production (Produits)\
4.  Person (Localisation)

## Tables de faits

-   **SalesOrderHeader**
-   **SalesOrderDetail**

## Tables de dimensions

-   **HumanResources.Employee**
-   **Production.Product**
-   **Person.Address**
-   **Person.StateProvince**

------------------------------------------------------------------------

# Modélisation

## Schéma en étoile

Relations de type **1 : ∞** avec filtrage des dimensions vers la table
de faits.

------------------------------------------------------------------------

# Mesures DAX

``` dax
CA_Total = SUMX(SalesOrderDetail, SalesOrderDetail[LineTotal])
```

``` dax
Rang_Vendeur = RANKX(ALL(HumanResources.Employee), [CA_Total])
```

------------------------------------------------------------------------

# Analyse

-   Amérique du Nord : marché principal\
-   CA total \> 100 millions \$\
-   Top vendeurs : 275, 276, 277

------------------------------------------------------------------------

# Conclusion

Ce projet démontre l'efficacité de la Business Intelligence avec Power
BI pour transformer des données brutes en vision stratégique
exploitable.
