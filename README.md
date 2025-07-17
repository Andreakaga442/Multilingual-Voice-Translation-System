SYSTEME DE TRADUCTION VOCALE MULTILANGUES

Ce projet est une application de traduction vocale multilingue en temps réel, développé dans un cadre collaboratif par une équipe, répartis en 5 groupes fonctionnels.

Objectif : 
Permettre à un utilisateur de parler dans sa langue, faire transcrire automatisation sa voix en texte, conduire ce texte dans une autre langue, puis diffuser la traduction vocalement et visuellement à d'autres utilisateurs connectés.

Architecture Modulaire (5 groupes fonctionnels)
Groupe Fonction Technologies
1 Capture de la voix et conversion en texte Python + Whisper
2 Interface utilisateur et envoi du texte à travail Web (HTML/JS) ou client Python
3 Flacon multiligne automatique de traduction (API), HuggingFace, mBART50
4 Diffusion du texte et audio traduit WebRTC, PyTTX / Espeack
5 Backend centralisé pour coordonner les modifications Flask REST API, JSON, HTTP

Fonctionnalités principales
Transcription vocale : la voix de l'utilisateur est convertie en texte via Whisper.

Traduction automatique : le texte est traduit dans la langue choisie avec mBART50.

Restitution audio : le texte traduit est reconverti en voix (TTS) et diffusé aux utilisateurs.

Communication inter-groupe : tout passe par un backend central en JSON via HTTP POST/GET.

Optimisation des performances : détection automatique de la langue source + système de cache LRU pour éviter les traductions redondantes.

Technologies utilisées

-Python 3.10+
-Flacon
-Transformateurs HuggingFace (mBART50)
-Murmure (parole-texte)
-PyTTX / Espeack
-Détection de langage

Outils de cachet

WebRTC (pour la diffusion en temps réel)

HTML/CSS/JavaScript 
