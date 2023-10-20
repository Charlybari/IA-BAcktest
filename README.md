# IA-BAcktest

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
Script d'Indicateurs Techniques pour le Trading
Ce script est conçu pour calculer divers indicateurs techniques utilisés dans le trading. Ces indicateurs peuvent aider les traders à prendre des décisions éclairées en analysant les mouvements passés des prix.

Fonctionnalités :
Calcul de l'indice de choppiness.
Conversion de l'indice de choppiness en pourcentage.
Calcul de divers autres indicateurs techniques tels que le Supertrend, l'EMA, le RSI, le MACD, les Bollinger Bands, et bien d'autres.
Utilisation de la bibliothèque talib pour certains calculs.
Dépendances :
pandas
talib
numpy
Comment utiliser :
Assurez-vous d'avoir installé toutes les dépendances.
Intégrez ces fonctions dans votre script de trading ou utilisez-les séparément pour analyser les données historiques.
Passez un DataFrame contenant les données de prix (OHLC) à ces fonctions pour obtenir les valeurs des indicateurs.
Fonctions :
get_chop(): Calcule l'indice de choppiness.
chopiness_to_percentage(): Convertit l'indice de choppiness en pourcentage.
signal_4(): Génère un signal basé sur la différence de choppiness.
get_supertrend(): Calcule le Supertrend.
get_ema(): Calcule la Moyenne Mobile Exponentielle (EMA).
get_rsi(): Calcule l'indice de force relative (RSI).
get_macd(): Calcule le MACD (Moving Average Convergence Divergence).
get_bollinger_bands(): Calcule les Bollinger Bands.
get_stochastic_oscillator(): Calcule le Stochastic Oscillator.
get_sar_direction(): Détermine la direction du Parabolic SAR.
get_cmf(): Calcule le Money Flow Chaikin (CMF).
get_fibonacci_retracement(): Calcule les niveaux de retracement de Fibonacci.
get_atr_percent_diff(): Calcule la différence en pourcentage de l'ATR.
get_ema_diff(): Calcule la différence entre deux EMA.
ICPA(): Calcule un indicateur personnalisé basé sur la puissance et d'autres indicateurs.
bougie(): Détermine si une bougie est positive ou négative.
awesome_oscillator(): Calcule l'Awesome Oscillator.
bull_bear_power(): Calcule la puissance Bull et Bear.
simple_ultimate_oscillator(): Calcule l'Ultimate Oscillator.
compute_cci(): Calcule l'indice de canal des matières premières (CCI).

Régression prévisionnelle
La régression prévisionnelle est une technique utilisée pour prédire les valeurs futures d'une série de données en utilisant une régression polynomiale. Cette technique est particulièrement utile pour les séries de données financières, où la prédiction des prix futurs est cruciale pour les décisions d'investissement.

Comment ça marche ?
La régression prévisionnelle utilise une régression polynomiale pour ajuster un modèle à un ensemble de données historiques. Une fois que le modèle est ajusté, il peut être utilisé pour extrapoler ou prédire les valeurs futures.

Voici un exemple de code Python qui montre comment utiliser la régression prévisionnelle pour prédire les prix futurs d'une série de données financières :

python
Copy code
# Paramètres pour la régression
kwargs = {
    "column_name": "close",
    "degree": 3,
    "length": 10,
    "extrapolate":11
}

# Fonction pour appliquer la régression polynomiale sur un DataFrame
def polynomial_regression_on_dataframe(df, **kwargs):
    ...
    return df
La fonction polynomial_regression_on_dataframe prend en entrée un DataFrame contenant les données historiques et renvoie un DataFrame avec des colonnes supplémentaires contenant les coefficients de la régression, les prévisions, la direction de la tendance, et d'autres informations pertinentes.

Autres fonctions utiles
En plus de la fonction principale, il existe d'autres fonctions utiles qui peuvent être utilisées pour analyser les résultats de la régression et générer des signaux de trading. Par exemple, la fonction extrapolation_direction détermine la direction de la tendance en comparant la moyenne des valeurs extrapolées à la dernière valeur réelle avant l'extrapolation.

Il existe également des fonctions pour calculer les performances des prévisions, convertir les indicateurs en scores, et générer des signaux de trading en fonction des scores.

Conclusion
La régression prévisionnelle est une technique puissante pour prédire les valeurs futures d'une série de données. Avec le bon ensemble de fonctions et d'outils, il est possible de générer des prévisions précises et de prendre des décisions d'investissement éclairées.

Indicateurs Techniques et Analyse
Ce script fournit une série d'indicateurs techniques couramment utilisés dans l'analyse technique des marchés financiers. Voici une liste des indicateurs inclus et une brève description de chacun :

Moyenne Mobile Exponentielle (EMA)
La Moyenne Mobile Exponentielle (EMA) donne plus de poids aux prix récents et est donc plus réactive que la moyenne mobile simple. Les EMA sont calculées pour différentes fenêtres de temps :

EMA1 : Fenêtre de 1 période
EMA2 : Fenêtre de 2 périodes
... et ainsi de suite jusqu'à EMA6.
Super Trend
Le Super Trend est un indicateur de tendance basé sur le calcul de l'ATR (Average True Range). Il fournit des signaux d'achat et de vente en fonction de la direction de la tendance.

Stochastic RSI
Le Stochastic RSI est un oscillateur qui mesure le niveau du RSI par rapport à sa plage haute/basse sur un nombre spécifique de périodes. Il est utilisé pour identifier les conditions de surachat ou de survente.

Choppiness Index
Le Choppiness Index est un indicateur conçu pour déterminer si le marché est choppy (consolidation) ou en train de trader (directionnel).

Autres Indicateurs
Le script comprend également une variété d'autres indicateurs tels que :

Williams %R
MACD
ADX
Parabolic SAR
... et bien d'autres.
Calculs Supplémentaires
En plus des indicateurs, le script effectue également une série de calculs supplémentaires pour fournir des informations supplémentaires, telles que les divergences, les scores basés sur différents indicateurs, et une recommandation finale basée sur le score moyen de tous les indicateurs.

Utilisation :
Pour utiliser ces indicateurs, assurez-vous d'avoir un DataFrame contenant les colonnes 'open', 'high', 'low', 'close' et 'volume'. Passez ce DataFrame aux fonctions appropriées pour obtenir les valeurs des indicateurs.

Stratégies d'Investissement Basées sur des Indicateurs Techniques
Ce script génère des stratégies d'investissement basées sur une variété d'indicateurs techniques. Ces stratégies sont conçues pour aider les traders à prendre des décisions d'achat et de vente en fonction des signaux fournis par les indicateurs.

Famille d'Indicateurs
Le script catégorise les indicateurs en différentes familles :

Indicateurs de Sentiment : Ces indicateurs, tels que IndicateurBougie et Recommendation, fournissent des signaux basés sur l'analyse des chandeliers.
Indicateurs Binaires : Ces indicateurs, comme SUPER_TREND_DIRECTION, fournissent des signaux binaires (1 ou -1) indiquant la direction du marché.
Indicateurs Triples : Ces indicateurs, tels que bollinger_signal, peuvent avoir trois valeurs possibles (1, 0, -1).
Indicateurs de Moyenne Mobile : Cette famille comprend des indicateurs tels que EMA, SMA et d'autres variantes de moyennes mobiles.
Indicateurs de Pourcentage de Changement : Ces indicateurs mesurent le changement en pourcentage d'une valeur par rapport à sa valeur précédente.
Indicateurs Classiques : Cette catégorie comprend des indicateurs bien connus tels que CHOP, WillRPositive, et RSI.
Indicateurs Zéro : Ces indicateurs oscillent autour de zéro et peuvent être utilisés pour identifier les points de retournement du marché.
Indicateurs Précédents : Ces indicateurs comparent la valeur actuelle d'un indicateur à sa valeur précédente.
Génération de Stratégies
Le script fournit une fonction generate_strategy qui génère des stratégies d'investissement basées sur les indicateurs fournis. Les stratégies générées comprennent des scénarios pour ouvrir et fermer des positions longues et courtes.

Utilisation
Pour générer des stratégies, utilisez la fonction generate_strategy en fournissant le dictionnaire d'indicateurs et le nombre d'indicateurs à sélectionner pour chaque famille.

Sélection Dynamique des Indicateurs pour la Génération de Stratégies
Cette section du script se concentre sur la détermination du nombre d'indicateurs à utiliser pour chaque famille d'indicateurs. Au lieu de fixer un nombre prédéfini d'indicateurs pour chaque famille, le script sélectionne un nombre aléatoire d'indicateurs, offrant ainsi une variété de combinaisons possibles pour la génération de stratégies.

Fonction determine_num_indicators
La fonction determine_num_indicators sélectionne de manière aléatoire le nombre d'indicateurs à utiliser pour chaque famille. Elle renvoie un dictionnaire où les clés sont les noms des familles d'indicateurs et les valeurs sont le nombre d'indicateurs sélectionnés pour chaque famille.

Affichage des Informations
Après avoir déterminé le nombre d'indicateurs à utiliser, le script affiche les informations suivantes :

Symbol : Le symbole de l'actif pour lequel les stratégies sont générées.
Interval : L'intervalle de temps utilisé pour l'analyse technique.
Start Date : La date de début de l'analyse.
Leverage : L'effet de levier utilisé pour le trading.
Wallet : La taille du portefeuille ou du capital initial.
Ensuite, le script génère et affiche les stratégies d'investissement en utilisant la fonction generate_strategy.

Note :
La sélection dynamique des indicateurs permet d'explorer une variété de scénarios et de stratégies, ce qui peut être utile pour tester différentes combinaisons d'indicateurs et optimiser les performances de trading.

Analyse de Backtest
Cette section du script se concentre sur l'exécution d'un backtest basé sur les stratégies générées précédemment. Elle parcourt l'ensemble des données de prix et simule des trades basés sur les conditions définies pour ouvrir et fermer des positions longues et courtes.

Fonctions de Conditions
openLongCondition: Détermine si une position longue doit être ouverte.
closeLongCondition: Détermine si une position longue doit être fermée.
openShortCondition: Détermine si une position courte doit être ouverte.
closeShortCondition: Détermine si une position courte doit être fermée.
Simulation de Backtest
Le script itère sur l'ensemble des données de prix et vérifie à chaque étape si une condition de trading est remplie. Si c'est le cas, un trade est simulé, et les détails du trade sont enregistrés dans un DataFrame dt.

Analyse des Résultats
Après avoir simulé tous les trades, le script analyse les résultats pour fournir des statistiques telles que :

Le nombre total de trades.
Le nombre de trades gagnants et perdants.
Le meilleur et le pire trade.
Le rendement total du portefeuille.
Et d'autres statistiques pertinentes.
Affichage des Résultats
Les résultats du backtest sont affichés à la fin, fournissant un aperçu des performances de la stratégie sur les données historiques.

Note :
L'analyse de backtest est essentielle pour évaluer la viabilité d'une stratégie de trading avant de l'appliquer en temps réel. Il est important de noter que les performances passées ne garantissent pas les performances futures.

Résultats et Statistiques du Backtest
Cette section du script affiche les résultats et les statistiques détaillées du backtest. Elle fournit des informations sur la performance globale de la stratégie, ainsi que des détails sur les trades individuels.

Informations Générales
Pair Symbol : Symbole de la paire de trading.
Period : Période de temps sur laquelle le backtest a été effectué.
Starting balance : Solde initial avant le début du backtest.
Statistiques Générales
Performance globale par rapport au dollar américain.
Performance de la stratégie "Buy and Hold".
Meilleur et pire trade.
Drawback le plus défavorable.
Total des frais de trading.
Informations sur les Trades
Nombre total de trades effectués.
Nombre de trades positifs et négatifs.
Taux de réussite des trades.
Performance moyenne des trades.
Informations sur les Trades LONG
Statistiques détaillées sur les trades LONG, y compris le nombre total, la performance moyenne, le meilleur et le pire trade, et le taux de réussite.
Informations sur les Trades SHORT
Statistiques détaillées sur les trades SHORT, y compris le nombre total, la performance moyenne, le meilleur et le pire trade, et le taux de réussite.
Raisons des Trades
Liste des raisons pour lesquelles les trades ont été effectués et leur fréquence.
Note :
Les statistiques fournies sont essentielles pour évaluer la performance de la stratégie de trading. Il est recommandé de les examiner attentivement avant de prendre des décisions de trading en temps réel.

Visualisation des Résultats du Backtest
Cette section du script génère un graphique pour visualiser les résultats du backtest. Elle permet de comparer visuellement l'évolution du portefeuille avec les variations de prix.

Graphique
Le graphique est divisé en deux sous-graphiques :

Wallet : Montre l'évolution du solde du portefeuille au fil du temps.
Price : Affiche les variations du prix de l'actif tradé pendant la période du backtest.
Utilisation
Pour visualiser les résultats, exécutez simplement cette section du script. Assurez-vous que vous avez déjà exécuté les parties précédentes du script pour générer les données nécessaires.

Affichage
Après avoir exécuté cette section, un graphique sera affiché avec deux sous-graphiques. Cela vous aidera à comprendre comment le solde du portefeuille a évolué par rapport aux variations de prix.

Note :
La visualisation est un outil puissant pour comprendre les performances de votre stratégie. Il est recommandé de l'utiliser régulièrement pour évaluer et ajuster votre stratégie de trading.



er


