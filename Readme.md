## 🔐 Private Project


# 🎓 Assistant Académique de Recherche - ENSIAS

## 📋 Synthèse du Projet

**Institution:** ENSIAS  
**Technologies principales:** NLP, RAG, IA Générative, LangChain, Hugging Face

---

## 🧠 Vue d’Ensemble

Ce projet vise à concevoir un **assistant intelligent de recherche académique** capable d’analyser, résumer et interagir avec des articles scientifiques.  
Il intègre un pipeline complet allant de **l’extraction automatique de contenu PDF** jusqu’à la **génération contextuelle de réponses** via des modèles de langage (LLM).

**Objectifs principaux :**
- Automatiser l’analyse de la littérature scientifique.
- Permettre des recherches sémantiques avancées sur des corpus de papiers.
- Faciliter la validation d’idées et la veille scientifique.
- Offrir une interface web fluide (Streamlit) et une API CLI performante.

---

## ⚙️ Architecture Globale
academic_research_assistant/
│
├── config/ # Configuration et logs
├── data/ # Données brutes, traitées et vectorisées
├── src/ # Code source principal
│ ├── document_processing/ # Extraction et nettoyage des PDFs
│ ├── nlp/ # Embeddings, recherche sémantique et Q&A
│ ├── rag/ # Pipeline RAG (retrieval + génération)
│ ├── llm/ # Gestion et chargement des modèles HF
│ ├── api/ # Intégration arXiv et APIs externes
│ └── utils/ # Fonctions utilitaires
│
├── interface/ # Application Streamlit
├── tests/ # Tests unitaires et d’intégration
├── examples/ # Exemples et tutoriels
│
├── main.py # CLI principale
├── requirements.txt # Dépendances Python
└── README.md # Documentation




---

## 🔍 Fonctionnalités Clés

### 🧾 Traitement Intelligent de Documents
- Extraction texte, formules, figures et références depuis des PDFs scientifiques.  
- Nettoyage et segmentation automatique (Abstract, Méthodes, Résultats…).

### 🔎 Recherche & RAG
- Indexation vectorielle avec FAISS.  
- Recherche sémantique à base d’embeddings (Sentence Transformers).  
- Re-ranking contextuel pour une pertinence accrue.

### 💬 Q&A Contextuel
- Génération de réponses précises avec LLM (Mistral, LLaMA, Flan-T5).  
- Historique conversationnel et traçabilité des sources.  
- Suggestions de questions pertinentes.

### 🧾 Intégration arXiv
- Recherche avancée par mot-clé ou auteur.  
- Téléchargement et indexation automatique d’articles.  
- Veille scientifique et suivi des publications récentes.

### 💻 Interface Streamlit
- Upload de documents et exploration interactive.  
- Chat académique contextuel.  
- Statistiques sur la base de données vectorielle.

---

## 📈 Performance & Scalabilité

| Opération | CPU | GPU | Description |
|------------|-----|-----|-------------|
| Extraction PDF (10p) | 5s | 5s | Extraction complète |
| Embeddings (100 docs) | 30s | 10s | Batch processing |
| Recherche vectorielle | 0.8s | 0.3s | Index FAISS optimisé |
| Génération LLM | 15s | 4s | Mistral-7B (512 tokens) |

Le système est capable de gérer jusqu’à **100k documents** avec des requêtes en moins de **5 secondes** grâce à une architecture FAISS optimisée.

---

## 🧰 Technologies Utilisées

| Domaine | Outils / Librairies |
|----------|--------------------|
| **LangChain** | Orchestration RAG |
| **Hugging Face** | LLMs & Transformers |
| **FAISS / ChromaDB** | Stockage vectoriel |
| **PyMuPDF / pdfplumber** | Extraction PDF |
| **Sentence Transformers** | Embeddings |
| **Streamlit** | Interface web |
| **arxiv API** | Recherche scientifique |

---

## 🧪 Tests et Qualité
- Tests unitaires sur toutes les composantes principales (Extraction, RAG, LLM).  
- Mesures de performance CPU/GPU.  
- Type hints et docstrings détaillées.  
- Couverture complète via `pytest --cov`.

---

## 🚀 Cas d’Usage

- **Revue de littérature** : indexer et interroger des corpus d’articles.  
- **Veille scientifique** : suivi automatisé d’auteurs ou de mots-clés.  
- **Rédaction de papiers** : validation d’hypothèses et recherche de références.  
- **Pédagogie** : réponses contextualisées aux questions d’étudiants.

---

## 🔐 Sécurité & Bonnes Pratiques
- Variables sensibles dans `.env` (jamais versionnées).  
- Connexions sécurisées HTTPS.  
- Logs protégés et anonymisation des requêtes.  
- Architecture modulaire pour déploiement cloud (Docker / systemd).

---

## 🛠️ Roadmap

| Horizon | Fonctionnalités prévues |
|----------|------------------------|
| **Court terme** | API REST (FastAPI), support Word/HTML |
| **Moyen terme** | Multi-langues, fine-tuning de modèles HF |
| **Long terme** | Agent autonome de recherche, génération de reviews automatiques |

---

## 🤝 Contribution
```bash
git clone <repo_url>
git checkout -b feature/ma-contribution
# Développement
git commit -m "Ajout fonctionnalité"
git push origin feature/ma-contribution
# Créer une Pull Request
```


💡 Conclusion

L’Assistant Académique de Recherche représente une plateforme complète et modulaire pour la recherche scientifique moderne.
Grâce à l’intégration des dernières avancées en NLP et IA générative, il simplifie l’accès, la compréhension et la production de connaissances.

Développé avec ❤️ à l’ENSIAS pour la communauté académique.
