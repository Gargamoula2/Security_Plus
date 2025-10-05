[[Security+]]
### **ECDHE (Elliptic Curve Diffie-Hellman Ephemeral)**

**Protocole d'échange de clés sécurisé utilisé dans TLS/SSL pour établir une clé de session chiffrée.**

---

#### **1. Fonctionnement**

ECDHE combine deux concepts :

- **ECDH (Elliptic Curve Diffie-Hellman)** : Version du protocole **Diffie-Hellman** utilisant les **courbes elliptiques** pour un échange de clés plus efficace.
    
- **Ephemeral (Éphémère)** : Génération de clés temporaires **uniques par session**, contrairement à DH statique (moins sécurisé).
    

**Étapes clés :**

1. Le client et le serveur se mettent d’accord sur une **courbe elliptique** (ex : secp256r1).
    
2. Chacun génère une **paire de clés éphémères** (publique/privée).
    
3. Ils échangent leurs clés publiques et calculent une **clé secrète commune** (sans jamais la transmettre).
    
4. Cette clé est utilisée pour dériver la **clé de session TLS** (ex : pour AES-256).
    

---

#### **2. Avantages**

✅ **Forward Secrecy (PFS)** : Même si la clé privée du serveur est compromise, les sessions passées restent protégées (car les clés éphémères sont jetées).  
✅ **Efficacité** : Les courbes elliptiques offrent une sécurité équivalente à RSA/DH avec des **clés plus courtes** (ex : 256 bits vs. 3072 bits).  
✅ **Rapidité** : Moins gourmand en CPU que RSA ou DH classique.

#### **3. Comparaison avec d’autres protocoles**

|Protocole|Forward Secrecy ?|Basé sur|Taille clé équivalente|
|---|---|---|---|
|**ECDHE**|✅ Oui|Courbes elliptiques|256 bits = 3072 bits RSA|
|**DHE** (classique)|✅ Oui|Logarithmes discrets|2048 bits = 2048 bits RSA|
|**RSA** (statique)|❌ Non|Factorisation|3072 bits recommandés|

---

#### **4. Attaques et Bonnes Pratiques**

- **Choix des courbes** :
    
    - Préférer **secp256r1** (NIST), **x25519** (Curve25519, plus moderne).
        
    - Éviter les courbes faibles (ex : secp112r1).
        
- **Protection contre les attaques** :
    
    - **Logjam** (affaiblissement de DH) → Désactiver les groupes DH < 2048 bits.
        
    - **Side-channel attacks** → Implémentations matérielles sécurisées (ex : Intel SGX).



**Résumé** : ECDHE est aujourd’hui la norme pour les échanges de clés sécurisés, offrant un bon équilibre entre sécurité (PFS), performance et compatibilité. Son adoption est essentielle pour les applications sensibles (banque, santé, messagerie).