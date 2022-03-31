---
Demo:
  title: Microsoft Sentinel
  module: 'Module 3 Lesson 3: Describe the capabilities of Microsoft security solutions: Describe security capabilities of Microsoft Sentinel'
ms.openlocfilehash: 607c8097d17041f711aa1f40601e8433fcfce7f0
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/14/2022
ms.locfileid: "137894096"
---
# <a name="demo-microsoft-sentinel"></a>Démonstration : Microsoft Sentinel 

### <a name="demo-scenario"></a>Scénario de la démonstration
Lors de cette démonstration, vous présenterez le processus de création d’une instance Microsoft Sentinel.  Vous définirez également les autorisations pour assurer l’accès aux ressources qui vont être déployées pour prendre en charge Microsoft Sentinel.  Une fois la configuration de base terminée, vous allez connecter Microsoft Sentinel à vos sources de données en quelques étapes, puis utiliser l’analyse intégrée pour être averti en cas d’activité suspecte, avant de découvrir les possibilités d’automatisation.  

#### <a name="demo-part-1--create-an-microsoft-sentinel-instance"></a>Partie 1 de la démonstration :  Créer une instance Microsoft Sentinel

1. Ouvrez l’onglet du navigateur intitulé **Accueil-Microsoft Azure**.  Si vous avez fermé l’onglet, ouvrez une page du navigateur et saisissez portal.azure.com dans la barre d’adresse. Ensuite, reconnectez-vous.

1. Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **Sentinel** puis sélectionnez **Microsoft Sentinel** à partir des résultats de la recherche.

1. Dans la page Microsoft Sentinel, sélectionnez **Créer Microsoft Sentinel**.

1. Dans la page Ajouter Microsoft Sentinel à un espace de travail, sélectionnez **Créer un espace de travail**.

1. À partir de l’onglet de base de l’espace de travail Créer un journal d’analyses, saisissez les informations suivantes :
    1. Abonnement :  **Pass Azure - Parrainage**
    1. Groupe de ressources : sélectionnez **Créer un nouveau**, puis saisissez le nom **SC900-Sentinel-RG** et sélectionnez **OK**.
    1. Nom : **SC900-LogAnalytics-workspace**.
    1. Région : **USA Est** (conservez le paramètre par défaut)
    1. Sélectionnez **Suivant : Niveau tarifaire >**

1. Pour le niveau tarifaire, conservez les paramètres par défaut : **Paiement à l’utilisation (par Go 2018)** , puis sélectionnez **Suivant : Étiquettes >** .

1. Pour les balises, vous pouvez laissez ce champ vide, puis sélectionnez **Examiner et créer**.

1. Vérifiez les informations que vous avez saisies, puis sélectionnez **Créer**.

1. Cela peut prendre une ou deux minutes avant que l’espace de travail n’apparaisse. Si vous ne le voyez toujours pas, sélectionnez **Actualiser**, puis **Ajouter**.

1. Une fois le nouvel espace de travail ajouté, la page Microsoft Sentinel | Actualités et guides s’affiche.  Notez les trois étapes indiquées sur la page Mise en route.

1. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.

#### <a name="demo-part-2--with-the-microsoft-sentinel-instance-created-you-will-want-to-make-sure-that-you-have-the-necessary-access-to-the-resources-that-get-deployed-to-support-microsoft-sentinel--in-this-task-you-will-go-to-the-access-control-iam-page-for-the-resource-group-that-you-created-with-the-instance-of-microsoft-sentinel-view-the-available-roles-and-assign-yourself-mod-administrator-the-required-role-assigning-the-role-at-the-resource-group-level-will-ensure-the-role-will-apply-to-all-the-resources-that-are-deployed-to-support-microsoft-sentinel"></a>Partie 2 de la démonstration :  Avec la création de l’instance Microsoft Sentinel, vous voudrez vous assurer que vous avez les accès nécessaires aux ressources qui sont déployées pour prendre en charge Microsoft Sentinel.  Pour cette tâche, vous vous rendrez sur la page de contrôle d’accès (IAM) pour le groupe de ressources que vous avez créé avec l’instance de Microsoft Sentinel, vous afficherez les rôles disponibles et vous vous attribuerez le rôle nécessaire (administrateur MOD). Assigner le rôle pour le niveau de groupe de ressources garantira que le rôle s’applique à toutes les ressources qui sont déployées pour prendre en charge Microsoft Sentinel.

1. Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **groupes de ressources** puis sélectionnez **Groupes de ressources** à partir des résultats de la echerche.

1. Depuis la page des groupes de ressources, sélectionnez le groupe de ressources que vous avez créé avec Microsoft Sentinel, **SC900-Sentinel-RG**.

1. Depuis la page SC900-Sentinel-RG, sélectionnez **Contrôle d’accès (IAM)** dans le volet de navigation à gauche.

1. Depuis la page Contrôle d’accès, sélectionnez **Afficher mon accès**.  Remarquez que le rôle actuel est Administrateur de service.  Fermez la fenêtre des attributions d’administrateur MOD en cliquant sur le **X** en haut à droite de la fenêtre.

1. Depuis la page Contrôle d’accès, sélectionnez **+Ajouter**, puis **Ajouter une attribution de rôle**.

1. La fenêtre d’attribution de rôle s’ouvre.  Sélectionnez la flèche déroulante vers le bas dans le champ Sélectionner un rôle afin d’afficher les rôles disponibles. Dans la barre de recherche Sélectionner un rôle, saisissez **Microsoft Sentinel** pour afficher les quatre rôles associés à Microsoft Sentinel. Nous recommandons d’attribuer le privilège minimum nécessaire pour ce rôle.  Pour les besoins de ce labo, saisissez **Propriétaire** dans la barre de recherche et sélectionnez **Propriétaire** à partir des résultats.  Pour référence, passez en revue les autorisations dans Microsoft Sentinel : https://docs.microsoft.com/en-us/azure/sentinel/roles

1. Depuis la liste des utilisateurs affichés, sélectionnez **Administrateur MOD**.

1. Sélectionnez **Enregistrer** au bas de la page.

1. Depuis la page Contrôle d’accès, sélectionnez **Afficher mon accès** pour confirmer que le rôle a bien été ajouté, puis fermez la fenêtre en sélectionnant le **X** en haut à droite.

#### <a name="demo-part-3--in-this-part-of-the-demo-you-will-walk-through-the-process-of-connecting-microsoft-sentinel-to-your-data-source-to-begin-to-collect-data--note-it-can-take-a-bit-time-to-show-the-connected-status-of-a-connector-30-minutes-depending-on-the-tenant"></a>Partie 3 de la démonstration :  Dans cette partie de la démonstration, vous expliquerez le processus pour connecter Microsoft Sentinel à votre source de données pour commencer à collecter des données.  Remarque : le statut connecté d’un connecteur peut prendre un moment avant de s’afficher (environ 30 minutes selon le locataire).

1. Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **Sentinel** puis sélectionnez **Microsoft Sentinel** à partir des résultats de la recherche.

1. Depuis la page Microsoft Sentinel, sélectionnez l’espace de travail que vous avez créé avec l’instance de Microsoft Sentinel, **SC900-LogAnalytics-workspace**.

1. La première étape avec Microsoft Sentinel consiste à pouvoir collecter des données. Dans le volet de navigation à gauche, sélectionnez **Connecteurs de données**, qui se trouve sous configuration.

1. Depuis la page Connecteurs de données, sur la page principale, faites défiler vers le bas pour afficher la liste étendue des connecteurs disponibles. Dans la barre de recherche de la page des connecteurs de données, saisissez **Azure** puis, à partir de la liste, sélectionnez **Azure Active Directory**.

1. La fenêtre de connecteur Azure Active Directory s’ouvre.  Sélectionnez **Ouvrir la page du connecteur**.

1. Depuis la page du connecteur Azure Active Directory, examinez la description et remarquez le contenu associé. Cela comprend les classeurs, les requêtes et les modèles de règles d’analyse.  

1. L’onglet des instructions de la fenêtre principale fournit les conditions requises pour que Microsoft Sentinel s’intègre à Azure Active Directory.   Sous configuration, sélectionnez **Journaux de connexion** puis Appliquer les modifications (plusieurs connecteurs peuvent être choisis).  Remarque : le statut connecté du connecteur peut prendre un moment avant de s’afficher (environ 30 minutes).  Pour référence :
    1. Vérification des autorisations dans Microsoft Sentinel : https://docs.microsoft.com/en-us/azure/sentinel/roles
    1. Connexion à Azure Active Directory : https://docs.microsoft.com/en-us/azure/sentinel/connect-azure-active-directory

1. Depuis l’onglet Étapes suivantes, notez la liste de classeurs recommandés.   Sous classeurs recommandés, sélectionnez **Journaux de connexion Azure** (des classeurs supplémentaires peuvent être choisis).

1. Depuis la page des classeurs et avec l’onglet modèles sélectionné (souligné), sélectionnez **Journaux de connexion Azure**.

1. Depuis la fenêtre Journaux de connexion Azure AD qui s’ouvre, examinez la description et sélectionnez **Afficher le modèle**.  Fermez le modèle en sélectionnant le **X** en haut à droite de l’écran.  Sélectionnez **Enregistrer** en bas de la page, puis sélectionnez **OK** pour enregistrer le classeur à l’emplacement par défaut.

1. En haut à gauche de la page Classeurs, au-dessus de Classeurs, sélectionnez **Microsoft Sentinel**. Cela vous fait revenir à la page des connecteurs de données Microsoft Sentinel.

1. Le haut de la page Connecteurs de données doit afficher 1 connecté, afin de refléter le fait que vous êtes connecté à Azure Active Directory.

1. Dans le volet de navigation à gauche, sélectionnez **Classeurs**.

1. Depuis la page Classeurs, sélectionnez l’onglet **Mes classeurs** qui se trouve au-dessus de la barre de recherche.  Le classeur que vous venez d’enregistrer est répertorié et disponible pour que vous puissiez visualiser et contrôler vos données.  Les connexions suivantes apparaîtront dans le classeur. Vous pouvez donc choisir de les afficher.

1. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.

#### <a name="demo-part-4-optional--in-this-part-of-the-demo-you-will-walk-through-the-process-of-using-a-built-in-analytics-rule-template-to-create-a-rule-to-get-notified-when-something-suspicious-occurs"></a>Partie 4 de la démonstration (facultative) :  Dans cette partie de la démonstration, vous expliquerez le processus d’utilisation d’un modèle de règle d’analyse intégré afin de créer une règle pour être informé en cas d’activité suspecte.

1. Dans le volet de navigation à gauche, sélectionnez **Analyse**.

1. La page Analyse affiche les règles actives (la détection avancée des attaques multiphases est activée par défaut) et permet d’accéder aux modèles de règle.  Sélectionnez l’onglet **Modèles de règle**.  Notez la liste des modèles disponibles et les différentes façons de filtrer la liste.  Grâce aux alertes analytiques intégrées dans l’espace de travail Microsoft Sentinel, vous êtes notifié quand un événement suspect se produit.

1. Dans la barre de recherche, saisissez **Portail Azure**.  Sélectionnez **Échec des tentatives de connexions au portail Azure**.  

1. Depuis la fenêtre qui s’ouvre, lisez la description et examinez les informations associées au modèle.  Sélectionnez **Créer une règle** au bas de la page.
    1. Depuis l’assistant Règle d’analyse, examinez les informations, puis sélectionnez **Suivant : Définir la logique de la règle >** .
    1. C’est sur la page Définir la logique de la règle que vous définissez la logique pour votre nouvelle règle d’analyse. Le modèle fournit déjà une certaine logique et des paramètres prédéfinis.  Faites défiler la page pour voir les paramètres disponibles.  Conservez les paramètres par défaut. Sélectionnez **Suivant : Paramètres des incidents (préversion)>** .
    1. Avec les paramètres d’incident, les alertes Microsoft Sentinel peuvent être regroupées en un incident qui doit être examiné. Vous pouvez définir si les alertes qui sont déclenchées par cette règle d’analyse doivent générer des incidents ou non.  Conservez les paramètres par défaut et sélectionnez **Suivant : Réponse automatisée >** .
    1. Dans l’onglet Réponse automatisée, remarquez comment vous pouvez ajouter un playbook pour automatiser la réponse.  De la même façon, vous pouvez créer une règle d’automatisation d’incident.  Sélectionnez **+ Ajouter** une nouvelle sous l’automatisation d’incident.  Une fenêtre pour créer une nouvelle règle d’automatisation s’ouvre.  Toute règle d’automatisation que vous créez sur cette page est déclenchée par la règle d’analyse que vous avez initialement sélectionnée, dans ce cas, Échec des tentatives de connexion au portail Azure.  Remarquez que vous pouvez ajouter des conditions et définir des actions pour la règle.   Cliquez sur **Annuler** pour quitter la fenêtre.
    1. Sélectionnez **Suivant : Révision>** pour revoir tous les détails associés à la règle et basés sur le modèle choisi. Vous pouvez maintenant choisir de créer la règle en sélectionnant **Créer** ou quitter sans créer de règle en sélectionnant le **X** en haut à droite de la page.

1. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.

#### <a name="demo-step-5-optional--in-the-previous-step-you-created-an-analytics-rule-to-be-alerted-of-suspicious-activities--embedded-in-that-wizard-is-the-option-to-automate-the-response-to-an-incident-based-on-the-specific-rule--but-you-can-also-create-automation-rules-by-going-directly-to-the-automation-configuration-option"></a>Partie 5 de la démonstration (facultative) :  À l’étape précédente, vous avez créé une règle d’analyse pour être informé en cas d’activité suspecte.  L’option permettant d’automatiser la réponse à un incident basé sur une règle spécifique est incluse dans cet assistant.  Mais vous pouvez aussi créer des règles d’automatisation en accédant directement à l’option de configuration d’automatisation.

1. Dans le volet de navigation à gauche, sélectionnez **Automatisation**.  

1. Sélectionnez **+ Créer**. À partir du menu déroulant, remarquez comment vous pouvez choisir d’ajouter un nouveau playbook ou une nouvelle règle.  Sélectionnez **Ajouter une nouvelle règle**.  
    1. Une fenêtre pour créer une nouvelle règle d’automatisation s’ouvre.  Remarquez que vous pouvez ajouter des conditions et définir des actions pour la règle.  La seule distinction est que la première condition est d’associer les règles d’analyse auxquelles vous voulez appliquer cette règle d’automatisation.  Cette option était grisée lors de la tâche précédente, car l’automatisation était configurée pour la règle spécifique.  Sélectionnez **Annuler** pour quitter la fenêtre Créer une nouvelle règle d’automatisation.

1. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.

#### <a name="step-6-tear-down---instructor-do-this-step-after-class-delete-microsoft-sentinel-resource-group--microsoft-sentinel-is-billed-based-on-the-volume-of-data-ingested-for-analysis-in-microsoft-sentinel-although-the-amount-of-data-ingested-as-a-result-of-this-lab-is-minimal-it-is-recommended-that-you-delete-the-microsoft-sentinel-resource-group-when-you-are-done-exploring-the-features-of-capabilities-of-microsoft-sentinel"></a>Étape 6 : DESTRUCTION - Instructeur, effectuez cette étape après la classe. Supprimez le groupe de ressources Microsoft Sentinel.  Microsoft Sentinel est facturé en fonction du volume de données ingérées pour l’analyse dans Microsoft Sentinel. Bien que la quantité de données ingérées dans le cadre de ce labo soit minime, nous vous recommandons de supprimer le groupe de ressources Microsoft Sentinel quand vous avez fini de découvrir les fonctionnalités et les possibilités de Microsoft Sentinel.

1. Depuis la page Microsoft Sentinel, en haut à gauche, où il est indiqué Microsoft Sentinel, sélectionnez **Tous les services**.

1. Dans la barre de services de filtrage, saisissez groupes de ressources, puis à partir de la liste, sélectionnez **Groupes de ressources**.

1. Depuis la page des groupes de ressources, sélectionnez le groupe de ressources que vous avez créé avec Microsoft Sentinel, **SC900-Sentinel-RG**.

1. En haut au centre de la page, sélectionnez **Supprimer le groupe de ressources**.  Passez en revue l’avertissement.  Saisissez le nom du groupe de ressources, **SC900-Sentinel-RG**, puis sélectionnez **Supprimer** en bas de la page.  La suppression du groupe de ressources prend plusieurs minutes.

1. Une fois que vous avez vérifié que le groupe de ressources est bien supprimé, fermez la page de navigation. 

#### <a name="review"></a>Révision

Lors de cette démonstration, vous avez présenté le processus de création d’une instance Microsoft Sentinel.  Vous avez également présenté comment définir les autorisations pour assurer l’accès aux ressources associées à votre instance Microsoft Sentinel.  Une fois l’instance Microsoft Sentinel créée, vous avez expliqué les étapes pour connecter Sentinel à vos sources de données, vous avez montré comment utiliser des règles d’analyse intégrées pour être informé en cas d’activité suspecte. Enfin, vous avez découvert les possibilités d’automatisation. Vous avez terminé cette démonstration en supprimant le groupe de ressources associé à l’instance Microsoft Sentinel que vous aviez créée.