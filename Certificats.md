[[Security+]]
#### **1. Définition**

Un **certificat numérique** est une pièce d'identité électronique qui lie une clé publique à une entité (personne, machine, domaine). Il est utilisé pour authentifier et chiffrer les communications.

---

#### **2. Composants Clés**

|**Terme**|**Description**|**Exemple/Usage**|
|---|---|---|
|**Certificate Authority (CA)**|Entité de confiance qui émet et valide les certificats.|DigiCert, Let's Encrypt, Microsoft CA.|
|**CRL (Certificate Revocation List)**|Liste noire des certificats révoqués avant expiration.|Un certificat compromis est ajouté à la CRL.|
|**OCSP (Online Certificate Status Protocol)**|Alternative aux CRL pour vérifier en temps réel la validité d'un certificat.|Vérification instantanée via une requête OCSP.|
|**Self-Signed Certificate**|Certificat signé par son propre créateur (non émis par une CA tierce).|Utilisé en interne pour les tests.|
|**Third-Party Certificate**|Certificat émis par une CA externe reconnue (confiance publique).|Certificat SSL/TLS pour un site web public.|
|**Root of Trust**|CA racine ultime qui signe les autres CA intermédiaires.|Symantec Root CA, GlobalSign Root CA.|
|**CSR (Certificate Signing Request)**|Fichier contenant les infos pour générer un certificat (clé publique + métadonnées).|Généré via OpenSSL ou l'interface d'un serveur web.|
|**Wildcard Certificate**|Certificat valable pour tous les sous-domaines d'un domaine principal.|`*.exemple.com` couvre `blog.exemple.com`, `api.exemple.com`.|

---

#### **3. Processus de Validation**

1. **Génération d'une CSR** (via OpenSSL ou un serveur web).
    
2. **Soumission à une CA** (interne ou tierce).
    
3. **Vérification de l'identité** (par la CA).
    
4. **Émission du certificat** signé.
    
5. **Installation** sur le serveur/client.
    

---

#### **4. Révocation des Certificats**

- **CRL** : Liste périodiquement mise à jour (peut être lente).
    
- **OCSP** : Réponse instantanée (mais dépend de la disponibilité du serveur OCSP).
    

---

#### **5. Bonnes Pratiques**

- **Éviter les self-signed** en production (manque de confiance publique).
    
- **Renouveler avant expiration** pour éviter les interruptions.
    
- **Utiliser des wildcards avec précaution** (si un sous-domaine est compromis, tous le sont).