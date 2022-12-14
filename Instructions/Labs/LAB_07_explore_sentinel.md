<a name="---"></a><!---
---
Labo : Titre : « Explorer Microsoft Sentinel » Parcours d’apprentissage/Module/Titre : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft ; Module 3 : Décrire les fonctionnalités de sécurité de Microsoft Sentinel ; Unité 3 : Décrire la façon dont Microsoft Sentinel fournit une gestion des menaces intégrée »
---
--->

# <a name="lab-explore-microsoft-sentinel"></a>Labo : Explorer Microsoft Sentinel

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft
- Module : Décrire les fonctionnalités de sécurité de Microsoft Sentinel
- Unité : Décrire la façon dont Microsoft Sentinel fournit une gestion des menaces intégrée

## <a name="lab-scenario"></a>Scénario du labo

Vous allez présenter le processus de création d’une instance Microsoft Sentinel.  Vous définirez également les autorisations afin de garantir l’accès aux ressources qui seront déployées pour prendre en charge Microsoft Sentinel.  Une fois cette configuration de base effectuée, vous suivrez les étapes de connexion de Microsoft Sentinel à vos sources de données, configurerez un classeur et présenterez brièvement certaines des fonctionnalités clés disponibles dans Microsoft Sentinel. 

**Durée estimée** : 45-60 minutes

### <a name="task-1"></a>Tâche 1

Créer une instance Microsoft Sentinel

1. Ouvrez Microsoft Edge. Dans la barre d’adresse, entrez **portal.azure.com**.
1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez le nom d’utilisateur fourni par votre fournisseur d’hébergement de labo, puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Dans la barre de recherche bleue en haut de la page, entrez **Microsoft Sentinel**, puis sélectionnez **Microsoft Sentinel** dans les résultats de la recherche.

1. Dans la page Microsoft Sentinel, sélectionnez **Créer Microsoft Sentinel**.

1. Dans la page Ajouter Microsoft Sentinel à un espace de travail, sélectionnez **Créer un espace de travail**.

1. À partir de l’onglet de base de l’espace de travail Créer un journal d’analyses, saisissez les informations suivantes :
    1. Abonnement : conservez la valeur par défaut. Il s’agit de l’abonnement Azure fourni par l’hébergeur de labo autorisé (ALH).
    1. Groupe de ressources : sélectionnez **Créer un nouveau**, puis saisissez le nom **SC900-Sentinel-RG** et sélectionnez **OK**.
    1. Nom : **SC900-LogAnalytics-workspace**.
    1. Région : **USA Est** (une autre région par défaut peut être sélectionnée en fonction de votre emplacement)
    1. Sélectionnez **Vérifier + Créer** (aucune étiquette n’est configurée).
    1. Vérifiez les informations que vous avez saisies, puis sélectionnez **Créer**.
    1. Cela peut prendre une ou deux minutes avant que l’espace de travail n’apparaisse. Si vous ne le voyez toujours pas, sélectionnez **Actualiser**, puis **Ajouter**.

1. Une fois le nouvel espace de travail ajouté, la page Microsoft Sentinel | Actualités et guides s’affiche, indiquant que l’essai gratuit de Microsoft Sentinel est activé.  Sélectionnez **OK**.  Notez les trois étapes indiquées sur la page Mise en route.

1. Laissez cette page ouverte, car vous en aurez besoin pour la tâche suivante.

### <a name="task-2"></a>Tâche 2

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

### <a name="task-3"></a>Tâche 3

L’objectif de cette tâche est de vous guider tout au long des étapes nécessaires à la configuration d’un connecteur de données à votre instance de Microsoft Sentinel et à la sélection d’un modèle de classeur intégré pour vous permettre d’obtenir rapidement des insights sur vos données dès que vous connectez une source de données. REMARQUE : Les abonnements aux labos Azure peuvent rencontrer des délais plus longs qu’à l’accoutumée lors de la connexion à une source de données et/ou de la visualisation des données.

1. Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **Sentinel** puis sélectionnez **Microsoft Sentinel** à partir des résultats de la recherche.

1. Depuis la page Microsoft Sentinel, sélectionnez l’espace de travail que vous avez créé avec l’instance de Microsoft Sentinel, **SC900-LogAnalytics-workspace**.

1. La première étape avec Microsoft Sentinel consiste à pouvoir collecter des données. Dans le volet de navigation à gauche, sélectionnez **Connecteurs de données**, qui se trouve sous configuration.

1. Depuis la page Connecteurs de données, sur la page principale, faites défiler vers le bas pour afficher la liste étendue des connecteurs disponibles. Dans la zone de recherche de la page des connecteurs de données, entrez **Microsoft Defender pour le cloud**, puis dans la liste, sélectionnez **Microsoft Defender pour le cloud**.

1. La fenêtre du connecteur Microsoft Defender pour le cloud s’ouvre. Passez en revue la description, puis sélectionnez **Ouvrir la page du connecteur**.

1. Dans la page du connecteur Microsoft Defender pour le cloud, passez en revue la description sur le côté gauche de la fenêtre.

1. L’onglet Instructions de la fenêtre principale fournit les prérequis.  Passez en revue les instructions et les informations de configuration.
    1. Dans la section de configuration, sélectionnez la zone vide en regard de l’abonnement listé, **MOC Subscription--lodXXXXXXXX**, pour faire apparaître une coche dans une zone bleue, puis sélectionnez **Se connecter** (l’option de connexion s’affiche au-dessus de la zone de recherche).  Dans la fenêtre de connexion qui s’affiche, sélectionnez **OK**.  La colonne de l’état, en regard de l’abonnement, doit désormais indiquer Connecté.  Ne vous inquiétez pas si vous ne voyez pas l’état Connecté dans la fenêtre à gauche de la page. N’actualisez PAS le navigateur.
    1. Faites défiler la page et sélectionnez **Activer** pour créer automatiquement des incidents à partir de toutes les alertes générées dans le service connecté.
    1. Sélectionnez maintenant l’onglet **Étapes suivantes** en haut de la page pour voir les classeurs recommandés pour ce connecteur de données.  Microsoft Sentinel est fourni avec des modèles de classeurs intégrés qui vous permettent d’obtenir rapidement des insights sur vos données dès que vous connectez une source de données.
    1. Sélectionnez **Conformité et protection ASC** (Remarque : ASC ou Azure Security Center s’appelle désormais Microsoft Defender pour le cloud).  La page des classeurs s’ouvre.  Sur le côté droit de l’écran, passez en revue la description, sélectionnez **Enregistrer** en bas de l’écran, puis sélectionnez **OK** pour enregistrer le classeur à l’emplacement par défaut.  À présent, sélectionnez **Afficher le classeur enregistré**.
    1. Dans le champ de l’espace de travail, sélectionnez **SC900-LogAnalytics-workspace**.
    1. En haut de la page du classeur, sélectionnez **Actualisation automatique : désactivée**, puis sélectionnez **5 minutes** et **Appliquer**.
    1. En haut de la page du classeur, sélectionnez l’**icône Enregistrer**.
    1. En haut à gauche de la page Classeurs, au-dessus de Classeurs, sélectionnez **Microsoft Sentinel**. Cette opération vous renvoie à la page Vue d’ensemble. Vous devriez maintenant voir le chiffre 1 au-dessus de la mention Connecté, ce qui indique qu’un connecteur est actif (vous devrez peut-être sélectionner Actualiser).

1. Laissez cette page ouverte, car vous en aurez besoin pour la tâche suivante.

### <a name="task-4"></a>Tâche 4

Dans cette tâche, vous allez parcourir certaines des options disponibles dans Sentinel.

1. Dans le volet de navigation gauche, sélectionnez **Hunting** (Repérage).  Sous l’onglet **requêtes**, qui est sélectionné (souligné), sélectionnez une requête dans la liste.  Une fois qu’une requête est sélectionnée, notez les informations fournies sur cette requête, notamment le code de la requête ainsi que l’option permettant d’exécuter la requête et d’afficher les résultats.  Ne sélectionnez rien.

1. Dans le volet de navigation de gauche, sélectionnez **MITRE ATT&CK**.  MITRE ATT&CK est un base de connaissances accessible publiquement regroupant les tactiques et les techniques couramment utilisées par les attaquants. Avec Microsoft Sentinel vous pouvez afficher les détections déjà actives dans votre espace de travail, et celles que vous pouvez configurer, afin de comprendre la couverture de sécurité de votre organisation, en fonction des tactiques et des techniques issues du framework MITRE ATT&CK®.  Sélectionnez une cellule dans la matrice et notez les informations disponibles sur le côté droit de l’écran.  

1. Dans le volet de navigation situé à gauche, sélectionnez **Communauté**. Les analystes de sécurité Microsoft créent et ajoutent constamment de nouveaux workbooks, de nouveaux playbooks, de nouvelles requêtes de chasse, entre autres, et les publient dans la communauté pour vous permettre de les utiliser dans votre environnement. Sur le côté droit de l’écran, sélectionnez **Intégrer le contenu de la communauté**.  Un nouvel onglet dans le référentiel GitHub s’ouvre où vous pouvez télécharger du contenu pour activer vos scénarios. Faites défiler jusqu’à la section README.md et passez en revue la description. Revenez à l’onglet Azure dans votre navigateur.

1. Dans le volet de navigation à gauche, sélectionnez **Analyse**.  Sélectionnez le premier élément dans la liste **Détection avancée des attaques multiphases**.  Notez les informations détaillées.  Microsoft Sentinel utilise Fusion, un moteur de corrélation basé sur des algorithmes évolutifs d’apprentissage automatique pour détecter automatiquement des attaques multiphases (également appelées menaces persistantes avancées) en identifiant des combinaisons de comportements anormaux et d’activités suspectes observés à différents stades de la chaîne de destruction. Sur la base de ces découvertes, Microsoft Sentinel génère des incidents qui seraient autrement difficiles à intercepter.

1. Dans le volet de navigation à gauche, sélectionnez **Automatisation**.  Ici, vous pouvez créer des règles d’automatisation simples, intégrer des playbooks existants ou créer des playbooks.  Sélectionnez **+ Créer**, puis **Règle d’automatisation**.  Notez la fenêtre qui s’ouvre sur le côté droit de l’écran et les options disponibles pour créer des conditions et des actions.  Sélectionnez **Annuler** en bas de l’écran.

1. Dans le volet de navigation à gauche, sélectionnez **Classeurs**. Depuis la page Classeurs, sélectionnez l’onglet **Mes classeurs** qui se trouve au-dessus de la barre de recherche.  Le classeur que vous avez enregistré plus tôt est répertorié et disponible pour que vous puissiez visualiser et contrôler vos données.   REMARQUE : Il n’y a pas d’activité réelle dans l’abonnement Azure à refléter dans le classeur et les abonnements aux labos Azure peuvent rencontrer des délais plus longs qu’à l’accoutumée lors de la collecte des données pouvant être visualisées dans le classeur.

1. Fermez la fenêtre en sélectionnant le **X** en haut à droite de la fenêtre.

1. Dans le coin supérieur gauche de la fenêtre, juste en dessous de la barre bleue, sélectionnez **Accueil** pour revenir à la page d’accueil du portail Azure.

1. Fermez tous les onglets ouverts du navigateur.

### <a name="review"></a>Révision

Dans cette démonstration, vous avez parcouru les étapes de connexion de Microsoft Sentinel à des sources de données, configuré un classeur et parcouru plusieurs options disponibles dans Microsoft Sentinel.
