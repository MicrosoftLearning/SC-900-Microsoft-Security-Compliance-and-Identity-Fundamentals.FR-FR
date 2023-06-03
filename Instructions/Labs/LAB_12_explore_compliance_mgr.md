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

Dans ce labo, vous explorez la page d’accueil du portail de conformité Microsoft Purview et comment les fonctionnalités du Gestionnaire de conformité peuvent aider les organisations à améliorer leur posture de conformité.

**Durée estimée** : 30-45 minutes

### <a name="task-1"></a>Tâche 1

Explorez la page d’accueil du portail de conformité Microsoft Purview, puis apprenez à personnaliser l’apparence de la carte et le volet de navigation.

1. Ouvrez Microsoft Edge. Dans la barre d’adresses, entrez **admin.microsoft.com**.
1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par le fournisseur d’hébergement de votre labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par le fournisseur d’hébergement de votre labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**. Vous accédez ainsi à la page du Centre d’administration Microsoft 365.
1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.
1. Sous les Centres d’administration, sélectionnez **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.  
1. Sur cette page, la section réservée aux cartes vous permet de connaître d’un coup d’œil la situation de sécurité de votre organisation, les solutions disponibles pour celle-ci, etc.
1. Depuis la fenêtre principale, faites défiler vers le bas pour consulter les différentes cartes. Les cartes disponibles sur l’écran d’accueil ainsi que leur emplacement peuvent être modifiés pour s’adapter aux préférences de chaque administrateur.  
1. Survolez la barre de titre de n’importe quelle carte avec votre curseur : celle-ci devient grise.  Lorsque votre curseur se transforme en croix, vous pouvez déplacer la carte où vous le souhaitez.
1. Dans la barre de titre de chaque carte, vous voyez aussi des points de suspension qui proposent des actions à exécuter.  Cliquez sur les points de suspension du Catalogue de solutions et sélectionnez **Supprimer**.
1. Vous pouvez ajouter des cartes en cliquant sur **+ Ajouter des cartes**.  La fenêtre d’ajout de cartes à votre page d’accueil s’ouvre.  Placez le curseur de votre souris sur la carte présentée dans cette fenêtre et faites-la glisser sur l’écran d’accueil à l’endroit où vous voulez la placer.
1. En tant qu’administrateur de la conformité, il peut y avoir un ensemble de solutions que vous gérez pour notre organisation et, en tant que tel, vous souhaiterez peut-être que seules les solutions indiquées dans le volet de navigation s’affichent. Pour personnaliser vos préférences, sélectionnez **Personnaliser la navigation**.  
1. À partir de la fenêtre intitulée Personnaliser votre volet de navigation, notez comment vous pouvez sélectionner les éléments que vous souhaitez voir apparaître dans le panneau de navigation et désélectionner les éléments que vous ne souhaitez pas afficher. Dans le cadre de ces labos, conservez tous les éléments sélectionnés, puis cliquez sur **Enregistrer** en bas de la fenêtre.  
1. Laissez cet onglet du navigateur ouvert.

### <a name="task-2"></a>Tâche 2

Découvrez la situation de sécurité de votre organisation par l’intermédiaire du Gestionnaire de conformité.

1. Dans le volet de navigation situé à gauche du portail de conformité Microsoft Purview, sélectionnez **Gestionnaire de conformité**.  Vous pouvez aussi sélectionnez Gestionnaire de conformité dans la barre de titre de la carte Gestionnaire de conformité.

1. Vérifiez qu’**Aperçu** est bien sélectionné (souligné) en haut de la page du Gestionnaire de conformité. Faites défiler vers le bas pour consulter l’ensemble des informations disponibles sur la page.  Les informations de cette page comprennent votre score de conformité. Il est calculé d’après les points que vous avez accumulés et ceux accumulés par la gestion de Microsoft.   Vous voyez les principales actions d’amélioration, les solutions qui influent sur votre score ainsi que le score de conformité réparti par catégorie.

1. Sélectionnez **Actions d’amélioration** en haut de la page de présentation.  Ce sont des actions qui peuvent améliorer le score de conformité de l’organisation. Notez qu’à mesure que des actions d’amélioration sont effectuées, la mise à jour des points peut prendre jusqu’à 24 heures.  Prenez note des filtres disponibles.

1. Sélectionnez **Activer la réinitialisation de mot de passe en libre-service** dans la liste des actions d’amélioration.  Passez en revue les informations disponibles pour l’action d’amélioration.  Le côté gauche de la fenêtre donne une brève vue d’ensemble de l’implémentation, de l’état des tests, etc. À droite de la vue d’ensemble, vous avez une page de détails dans laquelle vous pouvez sélectionner l’implémentation, les tests, les standards et les exigences réglementaires associés, ainsi que les documents. Chacun de ces onglets fournit des informations plus détaillées sur l’action d’amélioration.

1. Quittez cette action d’amélioration en sélectionnant **Actions d’amélioration** dans le fil d’Ariane en haut à gauche de la page.  Vous revenez maintenant à la page des actions d’amélioration.

1. Cliquez sur **Solutions** en haut de la page. Dans cette page, vous voyez comment les solutions contribuent à votre score et comment encore l’améliorer.

1. Cliquez sur **Évaluations** en haut de la page. Dans cette page, vous voyez la base de référence de protection des données pour Microsoft 365.  Il s’agit d’une évaluation de référence par défaut fournie par Microsoft dans le Gestionnaire de conformité pour Microsoft 365.  Cette évaluation de la base de référence dispose d’un ensemble de contrôles pour des réglementations et des normes clés destinées à la protection et à la gouvernance des données en général. Quand vous ajoutez vos propres évaluations au Gestionnaire de conformité, il vous aide de plus en plus à répondre aux besoins spécifiques de votre organisation.

1. Sélectionnez **Base de référence de protection des données**.  À gauche de la page, une vue d’ensemble vous donne des détails et des informations À propos de.  Développez **À propos de** et passez en revue la description de la base de référence de protection des données Microsoft 365.  À droite de la page, notez les informations disponibles sous l’onglet de progression et les actions d’amélioration. En haut de la page se trouvent des onglets que vous pouvez sélectionner pour voir des informations plus détaillées sur les contrôles, vos actions d’amélioration et les actions Microsoft. Explorez-les à volonté. 

1. En haut à gauche de la page, au-dessus de « Base de référence de protection des données pour Microsoft 365 » (la barre de navigation), sélectionnez **Évaluation** pour revenir à l’onglet des évaluations dans le Gestionnaire de conformité.  

1. Sélectionnez **Modèles d’évaluation** en haut de la page.  Cette page liste les modèles disponibles et est organisée par modèles inclus et modèles Premium (vous devez peut-être faire défiler vers le bas et/ou développer la liste pour les voir).  Vous pouvez créer des évaluations pour votre organisation à partir d’un modèle existant, ou en créer un.
    1. Dans la liste des modèles inclus, sélectionnez un modèle. Cliquez sur **+ Créer une évaluation** en haut à droite de la page.  Ici, vous pouvez voir les étapes et informations nécessaires pour créer une évaluation à partir d’un modèle existant : identifier le produit pour l’évaluation, nommer l’évaluation et l’attribuer à un groupe.  Sélectionnez Annuler en bas de la page.

1. Fermez tous les onglets ouverts du navigateur.

### <a name="review"></a>Révision

Dans ce labo, vous avez exploré la page d’accueil du portail de conformité Microsoft Purview et vu comment les fonctionnalités du Gestionnaire de conformité peuvent aider les organisations à améliorer leur posture de conformité.
