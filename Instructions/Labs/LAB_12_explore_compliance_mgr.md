---
ms.openlocfilehash: 8d3268c28c1dc2335f0554caf801abe11b6ae0d2
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892375"
---
<a name="---"></a><!---
---
Labo : Titre : « Explorer le portail de conformité Microsoft Purview et le Gestionnaire de conformité » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft ; Module 2 : Décrire les fonctionnalités de gestion de la conformité dans Microsoft Purview ; Unité 2 : Décrire le portail de conformité Microsoft Purview »
---
--->

# <a name="lab-explore-the-microsoft-purview-compliance-portal--compliance-manager"></a>Labo : Explorer le portail de conformité Microsoft Purview et le Gestionnaire de conformité

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft
- Module : Décrire les fonctionnalités de gestion de la conformité dans Microsoft Purview
- Unité : Décrire le portail de conformité Microsoft Purview

## <a name="lab-scenario"></a>Scénario du labo

Dans ce labo, vous allez explorer la page d’accueil du portail de conformité Microsoft Purview et voir comment les fonctionnalités du Gestionnaire de conformité peuvent aider les organisations à améliorer leur posture de conformité.

**Durée estimée** : 15-20 minutes

### <a name="task-1"></a>Tâche 1

Explorez la page d’accueil du portail de conformité Microsoft Purview, puis apprenez à personnaliser l’apparence de la carte et le volet de navigation.

1. Ouvrez Microsoft Edge. Saisissez **admin.microsoft.com** dans la barre d’adresse.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.

    1. Saisissez le mot de passe d’administrateur communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**. Vous accédez ainsi à la page du Centre d’administration Microsoft 365.

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous les Centres d’administration, sélectionnez **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.  
1. Sur cette page, la section réservée aux cartes vous permet de connaître d’un coup d’œil la situation de sécurité de votre organisation, les solutions disponibles pour celle-ci, etc.
1. Depuis la fenêtre principale, faites défiler vers le bas pour consulter les différentes cartes. Les cartes disponibles sur l’écran d’accueil ainsi que leur emplacement peuvent être modifiés pour s’adapter aux préférences de chaque administrateur.  
1. Survolez la barre de titre de n’importe quelle carte avec votre curseur : celle-ci devient grise.  Lorsque votre curseur se transforme en croix, vous pouvez déplacer la carte où vous le souhaitez.
1. Des points de suspension apparaissent également sur la barre de titre de chaque carte : ils vous proposeront des actions supplémentaires.  Cliquez sur les points de suspension du Catalogue de solutions et sélectionnez **Supprimer**.
1. Vous pouvez ajouter des cartes en cliquant sur **+ Ajouter des cartes**.  La fenêtre d’ajout de cartes à votre page d’accueil s’ouvre.  Survolez la carte du Catalogue des solutions affichée dans la fenêtre à l’aide de votre curseur et déplacez-la vers la zone de votre écran d’accueil à l’emplacement souhaité.
1. Dans le volet de navigation situé à gauche de la page d’accueil du portail de conformité Microsoft Purview, vous constaterez que seul le Catalogue s’affiche sous les Solutions.  Dans le volet de navigation situé à gauche, sélectionnez **...Afficher tout**.  Vous remarquerez que toutes les solutions supplémentaires apparaissent sous la section des solutions.  
1. Sélectionnez **Afficher moins** pour les masquer.
1. En tant qu’administrateur de la conformité, il peut y avoir un ensemble de solutions que vous gérez pour notre organisation et, en tant que tel, vous souhaiterez peut-être que seules les solutions indiquées dans le volet de navigation s’affichent. Pour personnaliser vos préférences, sélectionnez **Personnaliser la navigation**.  
1. À partir de la fenêtre intitulée Personnaliser votre volet de navigation, notez comment vous pouvez sélectionner les éléments que vous souhaitez voir apparaître dans le panneau de navigation et désélectionner les éléments que vous ne souhaitez pas afficher. Dans le cadre de ces labos, conservez tous les éléments sélectionnés, puis cliquez sur **Enregistrer** en bas de la fenêtre.  
1. Laissez cet onglet du navigateur ouvert.

### <a name="task-2"></a>Tâche 2

Découvrez la situation de sécurité de votre organisation par l’intermédiaire du Gestionnaire de conformité.

1. Dans le volet de navigation situé à gauche du portail de conformité Microsoft Purview, sélectionnez **Gestionnaire de conformité**.  Vous pouvez aussi sélectionnez Gestionnaire de conformité dans la barre de titre de la carte Gestionnaire de conformité.

1. Vérifiez qu’**Aperçu** est bien sélectionné (souligné) en haut de la page du Gestionnaire de conformité. Faites défiler vers le bas pour consulter l’ensemble des informations disponibles sur la page.  Les informations de cette page comprennent votre score de conformité. Il est calculé d’après les points que vous avez accumulés et ceux accumulés par la gestion de Microsoft.   Vous verrez les principales actions d’amélioration, les solutions qui influent sur votre score ainsi que le score de conformité répartis selon des catégories ou des évaluations.

1. Sélectionnez **Actions d’amélioration** en haut de la page de présentation.  Ce sont des actions qui peuvent améliorer le score de conformité de l’organisation. Notez qu’à mesure que des actions d’amélioration sont effectuées, la mise à jour des points peut prendre jusqu’à 24 heures.  Prenez note des filtres disponibles.

1. Sélectionnez **Activer la réinitialisation de mot de passe en libre-service** dans la liste des actions d’amélioration.  Chaque action d’amélioration dispose d’une section Présentation, ainsi que d’une page de détails à partir de laquelle vous pouvez sélectionner la mise en œuvre, le test, les normes et les exigences réglementaires associées, ainsi que les documents.

1. Quittez cette action d’amélioration en sélectionnant **Actions d’amélioration** dans le fil d’Ariane en haut à gauche de la page.  Vous vous retrouvez alors sur la page des actions d’amélioration.

1. Cliquez sur **Solutions** en haut de la page. Cette page vous présentera la manière dont les solutions contribuent à votre score et comment vous pouvez encore l’améliorer.

1. Cliquez sur **Évaluations** en haut de la page. Cette page affichera la base de référence de protection des données.  Il s’agit d’une évaluation par défaut fournie par Microsoft dans le Gestionnaire de conformité, destinée à la base de référence de protection des données de Microsoft 365.  Cette évaluation de la base de référence dispose d’un ensemble de contrôles pour des réglementations et des normes clés destinées à la protection et à la gouvernance des données en général. Le Gestionnaire de conformité devient plus utile à mesure que vous créez et gérez vos propres évaluations en vue de répondre aux besoins spécifiques de votre organisation.

1. Sélectionnez **Base de référence de protection des données**.  Prenez note des informations disponibles sur la barre de progression.  Vous pouvez également consulter des informations sur les contrôles, vos actions d’amélioration et les actions Microsoft.  

1. Cliquez sur **Évaluation** en haut à gauche de la page (au-dessus du fil d’Ariane, représenté par l’intitulé « Évaluation ») pour revenir à la page des évaluations.  

1. Sélectionnez **Modèles d’évaluation** en haut de la page.  Cette page répertorie les modèles disponibles. Vous pouvez créer des évaluations pour votre organisation à l’aide d’un modèle existant, ou vous pouvez en créer un nouveau.

1. Sélectionnez **ISO/IEC27001:2013** dans la liste des modèles inclus. Cliquez sur **+ Créer une évaluation** en haut à droite de la page.  Vous remarquerez que seules deux étapes se trouvent sur le côté gauche de l’écran pour créer une évaluation à partir du modèle.  Sélectionnez Annuler en bas de la page.

1. Fermez tous les onglets ouverts du navigateur.

### <a name="review"></a>Révision

Dans ce labo, vous avez exploré la page d’accueil du portail de conformité Microsoft Purview et vu comment les fonctionnalités du Gestionnaire de conformité peuvent aider les organisations à améliorer leur posture de conformité.
