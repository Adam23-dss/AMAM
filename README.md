# Projet AMAM – Hack2Hire 2025
### (Agriculture & Météo Assistée par Machine Learning)

---

## 🧭Contexte du projet

L’agriculture africaine dépend encore fortement des conditions météorologiques. Les agriculteurs et les populations plus généralement font face à des difficultés tels que:
- des pluies imprévisibles et des sécheresses fréquentes qui affectent les champs et les rendements
  ## [![situation de l'hivernage 2024 à Touba](https://i0.wp.com/www.vivafrik.com/wp-content/uploads/2015/10/Khelcom.jpg)](https://youtu.be/QU1AtGt3b1E?si=mxYrtdiGl-DaCY68 "situation de l'hivernage 2024 à Touba")
> Clique sur l'image : Ce reportage de la chaine Al Mouridiyyah tv illustre la situation de l'hivernage 2024 à Diourbel (Touba)
- 🍂 des maladies liées au climat (paludisme, etc),
- 📉 un manque de données locales fiables.

Le projet AMAM – Hack2Hire vise à fournir une plateforme intelligente d’aide à la décision agricole, combinant prévisions météorologiques locales, modèles de Machine Learning pour prédire la météo, et notifications simples (SMS/WhatsApp)** pour les agriculteurs.

---

## Objectifs

1. Offrir des **prévisions météo locales précises** adaptées à chaque champ agricole.  
2. Mettre en place des **modèles de prédiction intelligents** :
   - prévision de pluie et sécheresse,
   - détection de maladies liées au climat,
   - estimation des besoins en irrigation.
3. Développer une **application simple et multilingue** accessible via web, mobile ou SMS.  
4. Contribuer à la **sécurité alimentaire** et à une **agriculture durable**.

---

## 🧩 Architecture du projet

### 1️⃣ **Data Engineering (ETL)**
- **Sources :**
  - [OpenWeather One Call 3.0](https://openweathermap.org/api)
  - FAO (FAOSTAT)
  - Copernicus (végétation, humidité du sol)
- **Pipeline :**
  - Extraction, nettoyage, standardisation (°C, mm, %).
  - Stockage dans PostgreSQL/TimescaleDB.
- **Outils :**
  - Python, Airflow, Pandas, PostgreSQL

---

### 2️⃣ **Data Science & MLOps**
- Modèles de prédiction météo/agro (ML) :
> - Prédire la pluie → éviter d’arroser pour rien. 
> - Anticiper sécheresse → planifier irrigation. 
> - Détecter risque de maladies (ex. chaleur + humidité = champignons). 
> - Estimer besoins en eau → recommandations personnalisées.
- Gestion et suivi via MLflow.
- API ML pour servir les prédictions en temps réel.

**Outils :**
> [scikit-learn](https://scikit-learn.org/stable/), XGBoost, Prophet, [MLflow](https://mlflow.org/), FastAPI, [Docker](https://www.docker.com/)

---

### 3️⃣ **Développement Applicatif**
- **Backend** : FastAPI  
- **Frontend** : React  
- **Alertes** : Twilio (SMS/WhatsApp)  
- **Visualisation** : Plotly, Charts.js

**Fonctionnalités principales :**
- Tableau de bord météo agricole
- Graphiques pluie/température
- Alertes personnalisées
- Recommandations d’irrigation

---

## ⚙️ Environnement technique

| Domaine | Technologies |
|----------|---------------|
| Backend | FastAPI, Uvicorn |
| Data | Python, Pandas, Airflow |
| ML | scikit-learn, Prophet, XGBoost |
| BDD | PostgreSQL, SQLAlchemy |
| Frontend | React.js |
| Alertes | Twilio API |
| Déploiement | Docker, GitHub Actions, MLflow |


