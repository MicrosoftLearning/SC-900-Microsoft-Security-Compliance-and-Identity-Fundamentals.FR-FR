---
lab:
  title: Explorer Microsoft Sentinel
  module: 'Module 3 Lesson 3: Describe the capabilities of Microsoft security solutions: Describe security capabilities of Microsoft Sentinel'
ms.openlocfilehash: c5a7ba866c82f15a4f78099326fd93a734caead8
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/14/2022
ms.locfileid: "137894000"
---
# <a name="lab-explore-microsoft-sentinel"></a>Labo : Explorer Microsoft Sentinel 

## <a name="lab-scenario"></a>Scénario du labo
Ce labo vous présente le processus de création d’une instance Microsoft Sentinel.  Vous définirez également les autorisations pour assurer l’accès aux ressources qui vont être déployées pour prendre en charge Microsoft Sentinel.  Une fois la configuration de base terminée, vous allez connecter Microsoft Sentinel à vos sources de données en quelques étapes, puis utiliser l’analyse intégrée pour être averti en cas d’activité suspecte, avant de découvrir les possibilités d’automatisation.  

  

**Durée estimée** : 30-45 minutes

#### <a name="task-1--create-an-microsoft-sentinel-instance"></a>Tâche 1 :  Créez une instance Microsoft Sentinel.

1. Ouvrez Microsoft Edge. Dans la barre d’adresse, saisissez **portal.azure.com**.

2. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    
    1. Saisissez le mot de passe d’administrateur communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

3. Dans le coin supérieur gauche de l’écran, en regard de la mention Microsoft Azure, sélectionnez l’icône de menu Afficher le portail (les trois lignes horizontales également appelées icône Hamburger), puis sélectionnez **Tous les services**.  

4. Dans le champ destiné aux filtres, saisissez **Sentinel**, puis sélectionnez **Microsoft Sentinel** dans la liste.

5. Dans la page Microsoft Sentinel, sélectionnez **Créer Microsoft Sentinel**.

6. Dans la page Ajouter Microsoft Sentinel à un espace de travail, sélectionnez **Créer un espace de travail**.

7. À partir de l’onglet de base de l’espace de travail Créer un journal d’analyses, saisissez les informations suivantes :
    1. Abonnement :  **Pass Azure - Parrainage**
   
    1. Groupe de ressources : sélectionnez **Create New**, puis saisissez le nom **SC900-ResourceGroup** avant de confirmer avec **OK**.
    1. Nom : **SC900-LogAnalytics-workspace**.
    1. Région : **USA Est** (conservez le paramètre par défaut)
    1. Sélectionnez **Suivant : Niveau tarifaire >**

8. Pour le niveau tarifaire, conservez les paramètres par défaut : **Paiement à l’utilisation (par Go 2018)** , puis sélectionnez **Suivant : Étiquettes >** .

9. Pour les balises, vous pouvez laissez ce champ vide, puis sélectionnez **Examiner et créer**.

10. Vérifiez les informations que vous avez saisies, puis sélectionnez **Créer**.

11. Si le nouvel espace de travail créé ne s’affiche pas, sélectionnez **Actualiser**, puis **Ajouter**.

12. Une fois le nouvel espace de travail ajouté, la page Microsoft Sentinel | Actualités et guides s’affiche.  Notez les trois étapes indiquées sur la page Mise en route.

13. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.

#### <a name="task-2--with-the-microsoft-sentinel-instance-created-you-will-want-to-make-sure-that-you-have-the-necessary-access-to-the-resources-that-get-deployed-to-support-microsoft-sentinel--in-this-task-you-will-go-to-the-access-control-iam-page-for-the-resource-group-that-you-created-with-the-instance-of-microsoft-sentinel-view-the-available-roles-and-assign-yourself-mod-administrator-the-required-role-assigning-the-role-at-the-resource-group-level-will-ensure-the-role-will-apply-to-all-the-resources-that-are-deployed-to-support-microsoft-sentinel"></a>Tâche 2 :  Avec la création de l’instance Microsoft Sentinel, vous voudrez vous assurer que vous avez les accès nécessaires aux ressources qui sont déployées pour prendre en charge Microsoft Sentinel.  Pour cette tâche, vous vous rendrez sur la page de contrôle d’accès (IAM) pour le groupe de ressources que vous avez créé avec l’instance de Microsoft Sentinel, vous afficherez les rôles disponibles et vous vous attribuerez le rôle nécessaire (administrateur MOD). Assigner le rôle pour le niveau de groupe de ressources garantira que le rôle s’applique à toutes les ressources qui sont déployées pour prendre en charge Microsoft Sentinel.

1. Depuis la page Microsoft Sentinel, en haut à gauche, où il est indiqué Microsoft Sentinel, sélectionnez **Tous les services**.

2. Dans la barre de services de filtrage, saisissez groupes de ressources, puis à partir de la liste, sélectionnez **Groupes de ressources**.

3. Sur la page des groupes de ressources, sélectionnez celui que vous avez créé avec Microsoft Sentinel, **SC900-ResourceGroup**.

4. Sur la page suivante, sélectionnez **Access control (IAM)** dans le volet de navigation situé à gauche.

5. Depuis la page Contrôle d’accès, sélectionnez **Afficher mon accès**.  Vous constaterez que le rôle actuel est celui d’administrateur de sécurité.  Fermez la fenêtre des attributions d’administrateur MOD en cliquant sur le **X** en haut à droite de la fenêtre.

6. Depuis la page Contrôle d’accès, sélectionnez **+Ajouter**, puis **Ajouter une attribution de rôle**.

7. La fenêtre d’attribution de rôle s’ouvre.  Sélectionnez la flèche déroulante vers le bas dans le champ Sélectionner un rôle afin d’afficher les rôles disponibles.  Sélectionnez **Propriétaire** pour ce labo.  REMARQUE :  Nous recommandons d’attribuer le privilège minimum nécessaire pour ce rôle.  Pour référence, passez en revue les autorisations dans Microsoft Sentinel : https://docs.microsoft.com/en-us/azure/sentinel/roles

8. Depuis la liste des utilisateurs affichés, sélectionnez **Administrateur MOD**.

9. Sélectionnez **Enregistrer** au bas de la page.

10. Depuis la page Contrôle d’accès, sélectionnez **Afficher mon accès** pour confirmer que le rôle a bien été ajouté, puis fermez la fenêtre en sélectionnant le **X** en haut à droite.

11. Revenez à la page générale des services d’Azure en sélectionnant **Tous les services** dans le coin supérieur gauche, au-dessus des groupes de ressources.

#### <a name="task-3--in-this-task-you-will-walk-through-the-process-of-connecting-microsoft-sentinel-to-your-data-source-to-begin-to-collect-data-note-it-can-take-a-bit-time-to-show-the-connected-status-of-a-connector-30-minutes-depending-on-the-tenant"></a>Tâche 3 :  Cette tâche vous présente le processus de connexion entre Microsoft Sentinel et votre source de données, afin de démarrer la collecte de données. Remarque : le statut connecté d’un connecteur peut prendre un moment avant de s’afficher (environ 30 minutes selon le locataire).

1. Dans le champ destiné aux filtres sur la page Tous les services, saisissez **Microsoft Sentinel**, puis sélectionnez **Microsoft Sentinel** dans la liste des résultats. 

2. Depuis la page Microsoft Sentinel, sélectionnez l’espace de travail que vous avez créé avec l’instance de Microsoft Sentinel, **SC900-LogAnalytics-workspace**.

3. La première étape avec Microsoft Sentinel consiste à pouvoir collecter des données. Dans le volet de navigation à gauche, sélectionnez **Connecteurs de données**, qui se trouve sous configuration.

4. Depuis la page Connecteurs de données, sur la page principale, faites défiler vers le bas pour afficher la liste étendue des connecteurs disponibles. Dans la barre de recherche de la page des connecteurs de données, saisissez **Azure** puis, à partir de la liste, sélectionnez **Azure Active Directory**.

5. La fenêtre de connecteur Azure Active Directory s’ouvre.  Sélectionnez **Ouvrir la page du connecteur**.

6. Depuis la page du connecteur Azure Active Directory, examinez la description et remarquez le contenu associé. Cela comprend les classeurs, les requêtes et les modèles de règles d’analyse.  

7. L’onglet des instructions de la fenêtre principale fournit les conditions requises pour que Microsoft Sentinel s’intègre à Azure Active Directory.   Sous configuration, sélectionnez **Journaux de connexion** puis Appliquer les modifications (plusieurs connecteurs peuvent être choisis).

8. Depuis l’onglet Étapes suivantes, notez la liste de classeurs recommandés.   Sous classeurs recommandés, sélectionnez **Journaux de connexion Azure** (des classeurs supplémentaires peuvent être choisis).

9. Depuis la page des classeurs et avec l’onglet modèles sélectionné (souligné), sélectionnez **Journaux de connexion Azure**. 

10. Depuis la fenêtre Journaux de connexion Azure AD qui s’ouvre, examinez la description et sélectionnez **Afficher le modèle**.  Fermez le modèle en sélectionnant le **X** en haut à droite de l’écran.  Sélectionnez **Enregistrer** en bas de la page, puis sélectionnez **OK** pour enregistrer le classeur à l’emplacement par défaut.

11. En haut à gauche de la page Classeurs, au-dessus de Classeurs, sélectionnez **Microsoft Sentinel**. Cela vous fait revenir à la page des connecteurs de données Microsoft Sentinel.

12. Le haut de la page Connecteurs de données doit afficher 1 connecté, afin de refléter le fait que vous êtes connecté à Azure Active Directory.

13. Dans le volet de navigation à gauche, sélectionnez **Classeurs**.

14. Depuis la page Classeurs, sélectionnez l’onglet **Mes classeurs** qui se trouve au-dessus de la barre de recherche.  Le classeur que vous venez d’enregistrer est répertorié et disponible pour que vous puissiez visualiser et contrôler vos données.

15. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.

#### <a name="task-4--in-this-task-you-will-walk-through-the-process-of-using-a-built-in-analytics-rule-template-to-create-a-rule-to-get-notified-when-something-suspicious-occurs"></a>Tâche 4 :  Cette tâche vous présente le processus d’utilisation d’un modèle de règle pour l’analyse intégrée, afin de créer une règle qui vous alerte en cas d’activité suspecte.

1. Dans le volet de navigation à gauche, sélectionnez **Analyse**.

2. La page Analyse affiche les règles actives (la détection avancée des attaques multiphases est activée par défaut) et permet d’accéder aux modèles de règle.  Sélectionnez l’onglet **Modèles de règle**.  Notez la liste des modèles disponibles et les différentes façons de filtrer la liste.  Grâce aux alertes analytiques intégrées dans l’espace de travail Microsoft Sentinel, vous êtes notifié quand un événement suspect se produit.

3. Dans la barre de recherche, saisissez **Portail Azure**.  Sélectionnez **Échec des tentatives de connexions au portail Azure**.  

4. Depuis la fenêtre qui s’ouvre, lisez la description et examinez les informations associées au modèle.  Sélectionnez **Créer une règle** au bas de la page.

5. Depuis l’assistant Règle d’analyse, examinez les informations, puis sélectionnez **Suivant : Définir la logique de la règle >** .

6. C’est sur la page Définir la logique de la règle que vous définissez la logique pour votre nouvelle règle d’analyse. Le modèle fournit déjà une certaine logique et des paramètres prédéfinis.  Faites défiler la page pour voir les paramètres disponibles.  Conservez les paramètres par défaut. Sélectionnez **Suivant : Paramètres des incidents (préversion)>** .

7. Avec les paramètres d’incident, les alertes Microsoft Sentinel peuvent être regroupées en un incident qui doit être examiné. Vous pouvez définir si les alertes qui sont déclenchées par cette règle d’analyse doivent générer des incidents ou non.  Conservez les paramètres par défaut et sélectionnez **Suivant : Réponse automatisée >** .

8. Dans l’onglet Réponse automatisée, remarquez comment vous pouvez ajouter un playbook pour automatiser la réponse.  De la même façon, vous pouvez créer une règle d’automatisation d’incident.  Sélectionnez **+ Ajouter** une nouvelle sous l’automatisation d’incident.  Une fenêtre pour créer une nouvelle règle d’automatisation s’ouvre.  Toutes les règles d’automatisation que vous créez sur cette page sont déclenchées par la règle d’analyse que vous   Remarquez que vous pouvez ajouter des conditions et définir des actions pour la règle.   Cliquez sur **Annuler** pour quitter la fenêtre.

9. Sélectionnez **Suivant : Révision>** pour revoir tous les détails associés à la règle et basés sur le modèle choisi. Vous pouvez maintenant choisir de créer la règle en sélectionnant **Créer** ou quitter sans créer de règle en sélectionnant le **X** en haut à droite de la page.

10. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.

#### <a name="task-5--in-the-previous-task-you-created-an-analytics-rule-to-be-alerted-of-suspicious-activities--embedded-in-that-wizard-is-the-option-to-automate-the-response-to-an-incident-based-on-the-specific-rule--but-you-can-also-create-automation-rules-by-going-directly-to-the-automation-configuration-option"></a>Tâche 5 :  Lors de la tâche précédente, vous avez créé une règle d’analyse qui vous alerte en cas d’activité suspecte.  L’option permettant d’automatiser la réponse à un incident basé sur une règle spécifique est incluse dans cet assistant.  Mais vous pouvez aussi créer des règles d’automatisation en accédant directement à l’option de configuration d’automatisation.

1. Dans le volet de navigation à gauche, sélectionnez **Automatisation**.  

2. Sélectionnez **+ Créer**. À partir du menu déroulant, remarquez comment vous pouvez choisir d’ajouter un nouveau playbook ou une nouvelle règle.  Sélectionnez **Ajouter une nouvelle règle**.  

3. Une fenêtre pour créer une nouvelle règle d’automatisation s’ouvre.  Remarquez que vous pouvez ajouter des conditions et définir des actions pour la règle.  La seule distinction est que la première condition est d’associer les règles d’analyse auxquelles vous voulez appliquer cette règle d’automatisation.  Cette option était grisée lors de la tâche précédente, car l’automatisation était configurée pour la règle spécifique.  Sélectionnez **Annuler** pour quitter la fenêtre Créer une nouvelle règle d’automatisation.

4. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.


#### <a name="task-6--delete-microsoft-sentinel-resource-group--microsoft-sentinel-is-billed-based-on-the-volume-of-data-ingested-for-analysis-in-microsoft-sentinel-although-the-amount-of-data-ingested-as-a-result-of-this-lab-is-minimal-it-is-recommended-that-you-delete-the-microsoft-sentinel-resource-group-when-you-are-done-exploring-the-features-of-capabilities-of-microsoft-sentinel"></a>Tâche 6 :  Supprimez le groupe de ressources Microsoft Sentinel.  Microsoft Sentinel est facturé en fonction du volume de données ingérées pour l’analyse dans Microsoft Sentinel. Bien que la quantité de données ingérées dans le cadre de ce labo soit minime, nous vous recommandons de supprimer le groupe de ressources Microsoft Sentinel quand vous avez fini de découvrir les fonctionnalités et les possibilités de Microsoft Sentinel.

1. Depuis la page Microsoft Sentinel, en haut à gauche, où il est indiqué Microsoft Sentinel, sélectionnez **Tous les services**.

2. Dans la barre de services de filtrage, saisissez groupes de ressources, puis à partir de la liste, sélectionnez **Groupes de ressources**.

3. Sur la page des groupes de ressources, sélectionnez celui que vous avez créé avec Microsoft Sentinel, **SC900-ResourceGroup**.

4. En haut au centre de la page, sélectionnez **Supprimer le groupe de ressources**.  Passez en revue l’avertissement.  Saisissez le nom du groupe de ressources, **SC900-ResourceGroup**, puis sélectionnez **Supprimer** en bas de la page.  La suppression du groupe de ressources prend plusieurs minutes.

5. Une fois que vous avez vérifié que le groupe de ressources est bien supprimé, fermez la page de navigation. 


#### <a name="review"></a>Révision

Ce labo vous a présenté le processus de création d’une instance Microsoft Sentinel.  Vous avez également configuré les autorisations nécessaires à l’accès aux ressources associées à votre instance Microsoft Sentinel.  Après la création de cette instance, vous avez connecté Microsoft Sentinel à vos sources de données en quelques étapes, grâce à des règles d’analyse intégrée pour être averti en cas d’activité suspecte, puis vous avez découvert les possibilités d’automatisation. Le labo a pris fin lorsque vous avez supprimé le groupe de ressources associé à l’instance Microsoft Sentinel que vous avez créée.
