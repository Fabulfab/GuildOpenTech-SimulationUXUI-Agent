# Agent IA - Simulation Key Users

## 🚀 Fonctionnalités

Cet agent IA permet de simuler différents profils d'utilisateurs (personas) pour analyser des interfaces utilisateur. Il utilise l'API Mistral pour générer des réponses contextuelles selon le profil sélectionné.

### Personas disponibles :
- **P1_Spécialiste_UI** : Analyse basée sur Dribbble, Behance, Awwwards, Mobbin
- **P2_Spécialiste_UX** : Analyse selon le Baymard Institute et références UX
- **P3_Développeur_junior_homme** : Point de vue junior (<2 ans XP)
- **P4_Développeur_reconversion_expertise** : Profil mixte reconversion
- **P5_Développeur_senior_homme** : Expert senior (>10 ans XP)
- **P6_Développeur_confirmé_femme** : Confirmé (3-7 ans XP)
- **P7_Développeur_junior_femme_reconversion** : Junior reconversion
- **P8_Développeur_junior_homme_BTS** : Junior BTS

## 📋 Prérequis

1. **Clé API Mistral** : Obtenez votre clé sur [https://console.mistral.ai/](https://console.mistral.ai/)
2. **Node.js** : Version 18+ recommandée
3. **npm** ou **yarn**

## 🛠️ Installation et démarrage

### 1. Installer les dépendances
```bash
npm install
```

### 2. Démarrer le serveur de développement
```bash
npm run dev
```

### 3. Accéder à l'agent IA
Ouvrez votre navigateur et allez sur : `http://localhost:3000/ai-agent`

## 🎯 Utilisation

### Étape 1 : Configuration
1. Sélectionnez un persona dans le menu déroulant
2. Entrez votre clé API Mistral
3. (Optionnel) Importez une image UI à analyser

### Étape 2 : Créer des questions
1. Cliquez sur "Ajouter une question"
2. Saisissez votre question dans le champ
3. Répétez pour ajouter plusieurs questions

### Étape 3 : Générer des réponses
1. **Réponses manuelles** : Saisissez directement vos réponses
2. **Réponses IA** : Cliquez sur "Générer via IA" pour obtenir des réponses automatiques

### Étape 4 : Sauvegarder et exporter
1. Cliquez sur "Enregistrer mes réponses" pour sauvegarder localement
2. Cliquez sur "Exporter" pour télécharger un fichier Excel

## 🔧 Configuration avancée

### Variables d'environnement (optionnel)
Créez un fichier `.env.local` à la racine du projet :
```env
MISTRAL_API_KEY='Entrer la clé API'
```

### Personnalisation des personas
Modifiez le fichier `utils/ai-config.ts` pour ajouter ou modifier des personas.

## 📁 Structure du projet

```
├── app/
│   ├── ai-agent/
│   │   └── page.tsx          # Page Next.js de l'agent IA
│   ├── api/
│   │   └── mistral/
│   │       └── route.ts      # API route sécurisée
│   └── page.tsx              # Page d'accueil
├── public/
│   └── ai-agent.html         # Interface HTML/CSS/JS
├── utils/
│   └── ai-config.ts          # Configuration et personas
└── AI_AGENT_README.md        # Ce fichier
```

## 🔒 Sécurité

- La clé API est transmise côté client mais traitée côté serveur
- Les appels API passent par une route Next.js sécurisée
- Aucune clé API n'est stockée en dur dans le code

## 🐛 Dépannage

### Erreur "Clé API requise"
- Vérifiez que vous avez saisi votre clé API Mistral
- Assurez-vous que la clé est valide

### Erreur "Erreur API Mistral"
- Vérifiez votre connexion internet
- Vérifiez que votre clé API a des crédits disponibles
- Consultez la console du navigateur pour plus de détails

### L'agent ne répond pas
- Vérifiez que le serveur Next.js est démarré
- Vérifiez que vous accédez à la bonne URL
- Videz le cache du navigateur

## 📊 Export des données

Les données sont exportées au format Excel avec les colonnes :
- **Date** : Date et heure de la session
- **User** : Persona sélectionné
- **Question** : Question posée
- **Réponse** : Réponse générée (manuelle ou IA)

## 🤝 Contribution

Pour améliorer l'agent IA :
1. Modifiez les personas dans `utils/ai-config.ts`
2. Améliorez l'interface dans `public/ai-agent.html`
3. Ajoutez de nouvelles fonctionnalités dans les composants Next.js

## 📝 Licence

Ce projet est sous licence MIT. Voir le fichier LICENSE pour plus de détails. 