---
lab:
    title: 'Explorer Microsoft Sentinel'
    module : 'Module 3, leçon 3 : Décrire les fonctionnalités des solutions de sécurité Microsoft : Décrire les fonctionnalités de sécurité de Microsoft Sentinel'
---


# Labo : Explorer Microsoft Sentinel 

## Scénario du labo
Dans ce labo, vous présenterez le processus de création d’une instance Microsoft Sentinel.  Vous définirez également les autorisations requises pour assurer l’accès aux ressources à déployer pour la prise en charge de Microsoft Sentinel.  Une fois cette configuration de base effectuée, vous expliquerez les étapes pour connecter Microsoft Sentinel à vos sources de données à l’aide d’analyses intégrées pour être informé en cas d’activité suspecte. Enfin, vous découvrirez les possibilités d’automatisation.  

  

**Durée estimée** : 30 à 45 minutes

#### Tâche 1 :  Créez une instance Microsoft Sentinel.

1. Ouvrez Microsoft Edge. Dans la barre d’adresse, saisissez **portal.azure.com**.

2. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, saisissez **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    
    1. Saisissez le mot de passe d’administrateur fourni par votre fournisseur d’hébergement de labo. Sélectionnez **Se connecter**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

3. Dans le coin supérieur gauche de l’écran, en regard de la mention Microsoft Azure, sélectionnez l’icône de menu Afficher le portail (les trois lignes horizontales également appelées icône Hamburger), puis sélectionnez **Tous les services**.  

4. Dans le champ destiné aux filtres, saisissez **Microsoft Sentinel**, puis sélectionnez **Microsoft Sentinel** dans la liste.

5. Sur la page Microsoft Sentinel, sélectionnez **Créer Microsoft Sentinel**.

6. Sur la page Ajouter Microsoft Sentinel à un espace de travail, sélectionnez **Créer un nouvel espace de travail**.

7. Sous l’onglet de base de l’espace de travail Créer un journal d’analyses, saisissez les informations suivantes :
    1. Abonnement :  **Pass Azure - Parrainage**
   
    1. Groupe de ressources : sélectionnez **Create New (Créer un nouveau)**, puis saisissez le nom **SC900-ResourceGroup** avant de confirmer avec **OK**.
    1. Nom : **SC900-LogAnalytics-workspace**.
    1. Région : **USA Est** (conservez le paramètre par défaut)
    1. Sélectionnez **Suivant : Niveau tarifaire >**

8. Pour le niveau tarifaire, conservez les paramètres par défaut : **Paiement à l’utilisation (par Go 2018)**, puis sélectionnez **Suivant : Balises >**.

9. Pour les balises, vous pouvez laissez ce champ vide, puis sélectionnez **Examiner et créer**.

10. Vérifiez les informations que vous avez saisies, puis sélectionnez **Créer**.

11. Si le nouvel espace de travail créé ne s’affiche pas, sélectionnez **Actualiser**, puis **Ajouter**.

12. Une fois le nouvel espace de travail ajouté, la page Microsoft Sentinel | News & guides s’affichera.  Notez les trois étapes indiquées sur la page Mise en route.

13. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.

#### Tâche 2 :  Avec la création de l’instance Microsoft Sentinel, assurez-vous que vous disposez des autorisations d’accès nécessaires aux ressources à déployer pour la prise en charge de Microsoft Sentinel.  Pour cette tâche, rendez-vous sur la page de contrôle d’accès (IAM) du groupe de ressources que vous avez créé avec l’instance de Microsoft Sentinel, affichez les rôles disponibles et attribuez-vous le rôle requis (administrateur MOD). Assigner le rôle pour le niveau de groupe de ressources garantira que le rôle s’applique à toutes les ressources qui sont déployées pour prendre en charge Microsoft Sentinel.

1. Sur la partie supérieure gauche de la page Microsoft Sentinel, en regard de la mention Microsoft Sentinel, sélectionnez **Tous les services**.

2. Dans la barre de services de filtrage, saisissez groupes de ressources, puis à partir de la liste, sélectionnez **Groupes de ressources**.

3. Sur la page Groupes de ressources, sélectionnez le groupe de ressources que vous avez créé avec Microsoft Sentinel, **SC900-ResourceGroup**.

4. Sur la page suivante, sélectionnez **Access control (IAM)** dans le volet de navigation situé à gauche.

5. Sur la page Contrôle d’accès, sélectionnez **Afficher mon accès**.  Vous constaterez que le rôle actuel est celui d’administrateur de sécurité.  Fermez la fenêtre des attributions d’administrateur MOD en cliquant sur le **X** en haut à droite de la fenêtre.

6. Depuis la page Contrôle d’accès, sélectionnez **+Ajouter**, puis **Ajouter une attribution de rôle**.

7. La fenêtre d’attribution de rôle s’ouvre.  Sélectionnez la flèche déroulante vers le bas dans le champ Sélectionner un rôle afin d’afficher les rôles disponibles.  Sélectionnez **Propriétaire** pour ce labo.  REMARQUE :  Nous recommandons d’attribuer le privilège minimum nécessaire pour ce rôle.  Pour référence, passez en revue les autorisations dans Microsoft Sentinel :  https://docs.microsoft.com/fr-fr/azure/sentinel/roles

8. Depuis la liste des utilisateurs affichés, sélectionnez **Administrateur MOD**.

9. Sélectionnez **Enregistrer** au bas de la page.

10. Depuis la page Contrôle d’accès, sélectionnez **Afficher mon accès** pour confirmer que le rôle a bien été ajouté, puis fermez la fenêtre en sélectionnant le **X** en haut à droite.

11. Revenez à la page générale des services d’Azure en sélectionnant **Tous les services** dans le coin supérieur gauche, au-dessus des groupes de ressources.

#### Tâche 3 :  Cette tâche vous présente le processus de connexion entre Microsoft Sentinel et votre source de données, afin de démarrer la collecte de données. Remarque : le statut connecté d’un connecteur peut prendre un moment avant de s’afficher (environ 30 minutes selon le locataire).

1. Dans le champ Filtrer les services de la page Tous les services, saisissez **Microsoft Sentinel**, puis sélectionnez **Microsoft Sentinel** dans la liste des résultats. 

2. Sur la page Microsoft Sentinel, sélectionnez l’espace de travail que vous avez créé avec l’instance de Microsoft Sentinel, **SC900-LogAnalytics-workspace**.

3. Dans Microsoft Sentinel, la première étape consiste à pouvoir collecter des données. Dans le volet de navigation de gauche, sélectionnez **Connecteurs de données**, sous l’option Configuration.

4. Depuis la page Connecteurs de données, sur la page principale, faites défiler vers le bas pour afficher la liste étendue des connecteurs disponibles. Dans la barre de recherche de la page Connecteurs de données, saisissez **Azure**, puis, dans la liste déroulante, sélectionnez **Azure Active Directory**.

5. La fenêtre Connecteur Azure Active Directory s’affiche.  Sélectionnez **Ouvrir la page du connecteur**.

6. Depuis la page du connecteur Azure Active Directory, examinez la description et remarquez le contenu associé. Cela comprend les classeurs, les requêtes et les modèles de règles d’analyse.  

7. L’onglet Instructions de la fenêtre principale présente les conditions requises pour l’intégration de Microsoft Sentinel à Azure Active Directory.   Sous l’option Configuration, sélectionnez **Journaux de connexion**, puis sélectionnez Appliquer les modifications (plusieurs connecteurs peuvent être choisis).

8. Depuis l’onglet Étapes suivantes, notez la liste de classeurs recommandés.   Sous classeurs recommandés, sélectionnez **Journaux de connexion Azure** (des classeurs supplémentaires peuvent être choisis).

9. Depuis la page des classeurs et avec l’onglet modèles sélectionné (souligné), sélectionnez **Journaux de connexion Azure**. 

10. Depuis la fenêtre Journaux de connexion Azure AD qui s’ouvre, examinez la description et sélectionnez **Afficher le modèle**.  Fermez le modèle en sélectionnant le **X** en haut à droite de l’écran.  Sélectionnez **Enregistrer** en bas de la page, puis sélectionnez **OK** pour enregistrer le classeur à l’emplacement par défaut.

11. En haut à gauche de la page Classeurs, au-dessus de la mention Classeurs, sélectionnez **Microsoft Sentinel**. Vous revenez au niveau de la page Connecteurs de données de Microsoft Sentinel.

12. Le haut de la page Connecteurs de données doit afficher 1 connecté, afin de refléter votre connexion à Azure Active Directory.

13. Dans le volet de navigation de gauche, sélectionnez **Classeurs**.

14. Sur la page Classeurs, cliquez sur l’onglet **Mes classeurs**, au-dessus de la barre de recherche.  Le classeur que vous venez d’enregistrer est répertorié et disponible pour que vous puissiez visualiser et contrôler vos données.

15. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.

#### Tâche 4 :  Cette tâche vous présente le processus d’utilisation d’un modèle de règle pour l’analyse intégrée, afin de créer une règle qui vous alerte en cas d’activité suspecte.

1. Dans le volet de navigation de gauche, sélectionnez **Analyse**.

2. La page Analyse affiche les règles actives (la détection avancée des attaques multiphases est activée par défaut) et permet d’accéder aux modèles de règle.  Sélectionnez l’onglet **Modèles de règle**.  Notez la liste des modèles disponibles et les différentes façons de filtrer la liste.  Les alertes d’analyse intégrées au sein de l’espace de Microsoft Sentinel vous informent en cas d’activité suspecte.

3. Dans la barre de recherche, saisissez **Portail Azure**.  Sélectionnez **Échec des tentatives de connexions au portail Azure**.  

4. Depuis la fenêtre qui s’ouvre, lisez la description et examinez les informations associées au modèle.  Sélectionnez **Créer une règle** au bas de la page.

5. Depuis l’assistant Règle d’analyse, examinez les informations, puis sélectionnez **Suivant : Définir la logique de la règle >**.

6. C’est sur la page Définir la logique de la règle que vous définissez la logique pour votre nouvelle règle d’analyse. Le modèle fournit déjà une certaine logique et des paramètres prédéfinis.  Faites défiler la page pour voir les paramètres disponibles.  Conservez les paramètres par défaut. Sélectionnez **Suivant : Paramètres d’incident (préversion) >**.

7. Avec les paramètres d’incident, les alertes Microsoft Sentinel peuvent être regroupées en un incident qui doit être examiné. Vous pouvez définir si les alertes qui sont déclenchées par cette règle d’analyse doivent générer des incidents ou non.  Conservez les paramètres par défaut et sélectionnez **Suivant : Réponse automatisée >**.

8. Dans l’onglet Réponse automatisée, remarquez comment vous pouvez ajouter un playbook pour automatiser la réponse.  De la même façon, vous pouvez créer une règle d’automatisation d’incident.  Sélectionnez **+ Ajouter** une nouvelle sous l’automatisation d’incident.  Une fenêtre pour créer une nouvelle règle d’automatisation s’ouvre.  Toutes les règles d’automatisation que vous créez sur cette page sont déclenchées par la règle d’analyse que vous   Remarquez que vous pouvez ajouter des conditions et définir des actions pour la règle.   Cliquez sur **Annuler** pour quitter la fenêtre.

9. Sélectionnez **Suivant : Révision>** pour revoir tous les détails associés à la règle et basés sur le modèle choisi. Vous pouvez maintenant choisir de créer la règle en sélectionnant **Créer** ou quitter sans créer de règle en sélectionnant le **X** en haut à droite de la page.

10. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.

#### Tâche 5 :  Lors de la tâche précédente, vous avez créé une règle d’analyse qui vous alerte en cas d’activité suspecte.  L’option permettant d’automatiser la réponse à un incident basé sur une règle spécifique est incluse dans cet assistant.  Mais vous pouvez aussi créer des règles d’automatisation en accédant directement à l’option de configuration d’automatisation.

1. Dans le volet de navigation de gauche, sélectionnez **Automatisation**.  

2. Sélectionnez **+ Créer**. À partir du menu déroulant, remarquez comment vous pouvez choisir d’ajouter un nouveau playbook ou une nouvelle règle.  Sélectionnez **Ajouter une nouvelle règle**.  

3. Une fenêtre pour créer une nouvelle règle d’automatisation s’ouvre.  Remarquez que vous pouvez ajouter des conditions et définir des actions pour la règle.  La seule distinction est que la première condition est d’associer les règles d’analyse auxquelles vous voulez appliquer cette règle d’automatisation.  Cette option était grisée lors de la tâche précédente, car l’automatisation était configurée pour la règle spécifique.  Sélectionnez **Annuler** pour quitter la fenêtre Créer une nouvelle règle d’automatisation.

4. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.


#### Tâche 6 :  Supprimez un groupe de ressources Microsoft Sentinel.  Microsoft Sentinel est facturé en fonction du volume de données ingérées pour l’analyse dans Microsoft Sentinel. Bien que la quantité de données ingérées dans le cadre de ce labo soit minime, nous vous recommandons de supprimer le groupe de ressources Microsoft Sentinel quand vous avez fini de découvrir les fonctionnalités et les possibilités de Microsoft Sentinel.

1. Sur la partie supérieure gauche de la page Microsoft Sentinel, en regard de la mention Microsoft Sentinel, sélectionnez **Tous les services**.

2. Dans la barre de services de filtrage, saisissez groupes de ressources, puis à partir de la liste, sélectionnez **Groupes de ressources**.

3. Sur la page Groupes de ressources, sélectionnez le groupe de ressources que vous avez créé avec Microsoft Sentinel, **SC900-ResourceGroup**.

4. En haut au centre de la page, sélectionnez **Supprimer le groupe de ressources**.  Passez en revue l’avertissement.  Saisissez le nom du groupe de ressources, **SC900-ResourceGroup**, puis sélectionnez **Supprimer** en bas de la page.  La suppression du groupe de ressources prend plusieurs minutes.

5. Une fois que vous avez vérifié que le groupe de ressources est bien supprimé, fermez la page de navigation. 


#### Révision

Ce labo vous a présenté le processus de création d’une instance Microsoft Sentinel.  Vous avez également configuré les autorisations nécessaires à l’accès aux ressources associées à votre instance Microsoft Sentinel.  Après la création de votre instance Microsoft Sentinel, vous avez connecté Microsoft Sentinel à vos sources de données en quelques étapes, grâce à des règles d’analyse intégrée, pour être averti en cas d’activité suspecte, puis vous avez découvert les possibilités d’automatisation. Le labo a pris fin lorsque vous avez supprimé le groupe de ressources associé à l’instance Microsoft Sentinel que vous avez créée.
