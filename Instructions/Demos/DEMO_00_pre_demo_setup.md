<!---
---
Configuration avant la démonstration : Titre : « Configuration de la démonstration »
---
--->

## Locataires WWL : Conditions d’utilisation
Si un locataire vous est fourni dans le cadre d’une formation dispensée par un instructeur, notez qu’il est mis à votre disposition dans le seul but de prendre en charge les labos pratiques de la formation.

Vous ne devez ni partager ni utiliser les locataires en dehors des labos pratiques. Le locataire utilisé dans ce cours est un locataire d’essai. Au terme de la classe, le locataire ne pourra pas faire l’objet d’une prolongation et vous ne pourrez plus l’utiliser ni y accéder.

Vous n’êtes pas autorisé à convertir un locataire en abonnement payant. Les locataires obtenus dans le cadre de ce cours sont la propriété de Microsoft Corporation. Nous nous réservons le droit d’y accéder et d’en reprendre possession à tout moment.

## Configuration avant la démonstration du locataire Microsoft 365

### Activer le journal d’audit de Microsoft 365

Lors de cette tâche de configuration, vous allez activer la fonction de journal d’audit dans Microsoft 365.  Bien que la documentation indique que le journal d’audit est activé par défaut, la plupart des locataires de labo n’ont pas cette fonctionnalité activée. Il peut se passer plusieurs heures avant que l’activation ne prenne effet.  Il est conseillé d’activer cette fonctionnalité, car Microsoft 365 utilise les journaux d’audit pour les insights utilisateur, les activités identifiées dans les stratégies et les insights d’analyse.

1. Ouvrez Microsoft Edge. Dans la barre d’adresse, entrez **https://admin.microsoft.com** .

1. Connectez-vous avec les informations d’identification d’administrateur du locataire Microsoft 365 fournies par votre hôte de laboratoire autorisé (ALH).

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous les Centres d’administration, sélectionnez **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.  

1. Dans le volet de navigation situé à gauche du portail de conformité Microsoft Purview, sélectionnez **Tout afficher**.

1. Dans le volet de navigation à gauche, sélectionnez **Audit**.  Remarque : la fonctionnalité d’audit est également accessible depuis la page d’accueil de Microsoft 365 Defender.

1. Vérifiez que l’onglet **Recherche** est sélectionné (souligné).

1. Quand vous arrivez sur la page Audit, attendez 2 à 3 minutes.  Si l’audit n’est PAS activé, vous voyez une barre bleue en haut de la page indiquant de commencer à enregistrer les activités des utilisateurs et des administrateurs.  Sélectionnez **Commencer à enregistrer les activités des utilisateurs et des administrateurs**.  Une fois que l’audit est activé, la barre bleue disparaît.  S’il n’y a pas de barre bleue, l’audit est déjà activé et aucune autre action n’est nécessaire.

1. Retournez à la page d’accueil du portail de conformité Microsoft Purview en sélectionnant **Accueil** dans le volet de navigation de gauche.

### Supervision de fichiers de Microsoft Defender pour les applications cloud

Dans cette tâche de configuration, vous allez activer la supervision de fichiers dans Microsoft Defender pour les applications cloud.

1. Ouvrez l’onglet du navigateur pour le Centre d’administration Microsoft 365.  Si vous l’avez précédemment fermé, ouvrez un nouvel onglet de navigateur et entrez **https://admin.microsoft.com** dans la barre d’adresse, puis sélectionnez **Afficher tout** dans le volet de navigation de gauche du centre d’administration Microsoft 365.

1. Sous les centres d’administration, sélectionnez **Sécurité**.  Une nouvelle page de navigation s’ouvre sur la page d’accueil du portail Microsoft 365 Defender.  

1. Dans le volet de navigation de gauche, sélectionnez **Fichiers**, qui est répertorié sous Applications cloud.

1. S’il n’est pas déjà activé, vous devez sélectionner **Activer la supervision de fichier**, cocher la case en regard de l’option **Activer la supervision de fichier**, puis sélectionner **Enregistrer**.  

1. Dans le volet de navigation de gauche, sous applications cloud, sélectionnez **Fichiers** pour revenir à la page des fichiers.  Si vous avez correctement activé la supervision de fichiers, vous devriez voir les options de filtre en haut de la page.  L’affichage des fichiers du locataire de labo préconfiguré peut prendre un certain temps.

## Configuration avant la démonstration de l’abonnement Azure Cloud Slice

Pour cette configuration, vous utilisez l’environnement Azure Cloud Slice qui est distinct du locataire Microsoft 365 fourni. Déconnectez-vous du locataire Microsoft 365 et connectez-vous à l’aide des informations d’identification Azure Cloud Slice.

### Machine virtuelle Azure

Vérifiez qu’une machine virtuelle a déjà été créée. Si ce n’est pas le cas, configurez-la maintenant. Vous utiliserez la machine virtuelle dans le cadre de la démonstration du groupe de sécurité réseau.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse, entrez **https://portal.azure.com** et connectez-vous avec les informations d’identification Azure fournies par l’hébergeur de labo agréé.  Cela vous amène à la page d’accueil des services Azure.

1. Dans la zone de recherche bleue en haut de la page, entrez **Machines virtuelles** et sélectionnez **Machines virtuelles** dans les résultats de la recherche.

1. Si une machine virtuelle est déjà répertoriée, ignorez les étapes suivantes, sinon vous devez en créer une.  Sélectionnez **Créer**, puis, dans le menu déroulant, sélectionnez **Machine virtuelle Azure**. Configurez les paramètres suivants (si aucun paramètre n’est répertorié, conservez la valeur par défaut).
    1. Groupe de ressources : sélectionnez **Créer nouveau** et entrez **LabsSC900**, puis sélectionnez **OK**.
    1. Identité des machines virtuelles : entrez **SC900-WinVM**.
    1. Options de disponibilité : dans la liste déroulante, sélectionnez **Aucune redondance d’infrastructure requise**.
    1. Image : dans la liste déroulante, sélectionnez **Windows 11 Professionnel, version 22H2 - x64 Gen2** (ou toute image Windows 10 ou Windows 11 répertoriée).
    1. Taille : sélectionnez **Voir toutes les tailles** et sélectionnez **Standard_B1s**, puis sélectionnez **Sélectionner** en bas de la page.
    1. Nom d’utilisateur : entrez **SC900-VM-User**
    1. Mot de passe : entrez un mot de passe et notez-le, vous en aurez besoin ultérieurement !
    1. Confirmer le mot de passe : entrez à nouveau le mot de passe.
    1. Ports d’entrée publics : **Aucun**.
    1. Licences : sélectionnez l’option « Je confirme que je dispose d’une licence Windows 10/11 éligible avec des droits d’hébergement multilocataire ».  Une coche doit apparaître.
    1. Sélectionnez **Suivant : Disques**
    1. Type de disque de système d’exploitation : dans la liste déroulante, sélectionnez **SSD Standard**.
    1. Sélectionnez **Suivant : Réseaux**
    1. Groupe de sécurité réseau de la carte réseau : sélectionnez **Aucun**.  Vous allez créer un groupe de sécurité réseau dans le cadre de la démonstration, donc ne le faites pas ici !
    1. Supprimer l’IP publique et la carte réseau lorsque la machine virtuelle est supprimée : activez la case pour qu’une coche s’affiche.
    1. Sélectionnez **Vérifier + créer**, puis quand la validation réussit, sélectionnez **Créer**.
    1. Une fois le déploiement de la machine virtuelle terminé, sélectionnez **Accueil** en haut de la page.

1. Conservez l’onglet du navigateur Azure ouvert pour poursuivre la configuration avant la démonstration.

### Un groupe de sécurité réseau

Vérifiez qu’un groupe de sécurité réseau a déjà été créé. Si le groupe de sécurité réseau n’a pas été créé, configurez-le maintenant, mais ne lui associez aucune interface et ne créez pas de règles. Ces étapes seront effectuées dans le cadre de la démonstration du groupe de sécurité réseau.

1. Dans la barre de recherche bleue en haut de la page, entrez **Groupes de sécurité réseau**. Dans les résultats, sélectionnez **Groupes de sécurité réseau** (ne sélectionnez pas Groupes de sécurité réseau classiques).

1. Sélectionnez **Créer un groupe de sécurité réseau**. Sous l’onglet de base de la page Créer un groupe de sécurité réseau, spécifiez les paramètres suivants :
    1. Abonnement : conservez la valeur par défaut (il s’agit de l’abonnement Azure fourni par l’hébergeur de labo autorisé)
    1. Groupe de ressources :  **LabsSC900**
    1. Nom :  **NSG-SC900**
    1. Région : laissez la valeur par défaut.
    1. Sélectionnez **Examiner et créer** puis sélectionnez **Créer**.
    1. Une fois que le déploiement est terminé (l’opération est très rapide), sélectionnez **Accéder à la ressource**.

### Microsoft Defender pour le cloud

L’objectif ici est simplement d’accéder à Microsoft Defender pour le cloud pour la première fois. Cela est important, car Defender pour le cloud peut prendre jusqu’à 24 heures pour refléter un score de sécurité initial.  

1. Ouvrez l’onglet Accueil - Microsoft Azure dans votre navigateur.

1. Dans la barre de recherche bleue, entrez **Microsoft Defender pour le cloud**, puis dans la liste des résultats, sélectionnez **Microsoft Defender pour le cloud**.

1. Si c’est la première fois que vous accédez à Microsoft Defender pour le cloud avec votre abonnement, il est possible que la page Bien démarrer s’affiche et qu’une mise à niveau vous soit proposée.  Faites défiler vers le bas de la page et sélectionnez **Ignorer**.  Vous êtes dirigé vers la page Vue d’ensemble.

1. Tous les abonnements ont un CSPM fondamental activé par défaut qui fournit un score de sécurité, mais il peut s’écouler jusqu’à 24 heures avant que Defender pour le cloud ne reflète un score de sécurité initial.

1. Sélectionnez **Accueil** en haut de la page.

1. Conservez l’onglet du navigateur ouvert pour poursuivre la configuration avant la démonstration.

### Microsoft Sentinel

Vérifiez qu’une instance de Microsoft Sentinel a déjà été créée. Si ce n’est pas le cas, configurez-la maintenant, car vous en aurez besoin dans le cadre de la démonstration pas à pas sur Microsoft Sentinel.

1. Ouvrez l’onglet Accueil - Microsoft Azure dans votre navigateur.

1. Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **Sentinel** puis sélectionnez **Microsoft Sentinel** à partir des résultats de la recherche.

1. Dans la page Microsoft Sentinel, sélectionnez **Créer Microsoft Sentinel**.

1. Dans la page Ajouter Microsoft Sentinel à un espace de travail, sélectionnez **Créer un espace de travail**.

1. À partir de l’onglet de base de l’espace de travail Créer un journal d’analyses, saisissez les informations suivantes :
    1. Abonnement : conservez la valeur par défaut.
    1. Groupe de ressources : sélectionnez **Créer un nouveau**, puis saisissez le nom **SC900-Sentinel-RG** et sélectionnez **OK**.
    1. Nom : **SC900-LogAnalytics-workspace**.
    1. Région : **USA Est** (une autre région par défaut peut être sélectionnée en fonction de votre localisation).
    1. Sélectionnez **Vérifier + Créer** (aucune étiquette n’est configurée).
    1. Vérifiez les informations que vous avez saisies, puis sélectionnez **Créer**.
    1. Cela peut prendre une ou deux minutes avant que l’espace de travail n’apparaisse. Si vous ne le voyez toujours pas, sélectionnez **Actualiser**, puis **Ajouter**.

1. Une fois le nouvel espace de travail ajouté, la page Microsoft Sentinel | Actualités et guides s’affiche, indiquant que l’essai gratuit de Microsoft Sentinel est activé.  Sélectionnez **OK**.

### Révision

Dans cette configuration, vous avez activé la fonctionnalité de journal d’audit dans votre locataire Microsoft 365 et vous avez également créé ou vérifié qu’une machine virtuelle a été préconfigurée dans votre environnement Azure Cloud Slice. Vous avez également préparé votre environnement Defender pour le cloud et Microsoft Sentinel.
