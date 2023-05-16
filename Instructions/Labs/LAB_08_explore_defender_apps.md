---
lab:
  title: 'Explorer Microsoft Defender for Cloud Apps'
  module: 'Module 4 : Décrire les fonctionnalités de protection contre les menaces de Microsoft 365'
---


# <a name="lab-explore-microsoft-defender-for-cloud-apps"></a>Labo : Explorer Microsoft Defender pour les applications cloud

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft
- Module : Décrire les fonctionnalités de protection contre les menaces de Microsoft 365
- Unité : Décrire Microsoft Defender for Cloud Apps

## <a name="lab-scenario"></a>Scénario du labo

Dans ce labo, vous allez explorer les fonctionnalités de Microsoft Defender for Cloud Apps.  Vous présenterez les informations contenues dans le tableau de bord Cloud Discovery, le catalogue d’applications cloud, les fonctionnalités disponibles pour investiguer les résultats ainsi que les façons de contrôler l’impact sur votre organisation au moyen de stratégies. Remarque : Une organisation doit disposer d’une licence pour utiliser Microsoft Defender for Cloud Apps, qui est un service par abonnement basé sur l’utilisateur.

**Durée estimée** : 15-20 minutes

### <a name="task-1---explore-cloud-discovery"></a>Tâche 1 - Explorer Cloud Discovery

Découvrez Cloud Discovery.

1. Ouvrez Microsoft Edge. Dans la barre d’adresse, entrez **admin.microsoft.com**.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**. Vous accédez ainsi à la page du Centre d’administration Microsoft 365.

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous les centres d’administration, sélectionnez **Sécurité**.  Une nouvelle page de navigation s’ouvre sur la page d’accueil du portail Microsoft 365 Defender.  

1. Si c’est la première fois que vous vous rendez sur le portail Microsoft 365 Defender, il se peut qu’une fenêtre contextuelle s’ouvre et vous propose de faire le tour du portail.  Fermez-la.

1. Dans le panneau de navigation de gauche, sélectionnez **Applications cloud** pour développer la liste, puis sélectionnez **Cloud Discovery**. Vous accédez alors à la vue Tableau de bord.  Notez les informations disponibles dans le tableau de bord. À partir de la vue du tableau de bord, vous pouvez sélectionner différents onglets en haut de la page.  

1. Sélectionnez **Applications découvertes**. La fenêtre des applications découvertes fournit un affichage plus détaillé des applications découvertes, y compris le score de risque, le nombre d’utilisateurs, etc.
    1. À partir de n’importe quel élément de la liste, sélectionnez les **points de suspension** dans la colonne d’actions du tableau.  Notez les différentes options disponibles, y compris la possibilité d’identifier une application comme approuvée et non approuvée.  Sélectionnez à nouveau les **points de suspension** pour fermer la zone d’actions.
    1. Sélectionner un élément de ligne spécifique ouvre une page de détails pour cette application spécifique.  Sélectionnez un élément dans la liste et passez en revue les informations disponibles dans la page de présentation.  Sélectionnez l’onglet **Utilisation de l’application cloud** pour l’élément sélectionné afin d’afficher des informations plus détaillées : **Utilisation**, **Utilisateurs**, **Adresses IP**, **Alertes**, etc. Quand vous avez terminé d’explorer la page des détails, sélectionnez **Cloud Discovery** dans la barre de navigation en haut de la page pour revenir à la page des applications découvertes.  Si vous sélectionnez Cloud Discovery dans le panneau de navigation de gauche, vous revenez à la vue du tableau de bord.
    1. En haut de la page, sélectionnez l’onglet **Adresses IP**. Ici, vous trouverez des données comme le nombre de transactions, la quantité de trafic et les quantités de données chargées par adresse IP.  Notez que vous pouvez également filtrer par adresse IP spécifique ou exporter les données pour de plus amples analyses.
    1. En haut de la page, sélectionnez **Utilisateurs**.  Il s’agit des mêmes informations que celles obtenues quand vous sélectionnez Adresses IP, mais elles sont cette fois classées par utilisateur.  Ici aussi vous filtrez par utilisateur spécifique et exportez les données pour de plus amples analyses.

1. Les informations fournies dans la page Cloud Discovery et les onglets associés sont basées soit sur des rapports instantanés issus de journaux de trafic que vous chargez manuellement à partir de vos pare-feux et proxys, soit sur des rapports continus qui analysent tous les journaux transférés à partir de votre réseau avec Cloud App Security.  Pour voir où ces options sont configurées, sélectionnez **Actions** en haut à droite de la page.
    1. Sélectionnez la première option, **Créer un rapport d’instantané Cloud Discovery**, puis sélectionnez **Suivant**. Vous saisissez ici les détails demandés et chargez les journaux de trafic afin de générer et charger un rapport.  Sélectionnez **Quitter** et, si vous êtes invité à confirmer, sélectionnez à nouveau **Quitter**.  Les données que vous voyez pour votre locataire de labo proviennent d’un rapport instantané. Vous pouvez voir cette information en haut de la fenêtre Cloud Discovery.
    1. Pour voir l’option pour les rapports continus, sélectionnez **Actions** en haut à droite de la page, puis **Configurer le chargement automatique** dans la liste déroulante.  Il n’y a pas de sources de données connectées, mais c’est ici que vous en ajouteriez une. Sélectionnez **Ajouter une source de données**, puis sélectionnez la flèche déroulante dans le champ **Sélectionner une appliance** pour voir les types d’appliances que vous pouvez connecter en tant que source de données.  Sélectionnez **Annuler** pour quitter. 
    1. Dans le panneau de navigation de gauche, sélectionnez **Cloud Discovery** pour revenir à la page Cloud Discovery.

1. Vous pouvez vous connecter directement aux applications en configurant des connecteurs d’application qui vous fourniront plus de visibilité et de contrôle sur vos applications cloud. En haut à droite de l’écran, sélectionnez **Actions**, puis **Paramètres Cloud Discovery**.  Sur le côté gauche de l’écran, sous Applications connectées, sélectionnez **Connecteurs d’application**.  

    1. Dans la page Applications connectées, sélectionnez *Office 365** dans la liste pour voir des informations détaillées. Si Office 365 affiche une erreur de connexion, c’est probablement parce que l’audit n’est pas activé.  Si l’audit est activé, accédez aux trois points verticaux à droite de l’élément de ligne, puis sélectionnez **Modifier les paramètres**.  Pour vous reconnecter, sélectionnez **Connecter Office 365** en bas de la page. La page doit maintenant indiquer qu’Office 365 est connecté. Sélectionnez **Terminé**.  L’état est pour l’instant accompagné d’un signe d’avertissement jaune, ce qui signifie qu’il n’y a pas d’état récent.  La mise à jour de l’état prend un certain temps. En effet, la période d’analyse rétroactive varie d’une application à l’autre et les locataires de labo peuvent rencontrer des délais plus longs qu’à l’accoutumée.
    1. Vous allez maintenant configurer un nouveau connecteur d’application.  Sélectionnez **+Connecter une application** et, depuis la liste déroulante, sélectionnez **Microsoft Azure**.  À partir de la fenêtre contextuelle Microsoft Azure, sélectionnez **Connecter Microsoft Azure**, puis **Terminé**.  Vous voyez un état connecté (si ce n’est pas le cas, actualisez le navigateur) ainsi que des informations sur l’analyse des utilisateurs, des données et des activités.  Sélectionnez **Cloud Discovery** dans le panneau de navigation le plus à gauche pour revenir au tableau de bord Cloud Discovery.

1. Laissez cette page ouverte, car vous en aurez besoin pour la tâche suivante.

### <a name="task-part-2---explore-the-cloud-app-catalog"></a>Partie 2 de la tâche - Explorer le catalogue d’applications cloud

Cloud Discovery analyse vos journaux de trafic par rapport au catalogue d’applications cloud Microsoft Defender for Cloud Apps qui contient plus de 31 000 applications cloud. Les applications sont classées et évaluées selon plus de 80 facteurs de risque afin de vous offrir une visibilité en continu de l’utilisation du cloud, du « Shadow IT » et du risque que celui-ci représente pour votre organisation.  Dans cette tâche, vous allez explorer les fonctionnalités du catalogue d’applications cloud.

1. Dans le panneau de navigation de gauche, sélectionnez **Catalogue d’applications cloud**.

1. Le catalogue d’applications cloud vous permet de choisir les applications qui répondent le mieux aux exigences de sécurité de votre organisation. Les administrateurs peuvent filtrer les applications selon plusieurs critères de base indiqués en haut de la page : application approuvée, non approuvée, sans étiquette, score de risque, facteur de risque de conformité et facteur de risque de sécurité.  Par exemple, le filtrage par facteur de risque de conformité vous permet de rechercher des normes, une certification et une conformité spécifiques auxquelles l’application peut se conformer. Par exemple, les normes HIPAA, ISO 27001, SOC 2 ou PCI-DSS. Sélectionnez **Facteur de risque de conformité** pour voir les options disponibles.  Vous pouvez déplacer les curseurs du score de risque en haut de la page pour affiner votre filtrage. Si vous déplacez le curseur, veillez à le régler sur une plage comprise entre 0 et 10.

1. Les administrateurs peuvent également rechercher des applications par catégorie.  Par exemple, dans le champ Rechercher une catégorie, entrez **Réseau social**, puis sélectionnez **Réseau social**.  Sélectionnez **Yammer** pour obtenir une vue détaillée.  Pointez votre souris sur les rubriques d’une catégorie donnée pour afficher une icône d’informations que vous pouvez sélectionner pour obtenir plus de détails sur cette rubrique.

1. Laissez cette page ouverte, car vous en aurez besoin pour la tâche suivante.

### <a name="task-3---explore-the-activity-log-and-files"></a>Tâche 3 - Explorer le journal d’activité et les fichiers

Explorez les différentes façons d’investiguer les activités enregistrées avec le journal d’activité et les fichiers.

1. Dans le volet de navigation de gauche, sélectionnez et explorez l’option **Fichiers**. Notez les options de filtrage des données par application, propriétaire, niveau d’accès, type de fichier et stratégie correspondante. Notez également l’option de création d’une stratégie à partir de la recherche et d’exportation des données.
    1. Sélectionnez **+ Nouvelle stratégie à partir de la recherche**.  Notez comment vous pouvez créer une stratégie basée sur un modèle, sélectionner une gravité et catégorie de stratégie, créer des filtres pour une stratégie, créer des alertes et même envoyer des alertes à Power Automate.  Sélectionnez **Annuler** pour quitter la fenêtre de création de stratégie, puis sélectionnez **Quitter la page**.

1. Dans le panneau de navigation de gauche, sélectionnez **Journal d’activité**. C’est ici que vous verrez toutes les activités de vos applications connectées. Toutefois, étant donné que l’exécution d’analyses rétroactives peut prendre plusieurs heures une fois l’audit activé et que les locataires du labo peuvent rencontrer des délais plus longs qu’à l’accoutumée, il se peut qu’aucune donnée ne soit listée. Notez les options de filtre disponibles et l’option de création d’une stratégie à partir de la recherche.

1. Laissez cette page ouverte, car vous en aurez besoin pour la tâche suivante.

### <a name="task-4---explore-policies"></a>Tâche 4 - Explorer les stratégies

Dans cette tâche, vous allez explorer les stratégies dans Microsoft Defender for Cloud Apps.

1. Dans le panneau de navigation de gauche, sélectionnez **Stratégies**, puis **Gestion des stratégies**.  Les stratégies répertoriées fournissent des informations sur le nombre d’alertes générées par la stratégie, la gravité, etc. La sélection de n’importe quelle rubrique fournit des informations plus détaillées sur la stratégie. À partir de la liste, sélectionnez l’élément **Connexion risquée**.

    1. Notez que vous pouvez également créer une stratégie. Sélectionnez **+ Créer une stratégie** pour voir les types de stratégies que vous pouvez créer.  Sélectionnez **Stratégie d’activité** pour voir les différentes options disponibles pour créer la stratégie.  Sélectionnez **Annuler** pour quitter la fenêtre de configuration.
    1. Notez que vous pouvez également exporter les informations de la stratégie.

1. Dans le panneau de navigation de gauche, sélectionnez **Modèles de stratégie**. Pour créer une stratégie à partir de l’un des modèles disponibles, sélectionnez le signe **+** à gauche de l’élément de ligne de modèle.  Examinez les différentes options de configuration de la stratégie.  Cliquez sur **Annuler** pour quitter la page.

1. Fermez la fenêtre du navigateur.

### <a name="review"></a>Révision

Dans ce labo, vous avez découvert les possibilités offertes par Microsoft Defender pour le cloud.  Vous avez parcouru les informations contenues dans le tableau de bord Cloud Discovery, le catalogue d’applications cloud, les fonctionnalités disponibles pour investiguer les résultats ainsi que les façons de contrôler l’impact sur votre organisation au moyen de stratégies.
