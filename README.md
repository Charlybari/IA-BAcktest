# IA-BAcktest

Bien sûr, voici une version française du README pour votre script GitHub :

Script de Backtest pour Binance
Ce script est conçu pour effectuer des backtests de stratégies de trading sur des données historiques de prix de la plateforme d'échange Binance. Il récupère les données historiques des chandeliers (klines) pour une paire de trading et un intervalle donnés, puis applique un ensemble de règles de trading pour simuler la performance d'une stratégie sur cette période.

Fonctionnalités :
Récupération des données historiques des chandeliers de Binance pour une paire de trading et un intervalle spécifiés.
Sélection aléatoire d'une paire de trading, d'un intervalle, d'un effet de levier et d'un montant de portefeuille pour le backtest.
Utilisation de bibliothèques Python populaires telles que pandas, pandas_ta, talib et ta pour la manipulation des données et l'analyse technique.
Dépendances :
pandas
pandas_ta
requests
datetime
random
talib
numpy
ta
Comment utiliser :
Assurez-vous d'avoir installé toutes les dépendances.
Exécutez le script.
Le script sélectionnera aléatoirement une paire de trading, un intervalle, un effet de levier et un montant de portefeuille.
Il récupérera ensuite les données historiques pour les paramètres sélectionnés et affichera les résultats.
Variables :
makerFee et takerFee : Définissent les frais pour les ordres de type maker et taker.
initialWallet et lastAth : Initialisent le montant du portefeuille. Cette valeur sera modifiée ultérieurement en fonction du montant de portefeuille choisi aléatoirement.
stopLoss et takeProfit : Définissent les valeurs de stop loss et de prise de profit.
orderInProgress, longIniPrice, shortIniPrice, longLiquidationPrice, shortLiquidationPrice : Variables utilisées pour suivre l'état des trades.
Fonctions :
get_historical_klines() : Récupère les données historiques des chandeliers de Binance.
get_all_trading_pairs() : Récupère toutes les paires de trading disponibles sur Binance ayant USDT comme l'une des paires.
choose_parameters() : Sélectionne aléatoirement une paire de trading, un intervalle, un effet de levier et un montant de portefeuille pour le backtest.
Sorties :
Le script affichera les détails suivants :

Symbole de la paire de trading
Intervalle
Date de début du backtest
Effet de levier utilisé
Montant du portefeuille
Confirmation que le choix a été chargé
