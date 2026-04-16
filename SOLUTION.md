# **Hawta.com**  
**Hackathon 2026**  
**Date** : 16 avril 2026  

**Objectif** : Application mobile qui aide les Tangérois à faire leurs courses au prix le plus bas en combinant **IA + communauté + données locales** (supermarchés + souks + livraison).

## 1. Concept (Pitch 30 secondes)

**Hawta.com - Tanger** transforme les courses en jeu collectif intelligent :  

Tu listes tes produits, l’IA te dit **exactement** où acheter aujourd’hui à Tanger (Marjane, Aswak, Carrefour, Sabrine, Laquinta, souks…) pour payer le moins cher.  

Les utilisateurs partagent des promos en anonyme → l’IA vérifie et valide → tout le monde gagne.  

**Résultat** : **15-25 % d’économies** sur le budget courses.

---

## 2. Fonctionnalités détaillées

### Fonctionnalité principale : Optimiseur de courses IA
- Saisie libre ou dictée en temps réel (support complet Darija, français et arabe classique)
- Reconnaissance vocale naturelle pour dicter sa liste (“jbed 2l halib, 1kg maticha, 3 boites thon, 5kg riz”)
- Comparaison intelligente et actualisée en temps réel des prix chez :
  - Grandes surfaces : Marjane Tanger City Mall, Aswak Assalam Malabata, Carrefour Market, Sabrine
  - Service de livraison : Laquinta (livraison gratuite au-dessus de 150 DH)
  - Souks locaux : Marché Msala, Grand Souk / Grand Socco, Marché Central
- L’IA propose **exactement 3 meilleures options** classées selon :
  - Prix total le plus bas
  - Temps de déplacement estimé
  - Note « éco » (prise en compte distance, impact carbone et fraîcheur des produits)
- Suggestions automatiques de recettes low-cost basées sur les produits choisis
- Adaptation selon le profil : Famille de 5, Célibataire, Étudiant, etc.
- Prise en compte du jour de la semaine, de l’heure actuelle et du quartier de l’utilisateur

### Fonctionnalité 2 : Carte des deals en temps réel (Killer Feature)
- Carte interactive full-screen de Tanger (utilisant Leaflet ou Google Maps en dark mode)
- Filtres par quartier et par catégorie (chips horizontaux : Tous | Souks | Supermarchés | Livraison | Promos du jour)
- Épingles dynamiques et colorées :
  - Rouge = Promo très chaude (moins d’1 heure)
  - Vert = Meilleur prix du moment
  - Jaune = Souk du jour (meilleures affaires fraîches)
- Partage anonyme ultra-rapide : l’utilisateur prend une photo d’un ticket de caisse ou d’un stand au souk → l’IA analyse, vérifie la cohérence des prix et publie le deal en moins de 2 minutes
- Mode offline complet : tous les deals récents et prix sont mis en cache pour fonctionner sans connexion

### Fonctionnalité 3 : Alertes inflation intelligentes
- Notifications push personnalisées selon le quartier de l’utilisateur, son historique d’achats et ses produits préférés
- Détection automatique des hausses de prix significatives
- Exemple de notification : « Prix du lait +12 % cette semaine à Tanger → achète maintenant chez Laquinta avant que ça augmente encore »
- Possibilité de configurer des alertes personnalisées : produits suivis, seuils de variation de prix, quartiers prioritaires

### Fonctionnalité 4 : Gamification & communauté Tanger
- Système de points motivant :
  - +10 points par deal partagé et validé par l’IA
  - +25 points si le deal est utilisé par 10 personnes ou plus
  - +50 points si le deal est le plus utilisé de la semaine
  - +100 points pour le “Deal du mois”
- Leaderboard compétitif : Top Chasseurs de Tanger (classement global + classements par quartier)
- Badges locaux et valorisants : « Roi du Souk Msala », « Maître de Malabata », « Éco-chasseur Ibn Battouta », « Livraison Master Laquinta »
- Tout reste individuel : pas de partage de données personnelles entre utilisateurs

### Fonctionnalités bonus
- Scanner de ticket intelligent : photo d’un ticket de caisse → l’IA extrait automatiquement les produits et les prix (avec possibilité de correction manuelle)
- Historique détaillé des économies réalisées (graphiques mensuels et hebdomadaires)
- Interface en mode sombre complet avec gros boutons pour une utilisation facile
- Support multilingue complet : Darija en priorité, Français et Arabe

### Authentification
- Système simple et minimal : Email + mot de passe
- Bouton « Continuer en mode invité » pour tester l’application sans inscription
- Utilisation exclusive de Firebase Auth (aucun partage de compte ni de données sensibles)
---

## **Charte Graphique Globale**

**Mode principal** : **Dark Mode** (fond très sombre / noir)  
**Couleurs principales** :
- **Accent principal (highlight)** : Jaune vif / doré (#FFD700 ou similaire au jaune de l’image) → pour les cartes "Meilleur prix", deals chauds, badges
- **Accent secondaire** : Bleu (#3B82F6 ou bleu électrique comme dans l’image) → pour alertes, sections secondaires
- **Texte principal** : Blanc / gris clair sur fond sombre
- **Vert Hawta (économie)** : `#00B86E` (gardé pour les économies et notes éco)
- **Orange promo** : `#FF6B00`
- **Rouge alertes** : `#E63939`

**Polices** :
- Titres : Poppins Bold ou Cairo Bold (texte très bold et moderne)
- Texte : Noto Sans Arabic + Poppins (clean et lisible)

**Style général** :  
Modern Dark UI + cartes avec coins arrondis + glassmorphism léger + ombres subtiles + icônes stylisées marocaines (souk, tagine, carte Tanger).  
Mettre en avant les éléments importants avec des cartes jaunes comme dans l’image (ex. : meilleure option en jaune).

---

## **Écrans de l’Application**

### **Écran 0 : Login / Register (Onboarding)**
**Détails visuels :**
- Fond : Photo aérienne floutée de Tanger (baie + Médina + mer) avec overlay sombre 40%
- Logo Hawta.com centré en haut (texte blanc + petit tagine stylisé vert)
- Carte Tanger miniature en arrière-plan très transparente
- Formulaire centré dans une carte blanche avec coins arrondis (glassmorphism)
- Champs : Email + Mot de passe + “Confirmer mot de passe” (register)
- Boutons :
  - “Se connecter” → vert Hawta plein
  - “Créer un compte” → contour vert
  - “Continuer en mode invité” → texte gris + icône fantôme
- Lien “Mot de passe oublié ?”
- Footer : “Made with ❤️ for Tanger”

### **Écran 1 : Accueil / Dashboard**
**Layout (Mobile)** :
- Header : Photo de profil circulaire (coin gauche) + “Salut Fatima 👋” + “Malabata, Tanger” (avec petite icône localisation)
- Jauge circulaire “Budget avril” : 1240 DH / 2500 DH (vert → orange selon remplissage)
- Section “Deals chauds aujourd’hui” → 3 cartes horizontales scrollables :
  - Tomates 1kg → 6 DH (souk Msala) → badge “-38%”
  - Lait Laquinta → 17 DH (livraison gratuite)
  - Poulet entier → 42 DH (Aswak)
- Carte interactive miniature (Tanger) avec 4 épingles
- Gros bouton flottant central : **+ Nouvelle liste de courses** (vert + icône panier)
- Carte “J’ai économisé cette semaine” : **187 DH** (+12% vs semaine dernière) avec petite courbe
- Bottom Navigation (5 icônes) :
  - Accueil (maison)
  - Liste (panier)
  - Carte (map)
  - Communauté (users)
  - Profil (avatar)

### **Écran 2 : Nouvelle Liste de courses**
- Barre de saisie en haut avec micro + “Parle en darija ou français…”
- Exemple de chips suggérés : “Lait”, “Tomates”, “Thon”, “Huile”, “Riz”, “Poulet”, “Œufs”
- Liste des produits ajoutés (avec quantité modifiable + bouton supprimer)
- Bouton “Optimiser avec l’IA” → très gros, vert, en bas
- Après optimisation : **3 cartes résultats** (très détaillées) :

**Carte Option 1 (Meilleure)** :
- Badge “Meilleur prix global” (vert)
- Prix total : **214 DH** (économie -47 DH)
- Itinéraire : Souk Msala → Laquinta (livraison)
- Temps estimé : 35 min
- Note éco : ★★★★☆
- Bouton “Choisir cet itinéraire”

Suggestions recettes en bas : “Salade tunisienne low-cost” + “Chakchouka express”

### **Écran 3 : Carte des deals (Killer Feature)**
- Full screen map (Leaflet/Google)
- Filtres en haut (chips horizontaux) :
  - Tous | Souks | Supermarchés | Livraison | Promos du jour
- Épingles personnalisées :
  - Rouge = Promo très chaude (< 1h)
  - Vert = Meilleur prix
  - Jaune = Souk du jour
- Bottom sheet quand on clique sur une épingle (détails + photo + prix + “Aller”)
- Bouton flottant rouge en bas à droite : **“Partager un deal”** (icône appareil photo)

### **Écran 4 : Communauté / Mes Deals**
- Onglets : Mes Deals | Leaderboard | Tous les deals
- Liste des deals validés avec photo du ticket ou du stand
- Chaque carte : Produit + Prix + Magasin + Points gagnés + Temps depuis publication
- Leaderboard :
  - Top 10 avec avatars, noms, quartier, points
  - Toi en évidence avec ton rang (#12 – Malabata)
- Badges en grille : Roi du Souk Msala, Maître Laquinta, Chasseur Ibn Battouta, etc.

### **Écran 5 : Alertes & Notifications**
- Liste chronologique avec icônes :
  - ↑ Lait +12% cette semaine (rouge)
  - Tomates à 6 DH au souk Msala (vert)
  - Laquinta offre livraison gratuite aujourd’hui
- Bouton “Gérer mes alertes” → choix de produits + quartiers + seuil de variation

### **Écran 6 : Profil**
- Header avec photo de couverture (vue Tanger) + photo de profil
- Niveau + barre d’XP (niveau 7 – Chasseur Confirmé)
- Statistiques en 3 cartes :
  - 1 248 DH économisés
  - 47 deals partagés
  - 12 450 pts
- Grille de badges (débloqués + verrouillés)
- Historique des économies (graphique mensuel)
- Paramètres en liste

### **Écran 7 : Résultats d’optimisation (détaillé)**
- Comparaison en tableau ou 3 colonnes verticales
- Colonnes : Option A | Option B | Option C (recommandée)
- Lignes :
  - Prix total
  - Magasins & ordre
  - Temps total
  - Coût livraison
  - Note éco
  - Économie vs moyenne
- Bouton “Simuler économies” (animation avant/après)

### **Écran 8 : Scanner Ticket / Photo Promo**
- Caméra plein écran avec overlay de cadrage
- Bouton “Photo” + “Importer depuis galerie”
- Animation de scan IA (barre qui monte)
- Après analyse : écran de confirmation avec produits extraits + prix détectés (possibilité de corriger)

---

## **Fonctionnalités supplémentaires détaillées**

### Optimiseur IA avancé
- Compréhension Darija naturelle (“jbed 2l halib, 1kg maticha, 3 boites thon”)
- Prend en compte : jour de la semaine, heure actuelle, quartier de l’utilisateur, promos communautaires validées
- Mode “Famille de 5” / “Célibataire” / “Étudiant”

### Gamification
- Points : +10 (partage validé), +25 (deal utilisé par 10+ personnes), +100 (deal du mois)
- Niveaux : Débutant → Chasseur → Maître Souk → Légende de Tanger

### Mode Offline
- Toutes les listes sauvegardées localement
- Derniers prix connus + date de mise à jour
- Carte avec deals mis en cache
