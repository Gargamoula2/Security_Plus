[[Security+]]
## 🔽 **SSL/TLS Downgrade Attack**

### 🔎 **Définition**

Une **attaque de rétrogradation SSL/TLS** (aussi appelée **Protocol Downgrade Attack**) consiste à **forcer une connexion chiffrée à utiliser une version plus ancienne, moins sécurisée** du protocole SSL/TLS.

L’objectif est de rendre la communication plus facile à attaquer, en exploitant des vulnérabilités connues des anciennes versions (ex. SSL 3.0 ou TLS 1.0).

---

### 🎯 **But de l’attaquant**

- **Briser le chiffrement** en exploitant une version vulnérable.
    
- **Intercepter** ou **altérer** des données dans une session censée être sécurisée.
    
- Mener une attaque **Man-in-the-Middle (MITM)**.
    

---

### ⚙️ **Fonctionnement**

1. Le client (ex. navigateur) dit au serveur qu’il **supporte plusieurs versions** de TLS/SSL.
    
2. L’attaquant (placé entre les deux) **intercepte** la négociation.
    
3. Il **modifie les messages Client Hello** pour que le serveur **croit que seule une ancienne version est disponible**.
    
4. Le serveur accepte la rétrogradation — et la connexion sécurisée est établie… **mais affaiblie**.
    

---

### 🧪 **Exemples connus**

|Nom de l’attaque|Description courte|
|---|---|
|**POODLE (2014)**|Exploite SSL 3.0 forcé via downgrade de TLS|
|**FREAK (2015)**|Forçait l’utilisation de clés RSA faibles|
|**DROWN (2016)**|Exploite les serveurs supportant SSLv2 pour casser TLS|

---

### 🛡️ **Contre-mesures**

| Mesure                                                | Explication                                                               |
| ----------------------------------------------------- | ------------------------------------------------------------------------- |
| 🔐 **Désactiver SSL et TLS 1.0/1.1**                  | Ne laisser actifs que **TLS 1.2 ou 1.3** sur les serveurs et navigateurs. |
| 📦 **Utiliser HSTS (HTTP Strict Transport Security)** | Forcer les connexions chiffrées à TLS, **sans possibilité de downgrade**. |
| 🧱 **Déployer des pare-feux/IDS intelligents**        | Capables de **détecter des négociations anormales**.                      |
| 🧰 **Suivre les meilleures pratiques SSL/TLS**        | Mise à jour des bibliothèques (OpenSSL, etc.), configurations fortes.     |
| 🖥️ **Vérification côté client**                      | Certains clients modernes refusent les versions faibles automatiquement.  |