<!---
---
Labo : Titre : « Explorer Microsoft Sentinel » Parcours d’apprentissage/Module/Titre : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft ; Module 3 : Décrire les fonctionnalités de sécurité de Microsoft Sentinel ; Unité 3 : Décrire les fonctionnalités de détection et d’atténuation des menaces dans Microsoft Sentinel »
---
--->

# Labo : Explorer Microsoft Sentinel

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft
- Module : Décrire les fonctionnalités de sécurité de Microsoft Sentinel
- Unité : Décrire les fonctionnalités de détection et d’atténuation des menaces dans Microsoft Sentinel

## Scénario du labo

Vous allez présenter le processus de création d’une instance Microsoft Sentinel.  Vous définirez également les autorisations afin de garantir l’accès aux ressources qui seront déployées pour prendre en charge Microsoft Sentinel.  Une fois cette configuration de base effectuée, vous suivrez les étapes de connexion de Microsoft Sentinel à vos sources de données, configurerez un classeur et présenterez brièvement certaines des fonctionnalités clés disponibles dans Microsoft Sentinel.

**Durée estimée** : 45-60 minutes

### Tâche 1

Créer une instance Microsoft Sentinel

1. Vous devriez être sur la page d’accueil des services Azure.  Si vous avez précédemment fermé le navigateur, ouvrez Microsoft Edge. Dans la barre d’adresse, entrez **portal.azure.com** et connectez-vous avec vos informations d’identification.

1. Dans la barre de recherche bleue en haut de la page, entrez **Microsoft Sentinel**, puis sélectionnez **Microsoft Sentinel** dans les résultats de la recherche.

1. Dans la page Microsoft Sentinel, sélectionnez **Créer Microsoft Sentinel**.

1. Dans la page Ajouter Microsoft Sentinel à un espace de travail, sélectionnez **Créer un espace de travail**.

1. À partir de l’onglet de base de l’espace de travail Créer un journal d’analyses, saisissez les informations suivantes :
    1. Abonnement : conservez la valeur par défaut. Il s’agit de l’abonnement Azure fourni par l’hébergeur de labo autorisé (ALH).
    1. Groupe de ressources : sélectionnez **SC900-Sentinel-RG**. Si ce groupe de ressources n’est pas répertorié, créez-le en sélectionnant **En créer un nouveau**, entrez **SC900-Sentinel-RG**, puis sélectionnez **Ok**.
    1. Nom : **SC900-LogAnalytics-workspace**.
    1. Région : **USA Est** (une autre région par défaut peut être sélectionnée en fonction de votre emplacement)
    1. Sélectionnez **Vérifier + Créer** (aucune étiquette n’est configurée).
    1. Vérifiez les informations que vous avez saisies, puis sélectionnez **Créer**.
    1. Cela peut prendre une ou deux minutes avant que l’espace de travail n’apparaisse. Si vous ne le voyez toujours pas, sélectionnez **Actualiser**, puis **Ajouter**.

1. Une fois le nouvel espace de travail ajouté, la page Microsoft Sentinel | Actualités et guides s’affiche, indiquant que l’essai gratuit de Microsoft Sentinel est activé.  Sélectionnez **OK**.  Notez les trois étapes indiquées sur la page Mise en route.

1. Laissez cette page ouverte, car vous en aurez besoin pour la tâche suivante.

### Tâche 2

Une fois l’instance Microsoft Sentinel créée, il est important que les utilisateurs qui auront la responsabilité de prendre en charge Microsoft Sentinel disposent des autorisations nécessaires.  Pour cela, vous devez attribuer à l’utilisateur désigné les autorisations de rôle requises.  Dans cette tâche, vous allez afficher les rôles Microsoft Sentinel intégrés disponibles.

1. Dans la zone de recherche bleue, entrez **groupes de ressources**, puis sélectionnez **Groupes de ressources** dans les résultats de la recherche. 

1. Depuis la page des groupes de ressources, sélectionnez le groupe de ressources que vous avez créé avec Microsoft Sentinel, **SC900-Sentinel-RG**.  Le fait de travailler au niveau du groupe de ressources garantit que tout rôle sélectionné s’appliquera à toutes les ressources qui font partie de l’instance Microsoft Sentinel créée dans la tâche précédente.

1. Depuis la page SC900-Sentinel-RG, sélectionnez **Contrôle d’accès (IAM)** dans le volet de navigation à gauche.

1. Depuis la page Contrôle d’accès, sélectionnez **Afficher mon accès**.  Pour l’abonnement Azure qui vous est fourni par l’hébergeur de labo autorisé, un rôle a été défini pour vous permettre de gérer toutes les ressources nécessaires, comme indiqué dans la description. Toutefois, il est important de comprendre les rôles spécifiques à Sentinel disponibles.  Fermez la fenêtre des attributions en sélectionnant le **X** en haut à droite de l’écran.

1. Dans la page Contrôle d’accès, sélectionnez l’onglet **Rôles** en haut de la page.
    1. Dans la zone de recherche, entrez **Microsoft Sentinel** pour voir les rôles intégrés associés à Microsoft Sentinel.
    1. Dans l’un des rôles répertoriés, sélectionnez **afficher** pour afficher les détails de ce rôle.  Nous recommandons d’attribuer le privilège minimum nécessaire pour ce rôle.  
    1. Fermez la fenêtre en sélectionnant le **X** en haut à droite de la fenêtre.

1. Dans la page de contrôle d’accès, fermez la fenêtre en sélectionnant le **X** en haut à droite de la fenêtre.

1. Dans le coin supérieur gauche de la fenêtre, juste en dessous de la barre bleue où figure Microsoft Azure, sélectionnez **Accueil** pour revenir à la page d’accueil des services Azure.

1. Gardez l’onglet Azure ouvert dans votre navigateur.

### Tâche 3

L’objectif de cette tâche est de vous guider tout au long des étapes de la connexion à une source de données. De nombreux connecteurs de données sont déployés dans le cadre d’une solution Microsoft Sentinel avec du contenu associé comme des règles d’analyse, des classeurs et des guides opérationnels. Le hub de contenu Microsoft Sentinel est l’emplacement centralisé pour découvrir et gérer du contenu prêt à l’emploi (intégré). Cette étape consiste à utiliser le hub de contenu pour déployer la solution Microsoft Defender pour le cloud pour Microsoft Sentinel.  Cette solution vous permet d’ingérer des Alertes de sécurité signalées dans Microsoft Defender pour le cloud.

1. Dans la page d’accueil des services Azure, sélectionnez Microsoft Sentinel, puis l’instance que vous avez créée, **SC900-LogAnalytics-workspace**.

1. Dans le volet de navigation situé à gauche, sélectionnez **Hub de contenu**.

1. Prenez le temps de faire défiler les pages pour découvrir la longue liste des solutions disponibles et les options permettant de filtrer la liste.  Pour cette tâche, vous recherchez **Microsoft Defender pour le cloud**.  Sélectionnez-le dans la liste.  Dans la fenêtre latérale qui s’ouvre, lisez la description, puis sélectionnez **Installer**.  Cette solution comprend un connecteur de données et une règle d’analytique. L’installation peut prendre une minute.  Sélectionnez **Gérer**.

1. Cochez la case à côté de Microsoft Defender pour le cloud.  Une fenêtre s’ouvre à droite de la page.  Sélectionnez **Ouvrir la page du connecteur**.

1. Notez les instructions de configuration.  Cochez la case à côté du nom de l’abonnement, puis sélectionnez **Se connecter**.  Une fenêtre contextuelle peut s’afficher indiquant que seuls les abonnements sur lesquels vous disposez d’autorisations de Lecteur de sécurité commenceront à diffuser en continu les alertes de Microsoft Defender pour le cloud.  Sélectionnez **OK**.  L’état passera alors à connecté.  Le connecteur est maintenant activé, même si l’affichage du connecteur dans la page des connecteurs de données peut prendre un certain temps.  

1. Affichez maintenant des informations sur la règle d’analytique.  En haut de la page (dans la barre de navigation), sélectionnez **Microsoft Defender pour le cloud**. Désélectionnez la case à côté de Microsoft Defender pour le cloud, car vous avez déjà configuré le connecteur (la disparition de l’icône d’avertissement peut prendre un certain temps). Cochez la case à côté de la mention **Détecter l’activité de suppression CoreBackUp à partir des alertes de sécurité associées**. Dans la fenêtre qui s’ouvre, vous verrez des informations sur la règle et son rôle.  
    1. Bien que les détails de la logique de la règle dépassent la portée des principes de base, suivez les étapes de configuration de la règle afin d’afficher le type d’informations qui peuvent être configurées dans le cadre de la règle. Sélectionnez **Configuration**.
    1. Sélectionnez la règle **Détecter l’activité de suppression CoreBackUp à partir des alertes de sécurité associées**.
    1. Dans la fenêtre qui s’ouvre à droite de la page, sélectionnez **Créer une règle**.
    1. Parcourez chacune des pages de configuration, sélectionnez **Passez en revue et créer**, puis **Enregistrer**.

1. Revenez à la page Sentinel en sélectionnant **Microsoft Sentinel | Hub de contenu** à partir de la barre de navigation en haut de la page, au-dessus de la mention « Règles d’analyse ».

1. Laissez cette page ouverte, car vous en aurez besoin pour la tâche suivante.


### Tâche 4

Dans cette tâche, vous allez parcourir certaines des options disponibles dans Sentinel.

1. Dans le volet de navigation gauche, sélectionnez **Hunting** (Repérage).  En haut de la page, sélectionnez l’onglet **Requêtes**. Lisez la description de ce qu’est une requête de repérage. Les requêtes de repérage peuvent être ajoutées via le hub de contenu. Toutes les requêtes précédemment installées sont répertoriées ici. Sélectionnez **Accéder au hub de contenu**.  Le hub de contenu répertorie le contenu qui inclut des requêtes dans le cadre d’une solution ou en tant que requête autonome.  Faites défiler vers le bas pour afficher les options disponibles. Fermez le hub de contenu en sélectionnant le **X** en haut à droite de la fenêtre.

1. Dans le volet de navigation de gauche, sélectionnez **MITRE ATT&CK**.  MITRE ATT&CK est un base de connaissances accessible publiquement regroupant les tactiques et les techniques couramment utilisées par les attaquants. Avec Microsoft Sentinel vous pouvez afficher les détections déjà actives dans votre espace de travail, et celles que vous pouvez configurer, afin de comprendre la couverture de sécurité de votre organisation, en fonction des tactiques et des techniques issues du framework MITRE ATT&CK®.  Sélectionnez une cellule dans la matrice et notez les informations disponibles sur le côté droit de l’écran. **Remarque** : Vous devrez peut-être sélectionner le bouton « **<<**  » à l’extrême droite de la fenêtre pour afficher le panneau d’informations.

1. Dans le volet de navigation situé à gauche, sélectionnez **Communauté**. Les analystes de sécurité Microsoft créent et ajoutent constamment de nouveaux workbooks, de nouveaux playbooks, de nouvelles requêtes de chasse, entre autres, et les publient dans la communauté pour vous permettre de les utiliser dans votre environnement. Sur le côté droit de l’écran, sélectionnez **Intégrer le contenu de la communauté**.  Un nouvel onglet dans le référentiel GitHub s’ouvre où vous pouvez télécharger du contenu pour activer vos scénarios. Faites défiler jusqu’à la section README.md et passez en revue la description. Revenez à l’onglet Azure dans votre navigateur.

1. Dans le volet de navigation à gauche, sélectionnez **Analyse**.  Il devrait y avoir deux règles actives, une qui est disponible par défaut et la règle que vous avez créée dans la tâche précédente. Sélectionnez la règle par défaut **Détection avancée des attaques en plusieurs étapes**.  Notez les informations détaillées.  Microsoft Sentinel utilise Fusion, un moteur de corrélation basé sur des algorithmes évolutifs d’apprentissage automatique pour détecter automatiquement des attaques multiphases (également appelées menaces persistantes avancées) en identifiant des combinaisons de comportements anormaux et d’activités suspectes observés à différents stades de la chaîne de destruction. Sur la base de ces découvertes, Microsoft Sentinel génère des incidents qui seraient autrement difficiles à intercepter. **Remarque** : Vous devrez peut-être sélectionner le bouton « **<<**  » à l’extrême droite de la fenêtre pour afficher le panneau d’informations.

1. Dans le volet de navigation à gauche, sélectionnez **Automatisation**.  Ici, vous pouvez créer des règles d’automatisation simples, intégrer des playbooks existants ou créer des playbooks.  Sélectionnez **+ Créer**, puis **Règle d’automatisation**.  Notez la fenêtre qui s’ouvre sur le côté droit de l’écran et les options disponibles pour créer des conditions et des actions.  Sélectionnez **Annuler** en bas de l’écran.

1. Dans le volet de navigation à gauche, sélectionnez **Classeurs**. Lisez la description de ce qu’est un classeur Microsoft Sentinel.  Les classeurs peuvent être ajoutés via le hub de contenu. Tous les classeurs précédemment installés sont répertoriés ici. Sélectionnez **Accéder au hub de contenu**.  Le hub de contenu répertorie le contenu qui inclut des classeurs, soit en tant que partie d’une solution, soit en tant que classeur autonome. Faites défiler vers le bas pour afficher les options disponibles.

1. Fermez la fenêtre en sélectionnant le **X** en haut à droite de la fenêtre.

1. Dans le coin supérieur gauche de la fenêtre, juste en dessous de la barre bleue, sélectionnez **Accueil** pour revenir à la page d’accueil du portail Azure.

1. Déconnectez-vous et fermez tous les onglets ouverts du navigateur.

### Révision

Dans cette lV, vous avez parcouru les étapes de connexion de Microsoft Sentinel à des sources de données, vous avez configuré un classeur et vous avez parcouru plusieurs options disponibles dans Microsoft Sentinel.
