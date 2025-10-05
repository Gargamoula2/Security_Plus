[[Security+]]
#### **1. Définition du Control Plane**

- **Rôle** : Cerveau du modèle [[Zero Trust]] qui orchestre les décisions d’accès en temps réel.
    
- **Fonction** : Centralise la gestion des politiques, des identités et des menaces pour appliquer une sécurité dynamique.
    

---

#### **2. Composants Clés du Control Plane**

|**Composant**|**Description**|**Exemple**|
|---|---|---|
|**Adaptive Identity**|Identité dynamique ajustée en fonction du comportement et du contexte (localisation, appareil, heure).|Un utilisateur accédant depuis un nouvel appareil déclenche une vérification MFA supplémentaire.|
|**Threat Scope Reduction**|Minimisation de la surface d’attaque en limitant l’accès aux seules ressources nécessaires.|Un employé du marketing n’a pas accès aux bases de données financières.|
|**Policy-Driven Access Control**|Accès basé sur des politiques strictes (RBAC/ABAC) évaluées en temps réel.|Politique bloquant l’accès aux données sensibles en dehors des heures de bureau.|
|**Policy Administrator**|Système qui applique les décisions du Policy Engine (ex : octroi/refus d’accès).|Azure AD appliquant une restriction géographique.|
|**Policy Engine**|Prend des décisions d’accès en analysant les risques (données utilisateur, contexte, menaces).|Une analyse comportementale bloque un compte en cas d’activité anormale.|

---

#### **3. Interaction entre les Composants**

1. **Policy Engine** évalue la demande d’accès (identité + contexte).
    
2. **Policy Administrator** exécute la décision (autoriser/bloquer).
    
3. **Adaptive Identity** ajuste les permissions si le contexte change (ex : déplacement géographique).
    
4. **Threat Scope Reduction** est renforcée par des politiques granulaires (moindre privilège).
    

---

#### **4. Mise en Œuvre dans un Scénario Réel**

- **Cas** : Un employé tente d’accéder à un fichier confidentiel depuis un café.
    
    - **Adaptive Identity** : Vérifie l’appareil + MFA.
        
    - **Policy Engine** : Détecte un risque (réseau public) et demande une authentification supplémentaire.
        
    - **Threat Scope Reduction** : Limite l’accès en lecture seule (pas de téléchargement).
        

---

#### **5. Technologies Associées**

- **Okta/Google BeyondCorp** : Gestion adaptive des identités.
    
- **AWS IAM** : Politiques d’accès dynamiques.
    
- **Cisco ISE** : Policy Engine pour les réseaux.
    

---


**À retenir** : Le Control Plane est la colonne vertébrale du [[Zero Trust]], reliant identité, politique et sécurité en temps réel.