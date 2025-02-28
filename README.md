📊 Projet de Trading sur Ethereum - Cryptocurrencies & BTC
📝 Description du projet
Ce projet a été réalisé dans le cadre du cours Cryptocurrencies & BTC, avec pour objectif la conception et l’optimisation d’une stratégie de trading algorithmique sur Ethereum (5 minutes), en utilisant des techniques d’analyse technique et de backtesting.

🔍 Stratégies développées
📅 Découpage des données :

Période d'entraînement (Train) : 2021 Jusqu'à décembre 2023
Période de test (Test) : janvier 2024 à février 2025
⚡ Stratégie 1 : Trading sur Moyennes Mobiles
1️⃣ Optimisation des Moyennes Mobiles (MM) via GridSearch sur la période d’entraînement.
2️⃣ Génération d’un signal d'achat (1) ou de vente (-1) :

Achat (Signal = 1) : On achète 1 ETH et on le conserve jusqu'à un signal de vente (-1).
Vente (Signal = -1) : On revend tout, sans frais intermédiaires.
Si Signal = -1, on ne prend aucune position et on attend un signal d'achat pour entrer à nouveau.
🎯 Objectif : Profiter de la hausse en évitant les frais liés aux transactions multiples.

📈 Stratégie 2 : Trading avec Indicateurs Techniques
🎯 Amélioration de la Stratégie 1 en ajoutant des filtres basés sur des indicateurs avancés :

RSI (Relative Strength Index) : Achat si RSI < 30, vente si RSI > 70
MACD (Moving Average Convergence Divergence) : Achat si MACD > MACD Signal, vente si MACD < MACD Signal
ATR (Average True Range) : Évaluation de la volatilité pour ajuster les seuils
ROC (Rate of Change) & Volatilité 20 jours pour affiner les décisions
💡 Avantages :
✅ Filtrage des faux signaux pour éviter d’acheter ou vendre dans de mauvaises conditions de marché.
✅ Prise en compte de la volatilité pour ajuster les entrées et sorties.

🔬 Comparaison avec un Benchmark (Buy & Hold)
Buy & Hold : Achat d’1 ETH en début de période et conservation jusqu'à la fin.
Stratégie 1 (MM uniquement) : Achat/Vente en fonction des moyennes mobiles optimales.
Stratégie 2 (MM + Indicateurs avancés) : Prise de décision basée sur un ensemble de critères techniques.
Objectif : Évaluer laquelle des stratégies est la plus performante sur la période test.
📂 Contenu du projet
🔹 1. import_data.ipynb 🛠️

📥 Récupère et prépare les données de l’ETH pour l’analyse.

🔹 2. optimisation_strategie.ipynb 🔍

🏆 Recherche des meilleures Moyennes Mobiles (MM Courte & Longue) via GridSearch. Sépare égalmenent le dataset en train et test qui seront utilisées plus tard

🔹 3. backtesting.ipynb 📈

🧪 Backtest des performances des stratégies :
✅ Stratégie 1 : Moyennes Mobiles Optimales
✅ Stratégie 2 : MM + RSI, MACD, ATR, Volatilité
✅ Benchmark Buy & Hold

🔹 4. the-bot-test.ipynb 🤖

🚀 Application des stratégies sur la période test (2024-2025) en temps réel. (Prise en compte du décalage via un shift, on regarde la mm de la période p-1 et on achète au prix p
⚠️ Bot fictif permettant théoriquement de passer des ordres automatiquement.

🔹 5. analyse_resultats_test.ipynb 📊

📊 Rapport d’analyse avec :
✅ Graphiques de performance
✅ Analyse avec QuantStats
✅ Comparaison des rendements des stratégies
nb : les frais sont payer à l'achat et à la revente (0.05% du close)
