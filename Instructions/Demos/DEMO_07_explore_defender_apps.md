---
Demo:
    title: 'Mirosoft Defender for Cloud Apps'
    module : 'Module 3, leçon 4 : Décrire les fonctionnalités des solutions de sécurité Microsoft : Décrire la protection contre les menaces avec Microsoft 365 Defender'
---


# Démo : Microsoft Defender for Cloud Apps

### Scénario de la démonstration
Dans cette démo, vous allez découvrir les possibilités offertes par Microsoft Defender for Cloud Apps.  Vous guiderez le participant à travers les informations disponibles sur le tableau de bord de Cloud Discovery et vous lui montrerez les fonctionnalités disponibles pour examiner les résultats et contrôler l’impact sur votre organisation par le biais de stratégies.  Remarque :  Une organisation doit disposer d’une licence pour pouvoir utiliser Microsoft Defender for Cloud Apps, un service d’abonnement basé sur l’utilisateur.  

#### Partie 1 de la démonstration : Découvrez Cloud Discovery.

1. Ouvrez Microsoft Edge. Saisissez **admin.microsoft.com** dans la barre d’adresse.  Vous devriez déjà être connecté en tant qu’administrateur.  Si ce n’est pas le cas, connectez-vous à l’aide de vos informations d’identification d’administrateur.

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.  Parlez du fait que l’on peut accéder aux différents centres d’administration Microsoft 365 à partir d’ici.

1. Sous les centres d’administration, sélectionnez **Sécurité**.  Une nouvelle page de navigation s’ouvre sur la page d’accueil du portail Microsoft 365 Defender.  

1. Si c’est la première fois que vous vous rendez sur le portail Microsoft 365 Defender, il se peut qu’une fenêtre contextuelle s’ouvre et vous propose de faire le tour du portail.  Fermez-la.

1. En bas du volet de navigation gauche de la page Microsoft 365 Defender, sélectionnez **Autres ressources**.

1. Sur la carte **Microsoft Defender for Cloud Apps**, sélectionnez **Ouvrir**.  Une nouvelle page de navigation s’ouvre sur le tableau de bord de la sécurité des applications cloud.  Notez les cartes d’informations disponibles.  Il est possible que vous ne voyiez pas d’informations sur les cartes, car il s’agit d’un environnement locataire de labo préconfiguré qui n’a pas été utilisé de manière active.  

1. Dans le volet de navigation de gauche, sélectionnez **Découvrir**, puis, dans la liste déroulante, sélectionnez **Tableau de bord de Cloud Discovery**.  Le tableau de bord inclut une vue d’ensemble des applications découvertes, des catégories d’application, des niveaux de risque, etc.  

    1. En haut de la page de Cloud Discovery, sélectionnez l’onglet **Applications découvertes**.  La fenêtre des applications découvertes fournit un affichage plus détaillé des applications découvertes, y compris le score de risque, le nombre d’utilisateurs, etc.

        1. À partir de n’importe quel élément de la liste, sélectionnez les **points de suspension** dans la colonne d’actions du tableau.  Notez les différentes options disponibles, y compris la possibilité d’identifier une application comme approuvée et non approuvée.  Sélectionnez à nouveau les points de suspension pour fermer la boîte d’actions.

        1. Sélectionner un élément de ligne spécifique ouvre une page de détails pour cette application spécifique.  Sélectionnez un élément dans la liste.  Pour l’élément sélectionné, parcourez chaque onglet en haut de la page de détails :  **Usage**, **Info**,**Adresses IP**, **Utilisateurs** et **Alertes**. Lorsque vous avez fini de découvrir la page de détails, retournez aux applications découvertes en sélectionnant **Applications découvertes** dans le volet de navigation gauche.

    1. En haut de la page, sélectionnez l’onglet **Adresses IP** (cela équivaut à sélectionner Adresses IP dans le volet de navigation de gauche).  Vous trouverez ici des données, y compris le nombre de transactions, la quantité de trafic et les quantités de chargements par adresses IP.  Notez que vous pouvez également filtrer par adresse IP spécifique ou exporter les données pour de plus amples analyses.

    1. En haut de la page (ou depuis le volet de navigation de gauche), sélectionnez **Utilisateurs**.  Il s’agit des mêmes informations que quand vous sélectionnez Adresses IP, mais les informations sont cette fois classées par utilisateur.  Ici aussi vous filtrez par utilisateur spécifique et exportez les données pour de plus amples analyses.

1. Les informations fournies dans ces onglets se basent soit sur des rapports instantanés à partir des journaux de trafic que vous avez chargé manuellement depuis vos pare-feux et proxys, soit sur des rapports continus qui analysent tous les journaux qui sont transférés depuis votre réseau à l’aide de la sécurité des applications cloud.  Pour configurer ces options, sélectionnez les **points de suspension** en haut à droite de la page.

    1. Sélectionnez la première option, **Créer un rapport instantané Cloud Discovery**. Vous saisissez ici les détails demandés et chargez les journaux de trafic afin de générer et charger un rapport.  Sélectionnez **Annuler**.  Les données que vous voyez pour votre locataire de labo proviennent d’un rapport instantané. Vous pouvez voir cette information en haut à droite de l’écran.

    1. Afin d’afficher l’option pour les rapports continus, sélectionnez les **points de suspension** en haut à droite de la page et, dans la liste déroulante, sélectionnez **Configurer le chargement automatique**.  Il n’y a pas de sources de données connectées, mais c’est ici que vous en ajouteriez une. Sélectionnez la flèche déroulante vers le bas **Sélectionner une appliance** pour voir les types d’appliances que vous pouvez connecter en tant que source de données.  Sélectionnez **Annuler** pour quitter la page.

1. Un autre point à souligner est que vous pouvez vous connecter aux applications directement en configurant des connecteurs d’application qui vous fourniront une visibilité et un contrôle plus grand sur vos applications cloud. En haut à gauche de l’écran, sélectionnez **l’icône représentant un engrenage** et, dans la liste déroulante, sélectionnez **Connecteurs d’application**.  

    1. Sur la page des applications connectées, vous devriez voir Office 365 dans la liste avec un statut connecté.  Si Office 365 affiche une erreur de connexion, il est fortement probable qu’Audit ne soit pas activé.

    1. Sélectionnez **+Connecter une application** et, depuis la liste déroulante, sélectionnez **Microsoft Azure**.  Depuis la fenêtre contextuelle Microsoft Azure, sélectionnez **Connecter Microsoft Azure**.  Vous verrez le statut connecté ainsi que les informations quand vous analysez les utilisateurs, les données et les activités.  Sélectionnez le bouton **Fermer**.

1. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.

#### Partie 2 de la démonstration : Découvrez les manières d’examiner les activités enregistrées.

1. Dans le volet de navigation de gauche, sous **Examiner**, sélectionnez **Journal d’activité**.  C’est ici que vous verrez toutes les activités de vos applications connectées.   Comme vous avez déjà connecté le connecteur Office 365, vous devriez voir quelques données. Après que vous avez connecté la sécurité des applications cloud à une application à l’aide du connecteur d’application, celle-ci analyse toutes les activités qui se sont produites (la période d’analyse rétroactive diffère selon les applications), puis est constamment mise à jour avec de nouvelles activités.  

1. Sélectionnez un élément pour lequel vous souhaitez afficher plus d’informations détaillées. Remarquez l’option en haut de la page pour ajouter une nouvelle stratégie à partir de la recherche ou exporter les données pour de plus amples analyses.  Sélectionnez **+Nouvelle stratégie à partir de la recherche**.  Notez comment vous pouvez créer une stratégie basée sur un modèle, sélectionner une gravité et catégorie de stratégie, créer des filtres pour une stratégie, créer des alertes et même envoyer des alertes à Power Automate.  Sélectionnez **Annuler** pour quitter la fenêtre de création de stratégie.

1. Dans le volet de navigation de gauche, sélectionnez et découvrez les options de **Fichiers** et notez les options permettant de filtrer les données, de créer une stratégie de fichier et d’exporter les données.  Sélectionnez et découvrez l’option **utilisateur et comptes**.  Notez les options pour filtrer les données et les exporter.

1. Dans le volet de navigation de gauche, sélectionnez Configuration de la sécurité. Cette page vous fournit des évaluations sur la configuration de la sécurité pour vos comptes Azure, Amazon Web Services (AWS) et Google Cloud Platform (GCP).

1. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.


#### Partie 3 de la démonstration : Dans cette tâche, vous découvrirez les pages de stratégies et d’alertes dans Microsoft Defender for Cloud Apps.

1. Dans le volet de navigation de gauche, sous Contrôle, sélectionnez **Stratégies**.  Les stratégies répertoriées fournissent des informations sur le nombre d’alertes générées par la gravité de la stratégie, etc. Sélectionner un élément de ligne fournit des informations détaillées à propos de la stratégie. À partir de la liste, sélectionnez l’élément **Connexion risquée**.  

1. Dans le volet de navigation de gauche, sélectionnez **Alertes**.  Si des alertes sont présentes, sélectionnez un élément de la liste d’alertes. Passez en revue les informations fournies.  En haut à droite de la fenêtre, sélectionnez **Fermer l’alerte** afin d’afficher les options pour fermer l’alerte.  

1. Fermez la fenêtre du navigateur.

#### Révision
Dans cette démo, vous avez présenté les possibilités offertes par Microsoft Defender for Cloud Apps.  Vous avez présenté les informations disponibles sur le tableau de bord de Cloud Discovery ainsi que les fonctionnalités disponibles pour examiner les résultats et contrôler l’impact sur votre organisation par le biais de stratégies.