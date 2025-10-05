[[Security+]]
#### **1. Définition du Zero Trust**  
- **Principe** : "Ne jamais faire confiance, toujours vérifier" (*Never Trust, Always Verify*).  
- **Approche** : Aucun utilisateur, appareil ou réseau n'est considéré comme fiable par défaut, même s'il est à l'intérieur du périmètre réseau.  
- **Objectif** : Limiter les risques de compromission en supprimant la confiance implicite.  

---

#### **2. Principes Clés du Zero Trust**  
- **Vérification explicite** : Authentification et autorisation continues pour chaque accès.  
- **Moindre privilège** : Accès limité uniquement aux ressources nécessaires.  
- **Micro-segmentation** : Division du réseau en petites zones pour limiter les déplacements latéraux.  
- **Analyse continue** : Surveillance en temps réel des comportements et des risques.  

---

#### **3. Composants du Zero Trust**  
- **IAM (Identity and Access Management)** :  
  - Authentification multifacteur (MFA).  
  - Gestion des identités (SSO, RBAC, ABAC).  
- **PAM (Privileged Access Management)** : Contrôle des comptes à privilèges.  
- **SASE (Secure Access Service Edge)** : Combinaison de SD-WAN et de services de sécurité cloud.  
- **EDR/XDR** : Détection et réponse aux menaces sur les endpoints (EDR) ou étendue à plusieurs sources (XDR).  
- **Analyse comportementale** : Détection d'anomalies via l'IA/ML.  

---

#### **4. Mise en Œuvre du Zero Trust**  
- **Étape 1** : Inventaire des utilisateurs, appareils et données critiques.  
- **Étape 2** : Segmentation du réseau (micro-segmentation).  
- **Étape 3** : Mise en place de politiques d'accès strictes (moindre privilège).  
- **Étape 4** : Surveillance et analyse continue (logs, SIEM).  

---

#### **5. Avantages du Zero Trust**  
- Réduction de la surface d'attaque.  
- Meilleure conformité (RGPD, NIS2, etc.).  
- Adaptabilité aux environnements hybrides (cloud, télétravail).  

---

#### **6. Exemples de Technologies Zero Trust**  
- **Zscaler** : Plateforme SASE.  
- **Okta** : Gestion des identités.  
- **Cisco Duo** : MFA et contrôle d'accès.  
- **Microsoft Azure AD** : Accès conditionnel.  
