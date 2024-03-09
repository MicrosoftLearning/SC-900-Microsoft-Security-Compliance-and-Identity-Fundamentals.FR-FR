---
lab:
  title: Explorer Microsoft Defender pour le cloud
  module: Describe the security management capabilities of Azure
---

# Labo : Explorer Microsoft Defender pour le cloud

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft
- Module : Décrire les fonctionnalités de gestion de la sécurité d’Azure
- Unité : Décrire la gestion de la posture de sécurité cloud

## Scénario du labo

Dans ce labo, vous allez explorer Microsoft Defender pour le cloud.  REMARQUE : L’abonnement Azure fourni par l’hébergeur de labo autorisé (AH) limite l’accès et peut avoir des délais plus longs que la normale.

**Durée estimée** : 30 minutes

### Tâche 1

Dans cette tâche, vous allez faire une présentation générale de certaines des fonctionnalités de Microsoft Defender pour le cloud.

1. Vous devez être sur la page d’accueil des services Azure.  Si vous avez précédemment fermé le navigateur, ouvrez Microsoft Edge. Dans la barre d’adresse, entrez **portal.azure.com** et connectez-vous avec vos informations d’identification d’administrateur.

1. Dans la barre de recherche bleue, entrez **Microsoft Defender pour le cloud**, puis dans la liste des résultats, sélectionnez **Microsoft Defender pour le cloud**.

1. Si c’est la première fois que vous accédez à Microsoft Defender pour le cloud avec votre abonnement, il est possible que la page Bien démarrer s’affiche et qu’une mise à niveau vous soit proposée.  Faites défiler vers le bas de la page et sélectionnez **Me le rappeler ultérieurement** (ou **Ignorer**).  Vous êtes dirigé vers la page Vue d’ensemble.

1. Dans la page Vue d’ensemble de Microsoft Defender pour le cloud, notez les informations disponibles (si vous voyez 0 ressources évaluées et recommandations actives, actualisez la page du navigateur, car le processus peut prendre quelques minutes).  Les informations en haut de la page incluent le nombre d’abonnements Azure, le nombre de ressources évaluées, le nombre de recommandations actives et les éventuelles alertes de sécurité.  Dans le corps principal de la page s’affichent des cartes qui représentent la posture de sécurité, la conformité réglementaire, les insights, etc.  Remarque : L’initiative de stratégie par défaut Microsoft Defender pour le cloud, qui doit normalement être attribuée par l’administrateur, a déjà été attribuée dans le cadre de la configuration de l’abonnement Azure. Toutefois, le niveau de sécurité affiché est de 0 %, car il peut y avoir jusqu’à 24 heures de délai pour qu’Azure reflète un score initial.

1. En haut de la page, sélectionnez **Ajouter des ressources**. 
    1. Vous accédez alors à la page **Inventaire** qui liste les ressources actuelles. Sélectionnez la ressource de machine virtuelle **sc900-winwm**. Cette ressource est associée à la machine virtuelle que vous avez utilisée dans le labo précédent.
    1. La page Intégrité des ressources de la machine virtuelle présente une liste de recommandations.  Dans la liste disponible, sélectionnez n’importe quel élément de la liste qui affiche un état **non sain**.
    1. Notez la description détaillée.  Sélectionnez la flèche déroulante située à côté des étapes de correction. Notez les instructions de correction (ou de liens vers des instructions) ainsi que l’option pour entreprendre une action.  Quittez la fenêtre sans effectuer d’action.
    1. Revenez dans la page Vue d’ensemble de Microsoft Defender pour le cloud, en sélectionnant **Microsoft Defender pour le cloud | Vue d’ensemble** en haut de la page, au-dessus de l’intitulé Intégrité des ressources.

1. Dans le volet de navigation de gauche, sélectionnez **Recommandations**.  
    1. Vérifiez que l’onglet **Toutes les recommandations** est sélectionné (souligné).  Notez que la vue du tableau de bord affiche les recommandations actives par gravité, l’intégrité des ressources, etc.
    1. Dans la liste, sélectionnez un élément.  Dans la page qui s’ouvre, vous verrez une description et des informations supplémentaires pouvant inclure des étapes de correction, des ressources affectées, etc. Fermez cette page en sélectionnant le **X** dans le coin supérieur droit de l’écran.

1. Dans le volet de navigation principal à gauche, sélectionnez **Conformité réglementaire**.  **REMARQUE** : si vous voyez qu’il n’y a pas d’abonnement pour lequel calculer la conformité, c’est parce qu’il peut y avoir un délai de 24 heures pour que l’information apparaisse. Passez à la tâche 2.  Si vous voyez des informations, procédez comme suit.
    1. La page Conformité réglementaire fournit une liste des contrôles de conformité basés sur le benchmark de sécurité cloud Microsoft (vérifiez que l’onglet Benchmark de sécurité cloud Microsoft est sélectionné/souligné). Sous chaque domaine de contrôle, vous voyez un sous-ensemble de contrôles et, pour chaque contrôle, une ou plusieurs évaluations. Chaque évaluation fournit des informations, notamment une description, une correction et les ressources impactées.
    1. Explorons l’un des domaines de contrôle. Sélectionnez (développez) **NS. Sécurité réseau**. Une liste de contrôles liés à la sécurité réseau s’affiche.
    1. Sélectionnez **NS-10. Garantir la sécurité DNS (Domain Name System)** . Notez la liste des évaluations automatisées (qui incluent les évaluations automatisées pour AWS) et les informations fournies pour chaque élément de ligne d’évaluation, notamment le type de ressource, les ressources ayant échoué et les états de conformité. Sélectionnez les évaluations listées.  Vous voyez ici des informations, notamment une description, des étapes de correction et les ressources impactées.
    1. Sélectionnez le **X** dans le coin supérieur droit de l’écran pour fermer la page.
    1. Sélectionnez **Vue d’ensemble** dans le volet de navigation de gauche pour revenir dans la page Vue d’ensemble de Microsoft Defender pour le cloud.
    1. Gardez la page Vue d’ensemble de Microsoft Defender pour le cloud ouverte, car vous en aurez besoin dans la prochaine tâche.

### Tâche 2

Rappelons que Microsoft Defender pour le cloud est proposé en deux modes : sans fonctions de sécurité améliorées (gratuit) et avec des fonctions de sécurité améliorées qui sont disponibles dans les plans Microsoft Defender pour le cloud. Dans cette tâche, vous découvrez comment activer ou désactiver les différents plans Microsoft Defender pour le cloud.

1. Dans la page de vue d’ensemble de Microsoft Defender pour le cloud, sélectionnez **Paramètres d’environnement** dans le volet de navigation gauche.
1. Cochez la case **Développer tout**, puis sélectionnez **Abonnement MOC--lodXXXXXXXX** à côté de l’icône de clé jaune.
1. Sur la page Plans Defender, notez comment vous pouvez sélectionner Activer tout ou sélectionner des plans Defender individuels. 
    1. Vérifiez que l’état CSPM est défini sur **Activé**. Si ce n’est pas le cas, définissez-le maintenant.  
    1. Activez le plan pour l’élément Serveurs.  Sélectionnez **Activé** pour l’élément de ligne Serveurs, puis sélectionnez **Enregistrer** en haut de la page.
1. En haut à gauche de la fenêtre, juste en dessous de la barre bleue qui indique Microsoft Azure, sélectionnez **Accueil** pour revenir à la page d’accueil des services Azure.
1. Gardez l’onglet Azure ouvert dans votre navigateur.

### Révision

Dans ce labo, vous allez explorer Microsoft Defender pour le cloud.
