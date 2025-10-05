[[Security+]]
### 🍯 **Honeypot**

Un **honeypot** (ou "pot de miel") est un **système de sécurité informatique conçu pour attirer les attaquants** en simulant une cible vulnérable.

Il ne s’agit pas d’un système de production réel, mais d’un **leurre contrôlé** qui imite les failles d’un vrai serveur, d’un service ou d’un réseau, afin de :

- **Observer** les techniques utilisées par les attaquants,
    
- **Analyser** leur comportement,
    
- **Détourner** leur attention des véritables ressources critiques,
    
- **Collecter des informations** sur de nouvelles attaques (signatures, TTP, etc.).
    

Il peut être utilisé dans :

- Des environnements de recherche en cybersécurité,
    
- Des SOC (Security Operations Centers),
    
- Des systèmes de détection d’intrusion (IDS),
    
- Ou comme outil de renseignement (cyber threat intelligence).
    

---

#### 🔑 Types de honeypots :

- **Low-interaction** : simule des services basiques, faible risque, mais données limitées.
    
- **High-interaction** : imite un système complet (ex. un vrai serveur), plus risqué mais très informatif.
	
- **Client honeypot** :  Simule un **client vulnérable** (navigateur, app) qui se connecte à des serveurs pour détecter des malwares ou exploits.
### 🛰️ **Evil Twin (ou honeypot Wi-Fi)**

Un **Evil Twin** est un **faux point d'accès Wi-Fi** configuré pour **imiter un réseau légitime** (ex : même nom que le Wi-Fi d’un aéroport ou café). Il attire les utilisateurs qui s’y connectent **par erreur**, ce qui permet à l’attaquant de :

- Intercepter les données (attaque Man-in-the-Middle),
    
- Capturer des identifiants ou mots de passe,
    
- Injecter des malwares,
    
- Espionner le trafic.


### 🍪 **Honeytoken**

Un **honeytoken** est un **faux élément de donnée** (URL, fichier, clé API, identifiant, base de données...) inséré intentionnellement pour **détecter un accès non autorisé**.

#### 🔍 Exemples de honeytokens :

- Un **faux mot de passe** dans un fichier nommé `passwords.txt`,
    
- Une **fausse base de données** dans un SI,
    
- Une **clé API invalide** stockée dans un dépôt Git (détecte la compromission de secrets),
    
- Une **adresse e-mail unique** jamais utilisée ailleurs → alerte si elle reçoit un mail.
    

> 📌 **Avantage** : très léger, **aucun impact système**, idéal pour **détection rapide et ciblée**.
