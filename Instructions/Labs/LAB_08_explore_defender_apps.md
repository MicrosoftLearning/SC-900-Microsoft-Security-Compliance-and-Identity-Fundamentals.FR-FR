---
lab:
  title: 'Explorer Microsoft Defender pour les applications cloud '
  module: 'Module 3 Lesson 4: Describe the capabilities of Microsoft security solutions: Describe threat protection with Microsoft 365 Defender'
ms.openlocfilehash: c6b9e816596c74199123b21a9fcb07a5d33a725c
ms.sourcegitcommit: a69acc26ed3a09cea4a3af95719a6edc7fe2814d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2022
ms.locfileid: "146650063"
---
# <a name="lab-explore-microsoft-defender-for-cloud-apps"></a>Labo : Explorer Microsoft Defender pour les applications cloud

## <a name="lab-scenario"></a>Scénario du labo

Dans ce labo, vous allez découvrir les possibilités offertes par Microsoft Defender pour le cloud.  Vous allez parcourir les informations disponibles sur le tableau de bord de Cloud Discovery, ainsi que les possibilités offertes pour examiner les résultats et contrôler l’impact sur votre organisation par le biais de politiques.  Remarque :  Une organisation doit avoir une licence pour utiliser Microsoft Defender pour le cloud, qui est un service d’abonnement basé sur l’utilisateur.

**Durée estimée** : 15-20 minutes

### <a name="task-1"></a>Tâche 1

Découvrez Cloud Discovery.

1. Ouvrez Microsoft Edge. Saisissez **admin.microsoft.com** dans la barre d’adresse.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Saisissez le mot de passe d’administrateur communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**. Vous accédez ainsi à la page du Centre d’administration Microsoft 365.

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous les centres d’administration, sélectionnez **Sécurité**.  Une nouvelle page de navigation s’ouvre sur la page d’accueil du portail Microsoft 365 Defender.  

1. En bas du volet de navigation à gauche de la page Microsoft 365 Defender, sélectionnez **Autres ressources**.

1. Sur la carte **Applications Microsoft Defender pour le cloud**, sélectionnez **Ouvrir**.  Une nouvelle page de navigation s’ouvre sur le tableau de bord de la sécurité des applications cloud.  Notez les cartes d’informations disponibles.  Il est possible que vous ne voyiez pas d’informations sur les cartes, car il s’agit d’un environnement locataire de labo préconfiguré qui n’a pas été utilisé de manière active.  

1. Dans le volet de navigation à gauche, sélectionnez **Découvrir**, puis, à partir de la liste déroulante, sélectionnez **Tableau de bord de Cloud Discovery**.  Le tableau de bord inclut une vue d’ensemble des applications découvertes, des catégories d’application, des niveaux de risque, etc.  
    1. En haut de la page de Cloud Discovery, sélectionnez l’onglet **Applications découvertes**.  La fenêtre des applications découvertes fournit un affichage plus détaillé des applications découvertes, y compris le score de risque, le nombre d’utilisateurs, etc.
        1. À partir de n’importe quel élément de la liste, sélectionnez les **points de suspension** dans la colonne d’actions du tableau.  Notez les différentes options disponibles, y compris la possibilité d’identifier une application comme approuvée et non approuvée.  Sélectionnez à nouveau les points de suspension pour fermer la boîte d’actions.
        1. Sélectionner un élément de ligne spécifique ouvre une page de détails pour cette application spécifique.  Sélectionnez un élément dans la liste.  Pour l’élément sélectionné, parcourez chaque onglet en haut de la page de détails :  **Usage**, **Info**, **Adresses IP**, **Utilisateurs** et **Alertes**. Lorsque vous avez fini de découvrir la page de détails, retournez aux applications découvertes en sélectionnant **Applications découvertes** depuis le volet de navigation à gauche.
    1. En haut de la page, sélectionnez l’onglet **Adresses IP** (cela revient au même que de sélectionner Adresses IP depuis le volet de navigation à gauche).  Vous trouverez ici des données, y compris le nombre de transactions, la quantité de trafic et les quantités de chargements par adresses IP.  Notez que vous pouvez également filtrer par adresse IP spécifique ou exporter les données pour de plus amples analyses.
    1. En haut de la page (ou depuis le volet de navigation à gauche), sélectionnez **Utilisateurs**.  Il s’agit des mêmes informations que quand vous sélectionnez Adresses IP, mais les informations sont cette fois classées par utilisateur.  Ici aussi vous filtrez par utilisateur spécifique et exportez les données pour de plus amples analyses.

1. Les informations fournies dans ces onglets se basent soit sur des rapports instantanés à partir des journaux de trafic que vous avez chargé manuellement depuis vos pare-feux et proxys, soit sur des rapports continus qui analysent tous les journaux qui sont transférés depuis votre réseau à l’aide de la sécurité des applications cloud.  Pour configurer ces options, sélectionnez les **points de suspension** verticaux en haut à droite de la page.
    1. Sélectionnez la première option, **Créer un rapport instantané Cloud Discovery**. Vous saisissez ici les détails demandés et chargez les journaux de trafic afin de générer et charger un rapport.  Sélectionnez **Quitter**.  Les données que vous voyez pour votre locataire de labo proviennent d’un rapport instantané. Vous pouvez voir cette information en haut à droite de l’écran.
    1. Afin d’afficher l’option pour les rapports continus, sélectionnez les **points de suspension** en haut à droite de la page et, dans la liste déroulante, sélectionnez **Configurer le chargement automatique**.  Il n’y a pas de sources de données connectées, mais c’est ici que vous en ajouteriez une. Sélectionnez **Ajouter une source de données**, puis dans la fenêtre Ajouter une source de données, sélectionnez la flèche déroulante dans le champ Source pour afficher les types d’appliances que vous pouvez connecter en tant que source de données.  Sélectionnez **Annuler** pour quitter la page.

1. Un autre point à souligner est que vous pouvez vous connecter aux applications directement en configurant des connecteurs d’application qui vous fourniront une visibilité et un contrôle plus grand sur vos applications cloud. En haut à gauche de l’écran, sélectionnez **l’icône représentant un engrenage** et, dans la liste déroulante, sélectionnez **Connecteurs d’application**.  
    1. Sur la page des applications connectées, vous devriez voir Office 365 dans la liste avec un statut connecté.  Si Office 365 affiche une erreur de connexion, il est fortement probable qu’Audit ne soit pas activé.
    1. Sélectionnez **+Connecter une application** et, depuis la liste déroulante, sélectionnez **Microsoft Azure**.  Depuis la fenêtre contextuelle Microsoft Azure, sélectionnez **Connecter Microsoft Azure**.  Vous verrez le statut connecté ainsi que les informations quand vous analysez les utilisateurs, les données et les activités.  Sélectionnez le bouton **Fermer**.

1. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.

### <a name="task-2"></a>Tâche 2

Découvrez les manières d’examiner les activités enregistrées.

1. Dans le volet de navigation à gauche, sous Examiner, sélectionnez **Journal d’activité**.  C’est ici que vous verrez toutes les activités de vos applications connectées.   Comme vous avez déjà connecté le connecteur Office 365, vous devriez voir quelques données. Une fois connecté à une application à l’aide du connecteur d’applications, Cloud App Security analyse toutes les activités passées (la période d’analyse rétroactive varie par application). Cloud App Security est ensuite mis à jour en continu avec les nouvelles activités.  

1. Sélectionnez la colonne Activité pour tout élément pour afficher des informations plus détaillées. À l’extrême droite de l’élément sélectionné, sélectionnez les **ellipses** verticales.  Notez les différentes options.  Sélectionnez la colonne Activité pour le même élément afin de réduire la vue détaillée.

1. Remarquez l’option en haut de la page pour ajouter une nouvelle stratégie à partir de la recherche ou exporter les données pour de plus amples analyses.  Sélectionnez **+Nouvelle stratégie à partir de la recherche**.  Notez comment vous pouvez créer une stratégie basée sur un modèle, sélectionner une gravité et catégorie de stratégie, créer des filtres pour une stratégie, créer des alertes et même envoyer des alertes à Power Automate.  Sélectionnez **Annuler** pour quitter la fenêtre de création de stratégie.

1. À partir du volet de navigation à gauche, sélectionnez et découvrez les options de **Fichiers** et notez les options pour filtrer les données, créer une stratégie de fichier et exporter les données.  

1. Dans le volet de navigation gauche, sélectionnez et explorez l’option **Utilisateurs et comptes**.  Notez les options pour filtrer les données et les exporter.

1. Dans le volet de navigation à gauche, sélectionnez **Configuration de la sécurité**. Cette page vous fournit des évaluations sur la configuration de la sécurité pour vos comptes Azure, Amazon Web Services (AWS) et Google Cloud Platform (GCP).

1. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.

### <a name="task-3"></a>Tâche 3

Lors de cette tâche, vous découvrirez les pages de stratégies et d’alertes dans Microsoft Defender pour le cloud.

1. Dans le volet de navigation gauche, sélectionnez la touche de direction bas en regard de **Contrôle**, puis choisissez **Stratégies**.  Les stratégies répertoriées fournissent des informations sur le nombre d’alertes générées par la stratégie, la gravité, etc. La sélection de n’importe quelle ligne, par exemple **Connexion risquée**, offre la possibilité de modifier la stratégie. Sélectionnez **Annuler** en bas de la page.

1. Dans le volet de navigation à gauche, sélectionnez **Alertes**.  Si des alertes sont présentes, sélectionnez un élément de la liste d’alertes. Examinez les informations fournies.  En haut à droite de la fenêtre, sélectionnez **Fermer l’alerte** afin d’afficher les options pour fermer l’alerte.  

1. Fermez tous les onglets ouverts du navigateur.

### <a name="review"></a>Révision

Dans ce labo, vous avez découvert les possibilités offertes par Microsoft Defender pour le cloud.  Vous avez parcouru les informations disponibles sur le tableau de bord de Cloud Discovery, ainsi que les possibilités offertes pour examiner les résultats et contrôler l’impact sur votre organisation par le biais de politiques.
