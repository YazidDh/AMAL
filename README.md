# Rapport d'Architecture LLM — Multi-serveurs / Multi-clients

## Auteur
**Yazid Dhouioui et Mazen Haouari**  
Date : 6 octobre 2025

## Description
Ce rapport présente une **architecture client-serveur optimisée pour le déploiement de modèles de langage de grande taille (LLM)**.  
Il couvre deux types d'architectures :

### 1. Architecture parallèle (multi-serveurs / multi-clients)
**Composants principaux :**
- Clients multiples
- API Gateway
- Load Balancer
- Serveurs d’inférence (GPU/CPU)
- Module d’Embeddings
- Retriever
- Vector DB
- Cache (Redis)
- Orchestrateur (Docker, Kubernetes, etc.)
- Monitoring (Prometheus/Grafana)
- Storage persistant

**Objectifs :** scalabilité horizontale, faible latence, haute disponibilité, tolérance aux pannes, parallélisme massif.

### 2. Architecture locale (on-premise / single-host)
**Composants :**
- Clients locaux
- API Gateway
- Load Balancer
- Pool d’inférence (GPU local)
- Module d’Embeddings
- Retriever (ANN)
- Vector DB locale
- Cache Redis
- Storage local (SSD)
- Orchestrateur léger (docker-compose / systemd)
- Monitoring
- Modules d’Intelligence :
  - Collecte de données et feedback
  - Fine-tuning / apprentissage local
  - Gestionnaire de modèles

**Objectifs :** contrôle des données, latence faible pour les clients locaux, apprentissage local et adaptation du modèle.
