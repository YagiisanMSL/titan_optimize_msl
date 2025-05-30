# titan_optimize_msl

🐉 Calculateur de Debuffs Titan - Monster Super League
Afficher l'image
Afficher l'image
Afficher l'image
Un calculateur de probabilités avancé pour optimiser vos compositions d'équipe dans les raids Titan de Monster Super League.
🎯 Fonctionnalités
⚡ Mécaniques de jeu précises

Distribution des boules bleues : 2 boules par équipe par tour (4 total)
Système de talents : Passifs et actifs avec probabilités configurables
Résistance des Titans : 15% (Feu/Eau/Bois/Dark) ou 30% (Light)
Réinitialisation des debuffs : Durée max quand un nouveau debuff passe
Exclusivité boule bleue : Le talent passif est bloqué si une boule bleue est reçue

🛡️ Types de debuffs supportés

ATK Down - Réduction d'attaque
DEF Down - Réduction de défense
Affaiblissement - Debuff général
Faiblesse Exposée - Vulnérabilité accrue

🧮 Calculs avancés

Simulation Monte Carlo avec 10 000 itérations pour une précision maximale
Probabilités cumulées sur plusieurs tours
Prise en compte des durées (1-3 tours pour debuffs)
Validation croisée entre calcul théorique et simulation

🚀 Utilisation
Configuration

Sélectionnez le type de Titan (résistance automatique)
Configurez vos 8 monstres (2 équipes de 4)
Définissez les talents passifs : Type, probabilité, durée
Définissez les talents actifs : Type, probabilité, durée
Choisissez le tour à analyser (1-20)

Calcul

Bouton "Calculer les Probabilités" : Calcul rapide par simulation
Bouton "Simulation Monte Carlo" : Validation avec algorithme indépendant

Résultats
Affichage des probabilités qu'un debuff soit actif au tour sélectionné, en tenant compte :

Des tentatives des tours précédents encore actives
De la résistance du Titan
Des mécaniques de boules bleues
De la réinitialisation des durées

🔧 Technologies utilisées

HTML5 - Structure sémantique
CSS3 - Design moderne avec glassmorphism et animations
JavaScript Vanilla - Logique de calcul et simulation
Algorithmes statistiques - Monte Carlo, probabilités conditionnelles

📊 Algorithme de calcul
1. Distribution des boules bleues
P(monstre reçoit boule bleue) = 7/16 = 43.75%
- 2 boules sur 4 monstres par équipe
- Distribution aléatoire uniforme
2. Application des talents
Si boule bleue reçue:
  - Seul le talent actif peut proc
  - P(debuff) = P_talent × (1 - résistance_titan)
  
Si pas de boule bleue:
  - Seul le talent passif peut proc  
  - P(debuff) = P_talent × (1 - résistance_titan)
3. Gestion des durées
Si nouveau debuff appliqué:
  - tours_restants = durée_max_du_talent
  
À chaque tour:
  - tours_restants = max(0, tours_restants - 1)
📈 Cas d'usage
Optimisation d'équipe

Comparaison de compositions : Tester différentes combinaisons
Analyse de fiabilité : Probabilité d'avoir un debuff crucial
Planification stratégique : Optimiser selon le tour ciblé

Exemples pratiques

Garantir 90%+ de DEF Down au tour 3
Maximiser l'uptime d'ATK Down sur 5 tours
Équilibrer entre plusieurs types de debuffs

🎨 Interface
Design inspiré de MSL

Couleurs vibrantes : Dégradés cyan-bleu-vert
Animations fluides : Effets de survol et transitions
Glassmorphism : Transparence et flous modernes
Responsive : Adaptatif mobile/tablette/desktop

Disposition

4 monstres par ligne sur desktop
Interface compacte : Champs optimisés pour la lisibilité
Feedback visuel : Probabilités affichées en temps réel

🧪 Validation
Le calculateur a été testé avec :

Cas extrêmes : 0% et 100% de probabilités
Cohérence : Vérification calcul vs simulation
Précision : Margin d'erreur < 0.5% avec 10k itérations

📋 Installation
Déploiement local
bash# Cloner le repository
git clone https://github.com/[username]/msl-titan-calculator

# Ouvrir le fichier
open index.html
Déploiement web

GitHub Pages : Activez dans Settings > Pages
Netlify : Drag & drop du fichier HTML
Vercel : Import direct depuis GitHub

🤝 Contribution
Les contributions sont les bienvenues ! Pour contribuer :

Fork le projet
Créez votre branche feature (git checkout -b feature/amelioration)
Committez vos changements (git commit -m 'Ajout fonctionnalité')
Push vers la branche (git push origin feature/amelioration)
Ouvrez une Pull Request

Types de contributions recherchées

🐛 Corrections de bugs
✨ Nouvelles fonctionnalités (buffs d'équipe, nouveaux debuffs)
📚 Amélioration documentation
🎨 Améliorations UI/UX
⚡ Optimisations performance
