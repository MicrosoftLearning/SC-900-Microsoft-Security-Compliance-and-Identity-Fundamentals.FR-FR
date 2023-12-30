<!---
---
Démo : Titre : « Microsoft Defender pour le cloud » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft ; Module 2 : Décrire les fonctionnalités de gestion de la sécurité d’Azure ; Unité 3 : Décrire la gestion de la posture de sécurité cloud »
---
--->

# Démo : Microsoft Defender pour le cloud

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft
- Module : Décrire les fonctionnalités de gestion de la sécurité d’Azure
- Unité : Décrire la gestion de la posture de sécurité cloud

## Scénario de démonstration

Cette démonstration vous permettra d’explorer Microsoft Defender pour le cloud et de montrer comment utiliser cette solution pour améliorer la posture de sécurité d’une organisation.  REMARQUE : L’abonnement Azure géré par l’hébergeur de labo autorisé (AH) peut limiter certains accès et avoir des délais plus longs que la normale.

### Partie 1 de la démonstration

Dans cette tâche de démonstration, vous allez faire une présentation générale de certaines des fonctionnalités de Microsoft Defender pour le cloud.

1. Ouvrez l’onglet du navigateur, **Accueil - Microsoft Azure**.  Si vous avez fermé l’onglet, ouvrez une page du navigateur et saisissez **https://portal.azure.com** dans la barre d’adresse. Connectez-vous avec les informations d’identification Azure fournies par l’hôte de laboratoire autorisé (ALH).  Cela vous amène à la page d’accueil des services Azure.

1. Dans la barre de recherche bleue, entrez **Microsoft Defender pour le cloud**, puis dans la liste des résultats, sélectionnez **Microsoft Defender pour le cloud**.

1. Si c’est la première fois que vous accédez à Microsoft Defender pour le cloud avec votre abonnement, il est possible que la page Bien démarrer s’affiche et qu’une mise à niveau vous soit proposée.  Faites défiler vers le bas de la page et sélectionnez **Ignorer**.  Vous êtes dirigé vers la page Vue d’ensemble. Dans la page Vue d’ensemble de Microsoft Defender pour le cloud, remarquez les informations qui y sont disponibles.  Les informations en haut de la page incluent le nombre d’abonnements Azure, le nombre de ressources évaluées, le nombre de recommandations actives et les éventuelles alertes de sécurité.  Dans le corps principal de la page s’affichent des cartes qui représentent la posture de sécurité, la conformité réglementaire, les insights, etc.  Pour tous les abonnements, le CSPM fondamental est activé par défaut, ce qui permet d’obtenir un niveau de sécurité.  
    1. Si la valeur du niveau de sécurité est de 0 %, cela est dû au délai de 24 heures qui peut s’écouler avant qu’Azure ne reflète un score initial.  
    1. Il est également important de souligner que Defender for Cloud est une solution multicloud qui peut vous aider à améliorer votre posture de sécurité non seulement avec Azure, mais aussi avec AWS et Google Cloud Platform.

1. La première chose que vous voulez montrer est que Microsoft Defender pour le cloud utilise le benchmark de sécurité de Microsoft Cloud comme initiative de stratégie par défaut.  Dans le volet de navigation de gauche, sélectionnez **Paramètres de l’environnement** Dans la fenêtre principale, sélectionnez **Tout développer**.  Votre abonnement apparaît en bleu dans l’affichage développé.  Sélectionnez l’abonnement **MOC Subscription--lodXXXXXX.**

1. Dans le volet de navigation de gauche, sélectionnez **Stratégie de sécurité**, sous les paramètres de la stratégie. Si l’initiative par défaut n’est pas affectée, sélectionnez **Affecter une stratégie**.
    1. Remarquez que sur l’onglet des informations de base, la définition de l’initiative est le benchmark de sécurité de Microsoft Cloud.  Cette définition est grisée car il s’agit de l’initiative par défaut et nous ne faisons que l’affecter.
    1. Sélectionnez **Vérifier + créer**, puis sélectionnez **Créer**. Si vous le souhaitez, vous pouvez faire défiler les paramètres configurables des différents onglets avant de sélectionner l’option de révision et de création.
    1. Il s’agit d’une étape importante pour s’assurer que vous pouvez voir les recommandations de sécurité basées sur le benchmark de sécurité de Microsoft Cloud.  

1. Remarquez également que vous pouvez ajouter des normes industrielles et réglementaires prêtes à l’emploi. Si les normes répertoriées sont considérées comme déconseillées, sélectionnez **Ajouter d’autres normes** pour obtenir une liste complète.  Sélectionnez une norme dans la liste, puis ajoutez-la manuellement en sélectionnant **Vérifier + créer**, puis **Créer**.  Elle sera ajoutée à la liste des réglementations sectorielles et normatives.

1. Sélectionnez **Vue d’ensemble**.  Dans le corps principal de la page s’affichent des cartes qui représentent la posture de sécurité, la conformité réglementaire, les insights, etc.  Pour tous les abonnements, le CSPM fondamental est activé, ce qui permet d’obtenir un niveau de sécurité. La valeur affichée est de 0 %, car il peut y avoir jusqu’à 24 heures de délai pour qu’Azure reflète un score initial.  Bien que le niveau de sécurité soit actuellement de 0 %, rappelez que Defender for Cloud est une solution multicloud qui peut vous aider à améliorer votre posture de sécurité non seulement avec Azure, mais aussi avec AWS et Google Cloud Platform.

1. En haut de la page, sélectionnez **Ajouter des ressources**.  (Remarque : cela équivaut à avoir sélectionné Inventaire dans le volet de navigation gauche de la page d’accueil de Microsoft Defender pour le cloud.)
    1. Vous accédez alors à la page **Inventaire** qui liste les ressources actuelles. Sélectionnez la ressource de machine virtuelle **sc900-winwm**. Cette ressource est associée à la machine virtuelle que vous avez utilisée dans le labo précédent ou la démo précédente.
    1. La page Intégrité des ressources de la machine virtuelle présente une liste de recommandations.  Dans la liste disponible, sélectionnez n’importe quel élément de la liste qui affiche un état **non sain**.
    1. Notez la description détaillée.  Sélectionnez la flèche déroulante située à côté des étapes de correction. Notez les instructions de correction (ou de liens vers des instructions) ainsi que l’option pour entreprendre une action.  Quittez la fenêtre sans effectuer d’action.
    1. Revenez dans la page Vue d’ensemble de Microsoft Defender pour le cloud, en sélectionnant **Microsoft Defender pour le cloud | Vue d’ensemble** en haut de la page, au-dessus de l’intitulé Intégrité des ressources.

1. Dans le volet de navigation de gauche, sélectionnez **Recommandations**.  (Notez que cela équivaut à avoir sélectionné Recommandations actives en haut de la page Vue d’ensemble de Microsoft Defender pour le cloud.)
    1. Vérifiez que l’onglet **Toutes les recommandations** est sélectionné (souligné).  Notez que la vue du tableau de bord affiche les recommandations actives par gravité, l’intégrité des ressources, etc.
    1. Notez que les éléments signalés comme des ressources non saines ont une barre rouge affichée à leur droite.  Dans la liste, sélectionnez l’une des ressources non saines.  La page qui s’ouvre contient une description, les étapes de correction et les ressources impactées. Fermez cette page en sélectionnant le **X** dans le coin supérieur droit de l’écran.
    1. Quittez la page des recommandations en sélectionnant le **X** dans le coin supérieur droit de l’écran, pour revenir à la page de vue d’ensemble.

1. Dans le volet de navigation principal à gauche, sélectionnez **Conformité réglementaire**.  **REMARQUE** : si vous voyez qu’il n’y a pas d’abonnement pour lequel calculer la conformité, c’est parce qu’il peut y avoir un délai de 24 heures pour que l’information apparaisse. Passez à la tâche 2.  Si vous voyez des informations, procédez comme suit.
    1. La page Conformité réglementaire fournit une liste des contrôles de conformité basés sur le benchmark de sécurité cloud Microsoft (vérifiez que l’onglet Benchmark de sécurité cloud Microsoft est sélectionné/souligné). Sous chaque domaine de contrôle, vous voyez un sous-ensemble de contrôles et, pour chaque contrôle, une ou plusieurs évaluations. Chaque évaluation fournit des informations, notamment une description, une correction et les ressources impactées.
    1. Explorons l’un des domaines de contrôle. Sélectionnez (développez) **NS. Sécurité réseau**. Une liste de contrôles liés à la sécurité réseau s’affiche.
    1. Sélectionnez **NS-10. Microsoft Defender pour DNS doit être activé**. Notez la liste des évaluations automatisées (qui incluent les évaluations automatisées pour AWS) et les informations fournies pour chaque élément de ligne d’évaluation, notamment le type de ressource, les ressources ayant échoué et les états de conformité. Sélectionnez les évaluations listées.  Vous voyez ici des informations, notamment une description, des étapes de correction et les ressources impactées.
    1. Sélectionnez le **X** dans le coin supérieur droit de l’écran pour fermer la page.
    1. Sélectionnez **Vue d’ensemble** dans le volet de navigation de gauche pour revenir dans la page Vue d’ensemble de Microsoft Defender pour le cloud.
    1. Gardez la page Vue d’ensemble de Microsoft Defender pour le cloud ouverte, car vous en aurez besoin dans la prochaine tâche.

### Partie 2 de la démonstration

Rappelons que Microsoft Defender pour le cloud est proposé en deux modes : sans fonctions de sécurité améliorées (gratuit) et avec des fonctions de sécurité améliorées qui sont disponibles dans les plans Microsoft Defender pour le cloud. Dans cette tâche, vous découvrez comment activer ou désactiver les différents plans Microsoft Defender pour le cloud.

1. Dans la page de vue d’ensemble de Microsoft Defender pour le cloud, sélectionnez **Paramètres d’environnement** dans le volet de navigation gauche.
1. Cochez la case **Développer tout**, puis sélectionnez **Abonnement MOC--lodXXXXXXXX** à côté de l’icône de clé jaune.
1. Sur la page Plans Defender, notez comment vous pouvez sélectionner Activer tout ou sélectionner des plans Defender individuels. 
    1. Vérifiez que l’état CSPM est défini sur **Activé**. Si ce n’est pas le cas, définissez-le maintenant.  
    1. Activez le plan pour l’élément Serveurs.  Sélectionnez **Activé** pour l’élément de ligne Serveurs, puis sélectionnez **Enregistrer** en haut de la page.
1. Laissez l’onglet Azure ouvert dans votre navigateur pour la prochaine démo Azure.

## Révision

Dans cette démo, vous avez réalisé une présentation générale de Microsoft Defender pour le cloud et montré comment le Niveau de sécurité Azure peut être utilisé pour améliorer la posture de sécurité d’une organisation.
