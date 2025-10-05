
## **1. Les 3 Composants de AAA**

|**Composant**|**Fonction**|**Exemple**|
|---|---|---|
|**Authentication**|Vérifie l’identité d’un utilisateur/système ("Qui êtes-vous ?").|Login/mot de passe, certificat numérique, biométrie.|
|**Authorization**|Détermine ce que l’utilisateur/système a le droit de faire ("Que pouvez-vous faire ?").|Accès à un dossier partagé, permission d’exécuter une commande admin.|
|**Accounting**|Loggue et audite les actions de l’utilisateur/système ("Qu’avez-vous fait ?").|Journalisation des connexions VPN, durée de session, commandes exécutées.|

---

## **2. Protocoles AAA à connaître**

### **a) RADIUS (Remote Authentication Dial-In User Service)**

- **Utilisation** : Accès réseau (Wi-Fi, VPN, 802.1X).
    
- **Caractéristiques** :
    
    - Utilise **UDP** (ports 1812/1813).
        
    - Chiffrement **partiel** (seul le mot de passe est chiffré).
        
    - Combine _Authentication_ et _Authorization_ (moins granulaire que TACACS+).
        

### **b) TACACS+ (Terminal Access Controller Access-Control System)**

- **Utilisation** : Administration réseau (équipements Cisco).
    
- **Caractéristiques** :
    
    - Utilise **TCP** (port 49).
        
    - Chiffrement **complet** de la session.
        
    - Sépare clairement **AuthN, AuthZ et Accounting**.
        
    - Permet un contrôle **granulaire** (ex : autoriser `show run` mais pas `configure terminal`).

---

## **3. Cas d’Usage AAA dans la Security+**

### **Scénario 1 : Accès Wi-Fi d’entreprise**

- **Authentification** : L’utilisateur saisit son login/mot de passe → vérifié par **RADIUS**.
    
- **Autorisation** : RADIUS vérifie s’il a accès au VLAN "Employés".
    
- **Comptabilité** : Le SIEM loggue la connexion (heure, durée, adresse IP).
    

### **Scénario 2 : Administration d’un routeur Cisco**

- **Authentification** : L’admin se connecte via SSH → vérifié par **TACACS+**.
    
- **Autorisation** : TACACS+ autorise seulement les commandes `show` (pas de modification).
    
- **Comptabilité** : Toutes les commandes tapées sont enregistrées pour audit.
    

---

## **4. Bonnes Pratiques et Sécurité**

- **Pour RADIUS** :
    
    - Utiliser **EAP-TLS** (certificats) plutôt que MSCHAPv2 (moins sécurisé).
        
    - Éviter les mots de passe par défaut sur les serveurs RADIUS.
        
- **Pour TACACS+** :
    
    - Restreindre l’accès aux adresses IP des admins.
        
    - Chiffrer les logs d’accounting.