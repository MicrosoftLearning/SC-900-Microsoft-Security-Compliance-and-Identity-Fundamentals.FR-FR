---
ms.openlocfilehash: 8d58cd38338d81136cf0b9b474137354269507e6
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892387"
---
<a name="---"></a><!---
---
Démonstration : Titre : « Microsoft Sentinel » Parcours d’apprentissage/Module/Titre : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft ; Module 3 : Décrire les fonctionnalités de sécurité de Microsoft Sentinel ; Unité 3 : Décrire la façon dont Microsoft Sentinel fournit une gestion des menaces intégrée »
---
--->

# <a name="demo-microsoft-sentinel"></a>Démonstration : Microsoft Sentinel

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft
- Module : Décrire les fonctionnalités de sécurité de Microsoft Sentinel
- Unité : Décrire la façon dont Microsoft Sentinel fournit une gestion des menaces intégrée

## <a name="demo-scenario"></a>Scénario de la démonstration

Lors de cette démonstration, vous présenterez le processus de création d’une instance Microsoft Sentinel.  Vous définirez également les autorisations pour assurer l’accès aux ressources qui vont être déployées pour prendre en charge Microsoft Sentinel.  Une fois cette configuration de base effectuée, vous allez suivre les étapes de connexion de Microsoft Sentinel à vos sources de données et de création d’un classeur pour surveiller et visualiser vos données.  Enfin, vous allez afficher certaines des autres options disponibles, notamment l’analytique intégrée pour être informé de tout ce qui est suspect, la fonctionnalité d’automatisation, etc.

### <a name="pre-demo-setup--create-an-microsoft-sentinel-instance"></a>Configuration avant la démonstration :  Créer une instance Microsoft Sentinel

1. Ouvrez l’onglet du navigateur intitulé **Accueil-Microsoft Azure**.  Si vous avez fermé l’onglet, ouvrez une page du navigateur et saisissez portal.azure.com dans la barre d’adresse. Ensuite, reconnectez-vous.

1. Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **Sentinel** puis sélectionnez **Microsoft Sentinel** à partir des résultats de la recherche.

1. Dans la page Microsoft Sentinel, sélectionnez **Créer Microsoft Sentinel**.

1. Dans la page Ajouter Microsoft Sentinel à un espace de travail, sélectionnez **Créer un espace de travail**.

1. À partir de l’onglet de base de l’espace de travail Créer un journal d’analyses, saisissez les informations suivantes :
    1. Abonnement :  **Pass Azure - Parrainage**
    1. Groupe de ressources : sélectionnez **Créer un nouveau**, puis saisissez le nom **SC900-Sentinel-RG** et sélectionnez **OK**.
    1. Nom : **SC900-LogAnalytics-workspace**.
    1. Région : **USA Est** (une autre région par défaut peut être sélectionnée en fonction de votre emplacement)
    1. Sélectionnez **Suivant : Balises >**

1. Pour les balises, vous pouvez laissez ce champ vide, puis sélectionnez **Examiner et créer**.

1. Vérifiez les informations que vous avez saisies, puis sélectionnez **Créer**.

1. Cela peut prendre une ou deux minutes avant que l’espace de travail n’apparaisse. Si vous ne le voyez toujours pas, sélectionnez **Actualiser**, puis **Ajouter**.

1. Une fois le nouvel espace de travail ajouté, la page Microsoft Sentinel | Actualités et guides s’affiche.  Notez les trois étapes indiquées sur la page Mise en route.

1. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.

### <a name="demo-part-2"></a>Partie 2 de la démonstration

Avec la création de l’instance Microsoft Sentinel, vous voudrez vous assurer que vous avez les accès nécessaires aux ressources qui sont déployées pour prendre en charge Microsoft Sentinel.  

1. Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **groupes de ressources** puis sélectionnez **Groupes de ressources** à partir des résultats de la echerche. Assigner le rôle pour le niveau de groupe de ressources garantira que le rôle s’applique à toutes les ressources qui sont déployées pour prendre en charge Microsoft Sentinel.

1. Depuis la page des groupes de ressources, sélectionnez le groupe de ressources que vous avez créé avec Microsoft Sentinel, **SC900-Sentinel-RG**.

1. Depuis la page SC900-Sentinel-RG, sélectionnez **Contrôle d’accès (IAM)** dans le volet de navigation à gauche.

1. Depuis la page Contrôle d’accès, sélectionnez **Afficher mon accès**.  En tant qu’administrateur MOD, le rôle actuel est Administrateur de service.  Cela vous accorde les autorisations nécessaires, mais à des fins de démonstration, vous pouvez afficher les rôles spécifiques à Sentinel.  Fermez la fenêtre des attributions d’administrateur MOD en cliquant sur le **X** en haut à droite de la fenêtre.

    1. Depuis la page Contrôle d’accès, sélectionnez **+Ajouter**, puis **Ajouter une attribution de rôle**.

    1. La fenêtre d’attribution de rôle s’ouvre.  Dans la barre de recherche, saisissez **Microsoft Sentinel** pour afficher les quatre rôles associés à Microsoft Sentinel.
    1. Dans l’un des rôles répertoriés, sélectionnez **afficher** pour afficher les détails de ce rôle.  Nous recommandons d’attribuer le privilège minimum nécessaire pour ce rôle.  

    1. Fermez la fenêtre en cliquant sur le **X** en haut à droite de la fenêtre.

1. Dans la page de contrôle d’accès, fermez la fenêtre en sélectionnant **X** en haut à droite de la fenêtre.

### <a name="demo-part-3"></a>Partie 3 de la démonstration

Dans cette partie de la démonstration, vous expliquerez le processus pour connecter Microsoft Sentinel à votre source de données pour commencer à collecter des données.

1. Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **Sentinel** puis sélectionnez **Microsoft Sentinel** à partir des résultats de la recherche.

1. Depuis la page Microsoft Sentinel, sélectionnez l’espace de travail que vous avez créé avec l’instance de Microsoft Sentinel, **SC900-LogAnalytics-workspace**.

1. La première étape avec Microsoft Sentinel consiste à pouvoir collecter des données. Dans le volet de navigation à gauche, sélectionnez **Connecteurs de données**, qui se trouve sous configuration.

1. Depuis la page Connecteurs de données, sur la page principale, faites défiler vers le bas pour afficher la liste étendue des connecteurs disponibles. Dans la zone de recherche de la page des connecteurs de données, saisissez **Office 365** puis, dans la liste, sélectionnez **Office 365**.

1. La fenêtre du connecteur Office 365 s’ouvre.  Sélectionnez **Ouvrir la page du connecteur**.

1. Dans la page du connecteur Office 365, passez en revue la description sur le côté gauche de la fenêtre.

1. L’onglet des instructions dans la fenêtre principale fournit les prérequis pour l’intégration de Microsoft Sentinel à Office 365, qui doivent tous avoir une coche verte.   Sous la configuration, sélectionnez **Exchange** et **SharePoint** puis Appliquer les modifications.  Vous verrez presque immédiatement l’état connecté sur le côté gauche de la fenêtre.

1. Fermez la fenêtre en sélectionnant **X** dans le coin supérieur droit de la fenêtre pour revenir à la page des connecteurs de données.

1. Le haut de la page Connecteurs de données doit afficher 1 connecté, afin de refléter le fait que vous êtes connecté à Office 365. Si cela ne s’affiche pas, sélectionnez **Actualiser**. La mise à jour de cette page peut prendre quelques minutes.

1. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.

### <a name="demo-part-4"></a>Partie 4 de la démonstration

Dans cette partie de la démonstration, vous allez parcourir le processus de configuration d’un classeur pour Office 365, pour visualiser et surveiller vos données.

1. Dans le volet de navigation à gauche, sélectionnez **Classeurs**.

1. Dans la zone de recherche, saisissez Office 365, puis sélectionnez **Office 365**.

1. Dans la fenêtre qui s’ouvre sur le côté droit de l’écran, passez en revue la description, puis sélectionnez **Enregistrer** en bas de l’écran, puis sélectionnez **OK** pour enregistrer le classeur à l’emplacement par défaut.  À présent, sélectionnez **Afficher le classeur enregistré**.

1. La page Classeurs Office 365 s’ouvre.  Sélectionnez la flèche déroulante en regard de **Opérations : annuler**, puis sélectionnez **Tout**.  Sélectionnez maintenant la flèche déroulante en regard de **Utilisateurs : requête en attente** et sélectionnez **Tout**.  Sélectionnez **l’icône Enregistrer (disque)** . Fermez la fenêtre en cliquant sur le **X** en haut à droite de la fenêtre. L’affichage des données dans le classeur peut prendre quelques minutes. Vous reviendrez donc aux classeurs plus tard.

1. En haut à gauche de la page Classeurs, au-dessus de Classeurs, sélectionnez **Microsoft Sentinel**. Cette opération vous renvoie à la page Vue d’ensemble.

### <a name="demo-part-5"></a>Partie 5 de la démonstration

Dans cette partie de la démonstration, vous allez afficher certaines des options disponibles dans Sentinel.

1. Dans le volet de navigation gauche, sélectionnez **Hunting** (Repérage).  Sous l’onglet **requêtes**, qui est sélectionné (souligné), sélectionnez une requête dans la liste.  Une fois qu’une requête est sélectionnée, notez les informations fournies sur cette requête, y compris le code de la requête, ainsi que l’option permettant d’exécuter la requête et d’afficher les résultats.  Ne sélectionnez rien.

1. Dans le volet de navigation de gauche, sélectionnez **MITRE ATT&CK**.  MITRE ATT&CK est un base de connaissances accessible publiquement regroupant les tactiques et les techniques couramment utilisées par les attaquants. Avec Microsoft Sentinel vous pouvez afficher les détections déjà actives dans votre espace de travail, et celles que vous pouvez configurer, afin de comprendre la couverture de sécurité de votre organisation, en fonction des tactiques et des techniques issues du framework MITRE ATT&CK®.  Sélectionnez une cellule dans la matrice et notez les informations disponibles sur le côté droit de l’écran.  

1. Dans le volet de navigation situé à gauche, sélectionnez **Communauté**. Les analystes de sécurité Microsoft créent et ajoutent constamment de nouveaux workbooks, de nouveaux playbooks, de nouvelles requêtes de chasse, entre autres, et les publient dans la communauté pour vous permettre de les utiliser dans votre environnement. Vous pouvez télécharger l’exemple de contenu à partir du dépôt GitHub de la communauté privée pour créer des classeurs, requêtes de recherche, notebooks et playbooks personnalisés pour Microsoft Sentinel.  Sélectionnez **Intégrer le contenu de la communauté**.  Un nouvel onglet dans le référentiel GitHub s’ouvre où vous pouvez télécharger du contenu pour activer vos scénarios.  Revenez à l’onglet Azure dans votre navigateur.

1. Dans le volet de navigation à gauche, sélectionnez **Analyse**.  Sélectionnez le premier élément dans la liste **Détection avancée des attaques multiphases**.  Notez les informations détaillées.  Microsoft Sentinel utilise Fusion, un moteur de corrélation basé sur des algorithmes évolutifs d’apprentissage automatique pour détecter automatiquement des attaques multiphases (également appelées menaces persistantes avancées) en identifiant des combinaisons de comportements anormaux et d’activités suspectes observés à différents stades de la chaîne de destruction. Sur la base de ces découvertes, Microsoft Sentinel génère des incidents qui seraient autrement difficiles à intercepter.

1. Dans le volet de navigation à gauche, sélectionnez **Automatisation**.  Ici, vous pouvez créer simplement des règles d’automatisation, procéder à l’intégration à des playbooks existants ou créer de nouveaux playbooks.  Sélectionnez **+ Créer**, puis **Règle d’automatisation**.  Notez la fenêtre qui s’ouvre sur le côté droit de l’écran et les options disponibles pour créer des conditions et des actions.  Sélectionnez **Annuler** en bas de l’écran.

1. Dans le volet de navigation à gauche, sélectionnez **Classeurs**. Depuis la page Classeurs, sélectionnez l’onglet **Mes classeurs** qui se trouve au-dessus de la barre de recherche.  Le classeur que vous avez enregistré plus tôt est répertorié et disponible pour que vous puissiez visualiser et contrôler vos données.  Sélectionnez **Office 365** puis, dans la fenêtre qui s’ouvre sur le côté droit de l’écran, sélectionnez **Afficher le classeur enregistré**.  Notez les visualisations liées à vos charges de travail Office 365.  

1. Fermez la fenêtre en cliquant sur le **X** en haut à droite de la fenêtre.

1. Dans le coin supérieur gauche de la fenêtre, juste en dessous de la barre bleue, sélectionnez **Accueil** pour revenir à la page d’accueil du portail Azure.

### <a name="post-course-delivery-tear-down"></a>Opérations de suppression après le cours

Microsoft Sentinel est facturé en fonction du volume de données ingérées pour l’analyse dans Microsoft Sentinel. Bien que la quantité de données ingérées dans le cadre de cette démonstration soit minime, il est recommandé de supprimer le groupe de ressources Microsoft Sentinel quand vous avez terminé le cours.

1. Depuis la page Microsoft Sentinel, en haut à gauche, où il est indiqué Microsoft Sentinel, sélectionnez **Tous les services**.

2. Dans la barre de services de filtrage, saisissez groupes de ressources, puis à partir de la liste, sélectionnez **Groupes de ressources**.

3. Sur la page des groupes de ressources, sélectionnez celui que vous avez créé avec Microsoft Sentinel, **SC900-ResourceGroup**.

4. En haut au centre de la page, sélectionnez **Supprimer le groupe de ressources**.  Passez en revue l’avertissement.  Entrez le nom du groupe de ressources, **SC900-ResourceGroup**, puis sélectionnez **Supprimer** en bas de la page.  La suppression du groupe de ressources prend plusieurs minutes.

5. Une fois que vous avez vérifié que le groupe de ressources est bien supprimé, fermez la page de navigation.

### <a name="review"></a>Révision

Dans cette démonstration, vous avez parcouru les étapes de connexion de Microsoft Sentinel à des sources de données, vous avez configuré un classeur et parcouru plusieurs options disponibles dans Microsoft Sentinel.
