# Spotify-AI-agent

## 📌 Description

AI Spotify Mood Playlist Agent est un agent d’intelligence artificielle permettant de générer automatiquement des playlists Spotify personnalisées à partir des émotions exprimées par un utilisateur via Telegram.

L’agent utilise le modèle Mistral pour analyser l’émotion détectée dans le message (nostalgie, tristesse, joie, etc.), puis interroge l’API Spotify afin de créer une playlist adaptée à l’humeur et aux préférences de l’utilisateur.

---

## 🚀 Fonctionnalités

- Interaction en temps réel via Telegram
- Analyse des émotions avec Mistral (LLM)
- Génération automatique de playlists Spotify
- Intégration de l’API Spotify
- Recommandation basée sur l’humeur et les préférences utilisateur
- Retour automatique du lien de la playlist

---

## 🏗️ Architecture

1. L’utilisateur envoie un message via Telegram.
2. Le message est analysé par Mistral pour détecter l’émotion dominante.
3. L’API Spotify est interrogée avec des critères adaptés à l’émotion.
4. Une playlist personnalisée est générée.
5. Le lien Spotify est renvoyé à l’utilisateur.

---

## 🛠️ Technologies utilisées

- Python
- Telegram Bot API
- Spotify Web API
- Mistral (LLM) 

---

## 🎯 Exemple d’utilisation

Utilisateur :
"Je me sens nostalgique aujourd’hui."

Processus :
- Analyse émotionnelle → Nostalgie
- Génération d’une playlist adaptée
- Envoi du lien Spotify

---

## 🔐 Configuration

Créer un fichier `.env` ou configurer les variables d’environnement :

SPOTIFY_CLIENT_ID=your_client_id  
SPOTIFY_CLIENT_SECRET=your_client_secret  
TELEGRAM_BOT_TOKEN=your_bot_token  
MISTRAL_API_KEY=your_mistral_api_key  

Lancer le projet :

```bash
python main.py
