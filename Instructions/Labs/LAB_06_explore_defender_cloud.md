<a name="---"></a><!---
---
Labo : Titre : « Explorer Microsoft Defender pour le cloud » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft ; Module 2 : Décrire les fonctionnalités de gestion de la sécurité d’Azure ; Unité 3 : Décrire Microsoft Defender pour le cloud »
---
--->

# <a name="lab-explore-microsoft-defender-for-cloud"></a>Labo : Explorer Microsoft Defender pour le cloud

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft
- Module : Décrire les fonctionnalités de gestion de la sécurité d’Azure
- Unité : Décrire Microsoft Defender pour le cloud

## <a name="lab-scenario"></a>Scénario du labo

Dans ce labo, vous allez explorer Microsoft Defender pour le cloud.  REMARQUE : L’abonnement Azure fourni par l’hébergeur de labo autorisé (AH) limite l’accès et peut avoir des délais plus longs que la normale.

**Durée estimée** : 30 minutes

### <a name="task-1"></a>Tâche 1

Dans cette tâche, vous allez faire une présentation générale de certaines des fonctionnalités de Microsoft Defender pour le cloud.

1. Ouvrez Microsoft Edge. Dans la barre d’adresse, entrez **portal.azure.com**.
1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez le nom d’utilisateur fourni par votre fournisseur d’hébergement de labo, puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Dans la barre de recherche bleue, entrez **Microsoft Defender pour le cloud**, puis dans la liste des résultats, sélectionnez **Microsoft Defender pour le cloud**.

1. Si c’est la première fois que vous accédez à Microsoft Defender pour le cloud avec votre abonnement, il est possible que la page Bien démarrer s’affiche et qu’une mise à niveau vous soit proposée.  Faites défiler vers le bas de la page et sélectionnez **Me le rappeler ultérieurement** (ou **Ignorer**).  Vous êtes dirigé vers la page Vue d’ensemble.

1. Dans la page Vue d’ensemble de Microsoft Defender pour le cloud, notez les informations disponibles (si vous voyez 0 ressources évaluées et recommandations actives, actualisez la page du navigateur, car le processus peut prendre quelques minutes).  Les informations en haut de la page incluent le nombre d’abonnements Azure, le nombre de ressources évaluées, le nombre de recommandations actives et les éventuelles alertes de sécurité.  Dans le corps principal de la page s’affichent des cartes qui représentent la posture de sécurité, la conformité réglementaire, les insights, etc.  Remarque : L’initiative de stratégie par défaut Microsoft Defender pour le cloud, qui doit normalement être attribuée par l’administrateur, a déjà été attribuée dans le cadre de la configuration de l’abonnement Azure. Toutefois, le niveau de sécurité affiché est de 0 %, car il peut y avoir jusqu’à 24 heures de délai pour qu’Azure reflète un score initial.

1. Sélectionnez **Ressources évaluées** en haut de la page.  (Remarque : cela équivaut à avoir sélectionné Inventaire dans le volet de navigation gauche de la page d’accueil de Microsoft Defender pour le cloud.)
    1. Vous accédez alors à la page **Inventaire** qui liste les ressources actuelles. Sélectionnez la ressource de machine virtuelle **sc900-winwm**. Cette ressource est associée à la machine virtuelle que vous avez utilisée dans le labo précédent.
    1. La page Intégrité des ressources de la machine virtuelle présente une liste de recommandations.  Dans la liste disponible, sélectionnez n’importe quel élément de la liste qui affiche un état **non sain**.
    1. Notez la description détaillée.  Cliquez sur la flèche de déroulement près des étapes de correction. Notez les instructions de correction (ou de liens vers des instructions) ainsi que l’option pour entreprendre une action.  Quittez la fenêtre sans effectuer d’action.
    1. Revenez dans la page Vue d’ensemble de Microsoft Defender pour le cloud, en sélectionnant **Microsoft Defender pour le cloud | Vue d’ensemble** en haut de la page, au-dessus de l’intitulé Intégrité des ressources.

1. Dans le volet de navigation de gauche, sélectionnez **Recommandations**.  (Notez que cela équivaut à avoir sélectionné Recommandations actives en haut de la page Vue d’ensemble de Microsoft Defender pour le cloud.)
    1. Vérifiez que l’onglet **Toutes les recommandations** est sélectionné (souligné).  Notez que la vue du tableau de bord affiche les recommandations actives par gravité, l’intégrité des ressources, etc.
    1. Notez que les éléments signalés comme des ressources non saines ont une barre rouge affichée à leur droite.  Dans la liste, sélectionnez l’une des ressources non saines.  La page qui s’ouvre contient une description, les étapes de correction et les ressources impactées. Quittez cette page en cliquant sur le **X** en haut à droite de l’écran.
    1. Quittez la page des recommandations en cliquant sur le **X** en haut à droite de l’écran. Cela vous ramènera à la page de présentation.

1. Dans le volet de navigation principal à gauche, sélectionnez **Conformité réglementaire**. La page Conformité réglementaire fournit une liste des contrôles de conformité basés sur le benchmark de sécurité cloud Microsoft (vérifiez que l’onglet Benchmark de sécurité cloud Microsoft est sélectionné/souligné). Sous chaque domaine de contrôle, vous voyez un sous-ensemble de contrôles et, pour chaque contrôle, une ou plusieurs évaluations. Chaque évaluation fournit des informations, notamment une description, une correction et les ressources impactées.
    1. Explorons l’un des domaines de contrôle. Sélectionnez (développez) **NS. Sécurité réseau**. Une liste de contrôles liés à la sécurité réseau s’affiche.
    1. Sélectionnez **NS-10. Microsoft Defender pour DNS doit être activé**. Notez la liste des évaluations automatisées (qui incluent les évaluations automatisées pour AWS) et les informations fournies pour chaque élément de ligne d’évaluation, notamment le type de ressource, les ressources ayant échoué et les états de conformité. Sélectionnez les évaluations listées.  Vous voyez ici des informations, notamment une description, des étapes de correction et les ressources impactées.
    1. Sélectionnez le **X** dans le coin supérieur droit de l’écran pour fermer la page.
    1. Sélectionnez **Vue d’ensemble** dans le volet de navigation de gauche pour revenir dans la page Vue d’ensemble de Microsoft Defender pour le cloud.
    1. Gardez la page Vue d’ensemble de Microsoft Defender pour le cloud ouverte, car vous en aurez besoin dans la prochaine tâche.

### <a name="task-2"></a>Tâche 2

Rappelons que Microsoft Defender pour le cloud est proposé en deux modes : sans fonctions de sécurité améliorées (gratuit) et avec des fonctions de sécurité améliorées qui sont disponibles dans les plans Microsoft Defender pour le cloud. Dans cette tâche, vous découvrez comment activer ou désactiver les différents plans Microsoft Defender pour le cloud.

1. Dans la page de vue d’ensemble de Microsoft Defender pour le cloud, sélectionnez **Paramètres d’environnement** dans le volet de navigation gauche.
1. Cochez la case **Développer tout**, puis sélectionnez **Abonnement MOC--lodXXXXXXXX** à côté de l’icône de clé jaune.
1. Sur la page Plans Defender, notez comment vous pouvez sélectionner Activer tout ou sélectionner des plans Defender individuels. 
    1. Vérifiez que l’état CSPM est défini sur **Activé**. Si ce n’est pas le cas, définissez-le maintenant.  
    1. Activez le plan pour l’élément Serveurs.  Sélectionnez **Activé** pour l’élément de ligne Serveurs, puis sélectionnez **Enregistrer** en haut de la page.
1. Fermez tous les onglets ouverts du navigateur.

### <a name="review"></a>Révision

Dans ce labo, vous allez explorer Microsoft Defender pour le cloud.
