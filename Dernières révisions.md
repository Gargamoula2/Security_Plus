[[Security+]]

| **Type de Security Control**             | **Définition**                                                         | **Exemples concrets**                                                                     |
| ---------------------------------------- | ---------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| **Preventive Security Control**          | Empêche les incidents avant qu'ils ne se produisent.                   | Pare-feu, contrôle d'accès, authentification à deux facteurs (2FA), mises à jour.         |
| **Detective Security Control**           | Détecte et alerte lorsqu’un incident survient.                         | IDS (Intrusion Detection System), journaux d’audit, caméras de surveillance.              |
| **Corrective Security Control**          | Rétablit les systèmes après un incident ou corrige les vulnérabilités. | Restaurations de sauvegardes, correctifs logiciels, procédures de réponse aux incidents.  |
| **Deterrent Security Control**           | Dissuade un acteur malveillant d’agir.                                 | Panneaux de vidéosurveillance, avertissements juridiques, présence de gardes de sécurité. |
| **Compensating Security Control**        | Remplace ou compense un contrôle manquant ou non applicable.           | Revue manuelle des logs en l’absence d’un SIEM, restrictions réseau en l'absence de 2FA.  |
| **Physical Security Control**            | Empêche l’accès physique non autorisé aux ressources.                  | Serrures, barrières, badges, cartes magnétiques, cages Faraday.                           |
| **Administrative (Managerial) Control**  | Définit les politiques, les procédures et les formations.              | Politique de sécurité, plan de continuité, formations de sensibilisation.                 |
| **Technical (Logical) Security Control** | Implémenté par des moyens technologiques.                              | Antivirus, chiffrement, contrôle d’accès basé sur les rôles (RBAC), DLP.                  |

| Catégories      | Description / Exemple                                                                                                                                               |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Technical**   | Contrôles basés sur la technologie pour protéger les systèmes et données (ex. antivirus, pare-feu, chiffrement, MFA).                                               |
| **Managerial**  | Contrôles liés aux politiques et à la gestion du risque (ex. politiques de sécurité, formations, audits, gestion des accès).                                        |
| **Operational** | Contrôles liés aux processus et procédures pour sécuriser les opérations quotidiennes (ex. gestion des incidents, sauvegardes, surveillance réseau).                |
| **Physical**    | Contrôles qui protègent l’infrastructure physique et l’accès aux installations (ex. badges d’accès, caméras de surveillance, serrures, contrôles environnementaux). |

- **Risk Management** - Processus d'identification, d'analyse et de traitement des risques.
    
- **Risk Owner** - Personne responsable de prendre des décisions sur un risque spécifique.
    
- **Risk Assessor** - Professionnel qui évalue et analyse les risques.
    
- **Risk Assessment** - Évaluation des risques (qualitative : jugement expert ; quantitative : calculs financiers comme ALE=SLE×ARO).
    
- **Risk Appetite** - Niveau de risque qu'une organisation est prête à accepter globalement (souvent une tendance d'entreprise).
    
- **Risk Tolerance** - Marge de variation acceptable autour de l'appétence au risque (souvent en pourcentage).
    
- **Risk Transfer** - Faire porter le risque par un tiers (ex : assurance).
    
- **Risk Register** - Document listant tous les risques identifiés et leurs caractéristiques.
    
- **Risk Analysis** - Processus d'étude des risques (méthodes qualitatives ou quantitatives).
    
- **Risk Reporting** - Communication des résultats de l'évaluation des risques aux parties prenantes.
    
- **Risk Threshold** - Niveau spécifique de risque au-delà duquel une action est requise.
    
- **Risk Matrix** - Matrice imageant le risque par sa probabilité et sa gravité


- **Data Controller** - L’entité (entreprise, organisation, parfois une personne) qui décide pourquoi et comment les données personnelles sont collectées et utilisées.
    
- **Data Custodian** - Responsable de la fiabilité, l'anonymisation et la sécurité de la donnée
    
- **Data Subject** - Individu concerné par les données personnelles collectées (ex : client).
    
- **Data Processor** - Organisation externe qui traite les données pour le compte du contrôleur 
	(ex : fournisseur cloud).
     
- **Data Owner** - Responsable des données, souvent une personne haut placé
	
- **Data Plane** - Gère la transmission de la donnée entre les systèmes/services à travers le réseau

**Incremental backup VS Differential backup

**SPF** : est-ce que le serveur qui envoie le mail est autorisé à envoyer sur mon domaine ?
**DKIM** : est-ce que la signature du mail est valide (Intégrité/Authenticité) ?
**DMARC** : si SPF ou DKIM ou les deux ne sont pas valides, qu'est ce que je fais (quarantaine/bloquer le mail...)

**CASB** : outil qui contrôle et sécurise l’accès aux services cloud et protège les données

**OpenID -> Authentication
OAuth -> Authorization
RADIUS** 

![[Pasted image 20250820161547.png]]