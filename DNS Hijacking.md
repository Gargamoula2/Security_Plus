[[Security+]]
## 🧠 **DNS Hijacking (ou DNS Redirection)**

### 🔎 **Définition**

Le **DNS Hijacking** est une attaque où l’attaquant modifie la résolution DNS pour rediriger les utilisateurs vers un site frauduleux **alors qu’ils ont saisi une URL légitime**.

Plutôt que d’atteindre le vrai serveur (par ex. `www.banque.com`), l’utilisateur est envoyé vers **un faux site contrôlé par l’attaquant**.

---

### ⚙️ **Fonctionnement**

L’attaque cible le **processus de résolution DNS**, qui traduit un nom de domaine en adresse IP. Si ce processus est compromis, les utilisateurs peuvent être trompés **sans qu’ils s’en rendent compte**.

---

### 🎭 **Objectifs typiques**

- Vol de **mots de passe**, **informations bancaires**, ou **identifiants**.
    
- Installation de **malwares**.
    
- Redirection vers des sites publicitaires (dans des attaques moins graves).
    
- Surveillance ou censure (par des États ou réseaux compromis).
    

---

### 🧨 **Types courants de DNS Hijacking**

|Type|Description|
|---|---|
|**Local DNS hijacking**|L’attaquant modifie les paramètres DNS **sur l’ordinateur de la victime**.|
|**Router DNS hijacking**|Le **routeur** de la victime est compromis, modifiant les DNS pour tout le réseau.|
|**ISP-level DNS hijacking**|Le **fournisseur d’accès** redirige volontairement certaines requêtes (ex : erreurs 404 vers pub).|
|**Man-in-the-Middle DNS spoofing**|L’attaquant intercepte les requêtes DNS sur le réseau et envoie de fausses réponses.|

---

### 🛡️ **Contre-mesures**

- 🔒 **Utiliser DNSSEC** (DNS Security Extensions) : permet de vérifier l’authenticité des réponses DNS.
    
- 🔧 **Configurer un DNS fiable** : ex. Cloudflare (1.1.1.1), Google DNS (8.8.8.8).
    
- 📶 **Sécuriser le routeur** : changer les identifiants par défaut, mettre à jour le firmware.
    
- 🧑‍💻 **Utiliser un VPN** : chiffre les requêtes DNS.
    
- 🧪 **Scanner le système** pour vérifier si le DNS a été modifié (via paramètres réseau ou fichiers système).
    
- 🕵️‍♀️ **Surveiller les certificats SSL** : si un site légitime affiche un **certificat invalide**, alerte immédiate.