# Spotify-AI-agent
📌 Description

AI Spotify Mood Playlist Agent est un agent d’intelligence artificielle permettant de générer automatiquement des playlists Spotify personnalisées à partir des émotions exprimées par un utilisateur via Telegram.

L’agent utilise un modèle de langage Mistral pour analyser l’émotion (nostalgie, tristesse, joie, etc.) contenue dans la requête utilisateur, puis interroge l’API Spotify afin de créer une playlist adaptée aux préférences et à l’humeur détectée.

🚀 Fonctionnalités

💬 Interaction en temps réel via Telegram

🧠 Analyse des émotions grâce au modèle Mistral

🎵 Génération automatique de playlists personnalisées

🔗 Intégration de l’API Spotify

🎯 Recommandations basées sur :

L’émotion détectée

Les préférences musicales utilisateur

⚡ Création et retour automatique du lien Spotify

🏗️ Architecture

L’utilisateur envoie un message via Telegram.

Le message est transmis au modèle Mistral pour analyse sémantique.

L’émotion dominante est identifiée.

L’API Spotify est interrogée en fonction des critères émotionnels.

Une playlist est générée dynamiquement.

Le lien Spotify est renvoyé à l’utilisateur.

🛠️ Technologies utilisées

Python

Telegram Bot API

Spotify Web API

Mistral (LLM) pour l’analyse NLP

API REST

🎯 Exemple

Utilisateur :

"Je suis un peu triste ce soir, j’aimerais quelque chose de doux."

Processus :

Analyse via Mistral → émotion détectée : tristesse

Requête Spotify adaptée (tempo, énergie, valence)

Création playlist

Envoi du lien à l’utilisateur

🔐 Configuration

Variables d’environnement nécessaires :

SPOTIFY_CLIENT_ID=your_client_id
SPOTIFY_CLIENT_SECRET=your_client_secret
TELEGRAM_BOT_TOKEN=your_bot_token
MISTRAL_API_KEY=your_mistral_api_key


Lancement :

python main.py

📈 Améliorations futures

Classification émotionnelle multi-label

Personnalisation avancée via historique d’écoute

Système de feedback utilisateur

Déploiement cloud

Fine-tuning du modèle émotionnel
