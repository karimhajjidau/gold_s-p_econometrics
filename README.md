# README - Analyse Économétrique des Interactions entre l'Or et le S&P 500

## 📌 Introduction
Ce projet vise à analyser les relations dynamiques entre le prix de l'or (Gold Prices en USD) et l'indice S&P 500 (en USD) sur la période 2000-2019. L'objectif est d'évaluer si l'or peut être considéré comme un actif refuge en période de crise et d'examiner la relation entre ces deux actifs financiers.

## 📊 Données et Méthodologie
- **Source des données** : DBnomics (240 observations mensuelles de janvier 2000 à décembre 2019).
- **Méthodes utilisées** :
  - **Analyse univariée** : Stationnarisation des séries (tests ADF et KPSS), modélisation ARMA.
  - **Analyse multivariée** : Modèle VAR pour identifier les interactions entre les deux séries.
  - **Tests de causalité de Granger** pour déterminer si une variable influence l'autre.
  - **Analyse des réponses impulsionnelles** pour mesurer l'impact des chocs économiques.

## 🔍 Résultats Principaux
- L'or et le S&P 500 sont des processus non stationnaires, nécessitant une différenciation.
- Le modèle ARMA(1,1) est retenu pour le S&P 500 en log-différencié.
- Le modèle VAR(1) montre que :
  - Les variations du S&P 500 influencent significativement le prix de l’or.
  - En revanche, les variations du prix de l’or n’ont pas d’impact significatif sur le S&P 500.
- Les tests de causalité de Granger confirment que **le S&P 500 cause l'or, mais l’inverse n’est pas vrai**.
- Les fonctions impulsion-réponse indiquent que les chocs sur le S&P 500 se répercutent sur l’or à court terme.

## 📈 Implications pour les Investisseurs
- **L'or joue bien un rôle de refuge en période de crise**, mais son impact sur les actions est limité.
- **Les variations du marché actions précèdent celles de l'or**, ce qui peut être utile pour l’allocation d’actifs.
- **Les prévisions de l'indice S&P 500 à court terme** sont possibles via un modèle ARMA(1,1), mais restent sensibles aux événements exogènes (ex. crise COVID-19).

## 🛠️ Reproduction des Résultats
- **Langage utilisé** : R
- **Packages principaux** : `forecast`, `tseries`, `vars`, `urca`
- **Exécution du script** : Charger les séries, stationnariser, estimer le modèle VAR, tester la causalité, puis générer les prévisions.

