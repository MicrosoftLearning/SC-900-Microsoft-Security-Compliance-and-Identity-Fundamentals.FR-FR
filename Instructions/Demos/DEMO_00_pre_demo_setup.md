<!---
---
Configuration avant la démonstration : Titre : « Configuration de la démonstration »
---
--->

## Locataires WWL - Conditions d’utilisation
Si un locataire vous est fourni dans le cadre d’une formation dispensée par un instructeur, notez qu’il est mis à votre disposition dans le seul but de prendre en charge les labos pratiques de la formation.

Vous ne devez ni partager ni utiliser les locataires en dehors des labos pratiques. Le locataire utilisé dans ce cours est un locataire d’essai. Au terme de la classe, le locataire ne pourra pas faire l’objet d’une prolongation et vous ne pourrez plus l’utiliser ni y accéder.

Vous n’êtes pas autorisé à convertir un locataire en abonnement payant. Les locataires obtenus dans le cadre de ce cours sont la propriété de Microsoft Corporation. Nous nous réservons le droit d’y accéder et d’en reprendre possession à tout moment.

## Configuration de la pré-démo du locataire Microsoft 365

### Activer le journal d’audit de Microsoft 365

Lors de cette tâche de configuration, vous allez activer la fonction de journal d’audit dans Microsoft 365.  Bien que la documentation indique que le journal d’audit est activé par défaut, la plupart des locataires de labo n’ont pas cette fonctionnalité activée. Il peut se passer plusieurs heures avant que l’activation ne prenne effet.  Il est conseillé d’activer cette fonctionnalité, car Microsoft 365 utilise les journaux d’audit pour les insights utilisateur, les activités identifiées dans les stratégies et les insights d’analyse.

1. Ouvrez Microsoft Edge. Dans la barre d’adresse, entrez **https://admin.microsoft.com** .

1. Connectez-vous avec les informations d’identification d’administrateur du locataire Microsoft 365 fournis par votre hôte de labo autorisé (ALH).

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous Centres d’administration, sélectionnez **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.  

1. Dans le volet de navigation situé à gauche du portail de conformité Microsoft Purview, sélectionnez **Tout afficher**.

1. Dans le volet de navigation de gauche, sous Solutions, sélectionnez **Audit**.  Remarque : la fonctionnalité d’audit est également accessible via la page d’accueil de Microsoft 365 Defender.

1. Vérifiez que l’onglet **Recherche** est sélectionné (souligné).

1. Lorsque vous arrivez sur la page Audit, attendez 2 à 3 minutes.  Si l’audit n’est PAS activé, vous voyez une barre bleue en haut de la page indiquant de commencer à enregistrer les activités des utilisateurs et des administrateurs.  Sélectionnez **Commencer à enregistrer les activités de l’utilisateur et de l’administrateur**.  Une fois l’audit activé, la barre bleue disparaît.  S’il n’y a pas de barre bleue, alors l’audit est déjà activé et aucune autre action n’est requise.

1. Retournez à la page d’accueil du portail de conformité Microsoft Purview en sélectionnant **Accueil** dans le volet de navigation de gauche.

### Surveillance des fichiers par Microsoft Defender for Cloud Apps

Dans cette tâche de configuration, vous allez activer la surveillance des fichiers dans Microsoft Defender for Cloud Apps.

1. Ouvrez l’onglet du navigateur du Centre d’administration Microsoft 365.  Si vous l’aviez fermé, ouvrez un nouvel onglet de navigateur et saisissez **https://admin.microsoft.com** dans la barre d’adresse, puis sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous Centres d’administration, sélectionnez **Sécurité**.  Une nouvelle page de navigateur s’ouvre sur la page d’accueil du portail Microsoft 365 Defender.  

1. Dans le volet de navigation de gauche, sélectionnez **Fichiers**, sous Logiciels cloud.

1. Si ce n’est pas déjà fait, sélectionnez **Activer la supervision de fichier**, cochez la case en regard de l’option **Activer la supervision de fichier**, puis sélectionnez **Enregistrer**.  

1. Dans le volet de navigation de gauche, sous Logiciels cloud, sélectionnez **Fichiers** pour revenir à la page des fichiers.  Si vous avez bien activé la surveillance des fichiers, vous devriez voir les options de filtrage en haut de la page.  L’affichage des fichiers du locataire du labo préconfiguré peut prendre un certain temps.

## Configuration de la pré-démo de l’abonnement Azure Cloud Slice

Pour cette configuration, vous utilisez l’environnement Azure Cloud Slice qui est distinct du locataire Microsoft 365 fourni. Déconnectez-vous du locataire Microsoft 365 et connectez-vous à l’aide des informations d’identification Azure Cloud Slice.

### Machine virtuelle Azure

Vérifiez qu’une machine virtuelle a déjà été créée. Si ce n’est pas le cas, configurez-la maintenant. Vous utiliserez la machine virtuelle dans le cadre de la démo du NSG.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse, entrez **https://portal.azure.com** et connectez-vous avec les informations d’identification Azure fournies par l’hébergeur de labo agréé.  Cela vous amène à la page d’accueil des services Azure.

1. Dans la zone de recherche bleue en haut de la page, entrez **Machines virtuelles** et sélectionnez **Machines virtuelles** dans les résultats de la recherche.

1. Si une machine virtuelle est déjà répertoriée, ignorez les étapes qui suivent, sinon créez-en une.  Sélectionnez **Créer** dans le menu déroulant, puis **Machine virtuelle Azure**. Configurez les paramètres suivants (si un paramètre n’est pas répertorié, laissez la valeur par défaut).
    1. Groupe de ressources : sélectionnez **Créer**, saisissez **LabsSC900**, puis sélectionnez **OK**.
    1. Nom de la machine virtuelle : entrez **SC900-WinVM**.
    1. Options de disponibilité : **sélectionnez Aucune redondance d’infrastructure requise** dans le menu déroulant.
    1. Image : dans la liste déroulante, sélectionnez **Windows 11 Pro, version 22H2 (x64 Gen2)** (ou toute image Windows 10 ou Windows 11 répertoriée).
    1. Taille : sélectionnez **Afficher toutes les tailles**, **Standard_B1s**, puis **Sélectionner** en bas de la page.
    1. Nom d’utilisateur : saisissez **SC900-VM-User**.
    1. Mot de passe : saisissez un mot de passe et notez-le. Vous en aurez besoin ultérieurement.
    1. Confirmer le mot de passe : saisissez à nouveau le mot de passe.
    1. Ports d’entrée publics : **Aucun**.
    1. Octroi de licence : sélectionnez la mention « Je confirme que j’ai une licence Windows 10/11 éligible avec des droits d’hébergement multilocataire. »  Une coche doit apparaître.
    1. Sélectionnez **Suivant : Disques**.
    1. Type de disque du système d’exploitation : dans la liste déroulante, sélectionnez **SSD Standard**.
    1. Sélectionnez **Suivant : Mise en réseau**.
    1. Groupe de sécurité réseau de la carte réseau : sélectionnez **Aucun**.  Vous créerez un NSG dans le cadre de la démo, alors ne le faites pas maintenant.
    1. Supprimer l’IP et le NIC publics lorsque la machine virtuelle est supprimée : cochez la case.
    1. Sélectionnez **Vérifier + créer**, puis quand la validation réussit, sélectionnez **Créer**.
    1. Une fois le déploiement de la machine virtuelle terminé, sélectionnez **Accueil** en haut de la page.

1. Laissez l’onglet du navigateur Azure ouvert pour poursuivre la configuration de la pré-démo.

### Groupe de sécurité réseau

Vérifiez qu’un NSG a déjà été créé. Si le NSG n’a pas été créé, configurez-le maintenant, mais n’y associez aucune interface et ne créez aucune règle. Ces étapes seront réalisées dans le cadre de la démo du NSG.

1. Dans la barre de recherche bleue en haut de la page, entrez **Groupes de sécurité réseau**. Dans les résultats, sélectionnez **Groupes de sécurité réseau** (ne sélectionnez pas Groupes de sécurité réseau classiques).

1. Sélectionnez **Créer un groupe de sécurité réseau**. Sous l’onglet Options de base de la page Créer un groupe de sécurité réseau, spécifiez les paramètres suivants :
    1. Abonnement : conservez la valeur par défaut (il s’agit de l’abonnement Azure fourni par l’hébergeur de labo autorisé)
    1. Groupe de ressources : **LabsSC900**
    1. Nom : **NSG-SC900**
    1. Région : laissez la valeur par défaut.
    1. Sélectionnez **Vérifier + créer**, puis sélectionnez **Créer**.
    1. Une fois que le déploiement est terminé (l’opération est très rapide), sélectionnez **Accéder à la ressource**.

### Microsoft Defender pour le cloud

L’objectif ici est simplement d’accéder à Microsoft Defender pour le cloud pour la première fois. Cette étape est importante car Defender pour le cloud peut prendre jusqu’à 24 heures pour indiquer un premier niveau de sécurité.  

1. Ouvrez l’onglet Accueil - Microsoft Azure dans votre navigateur.

1. Dans la barre de recherche bleue, entrez **Microsoft Defender pour le cloud**, puis dans la liste des résultats, sélectionnez **Microsoft Defender pour le cloud**.

1. Si c’est la première fois que vous accédez à Microsoft Defender pour le cloud avec votre abonnement, il est possible que la page Bien démarrer s’affiche et qu’une mise à niveau vous soit proposée.  Faites défiler vers le bas de la page et sélectionnez **Ignorer**.  Vous êtes dirigé vers la page Vue d’ensemble.

1. Le CSPM de base est activé par défaut pour tous les abonnements, ce qui permet d’obtenir un niveau de sécurité, mais Defender for Cloud peut prendre jusqu’à 24 heures pour indiquer un niveau de sécurité initial.

1. Sélectionnez **Accueil** dans la partie supérieure de la page.

1. Laissez l’onglet du navigateur ouvert pour poursuivre la configuration de la pré-démo.

### Microsoft Sentinel

Vérifiez qu’une instance de Microsoft Sentinel a déjà été créée. Si ce n’est pas le cas, configurez-la maintenant, car vous en aurez besoin dans le cadre de la démo sur Microsoft Sentinel.

1. Ouvrez l’onglet Accueil - Microsoft Azure dans votre navigateur.

1. Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **Sentinel** puis sélectionnez **Microsoft Sentinel** à partir des résultats de la recherche.

1. Dans la page Microsoft Sentinel, sélectionnez **Créer Microsoft Sentinel**.

1. Dans la page Ajouter Microsoft Sentinel à un espace de travail, sélectionnez **Créer un espace de travail**.

1. Dans l’onglet Informations de base de la création d’espace de travail Log Analytics, saisissez les informations suivantes :
    1. Abonnement : conservez la valeur par défaut.
    1. Groupe de ressources : sélectionnez **Créer**, saisissez le nom **SC900-Sentinel-RG**, puis sélectionnez **OK**.
    1. Non : **SC900-LogAnalytics-workspace**.
    1. Région : **USA Est** (une autre région par défaut peut être sélectionnée en fonction de votre emplacement).
    1. Sélectionnez **Vérifier + Créer** (aucune étiquette n’est configurée).
    1. Vérifiez les informations saisies, puis sélectionnez **Créer**.
    1. Il peut s’écouler une minute ou deux avant que le nouvel espace de travail ne soit affiché. Si vous ne le voyez toujours pas, sélectionnez **Actualiser**, puis **Ajouter**.

1. Une fois le nouvel espace de travail ajouté, la page Microsoft Sentinel | Actualités et guides s’affiche, indiquant que l’essai gratuit de Microsoft Sentinel est activé.  Cliquez sur **OK**.

### Révision

Dans cette configuration, vous avez activé la fonction de journal d’audit dans votre locataire Microsoft 365 et vous avez également vérifié qu’une machine virtuelle était préconfigurée dans votre environnement Azure Cloud Slice. Vous avez également préparé votre environnement Defender pour le cloud et Microsoft Sentinel.
