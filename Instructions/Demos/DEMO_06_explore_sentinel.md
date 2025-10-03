<!---
---
Démonstration : Titre : « Microsoft Sentinel » Parcours d’apprentissage/Module/Titre : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft ; Module 3 : Décrire les fonctionnalités de sécurité de Microsoft Sentinel ; Unité 3 : Décrire les fonctionnalités de détection et d’atténuation des menaces dans Microsoft Sentinel »
---
--->

# Démo : Microsoft Sentinel

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft
- Module : Décrire les fonctionnalités de sécurité de Microsoft Sentinel
- Unité : Décrire les fonctionnalités de détection et d’atténuation des menaces dans Microsoft Sentinel

## Scénario de démonstration

Dans cette démonstration, vous allez passer en revue certaines des options disponibles avec Microsoft Sentinel, notamment l’utilisation du hub de contenu pour trouver des solutions empaquetées que vous pouvez déployer.  Tout d’abord, vous allez examiner le processus de configuration des autorisations de contrôle d’accès en fonction du rôle pour les utilisateurs qui auraient besoin d’accéder à vos ressources Microsoft Sentinel.

### Partie 1 de la démonstration

Une instance de Microsoft Sentinel doit déjà avoir été créée dans le cadre de la configuration de la préversion. Vérifiez qu’elle a été créée.

1. Ouvrez l’onglet du navigateur, **Accueil - Microsoft Azure**.  Si vous avez fermé l’onglet, ouvrez une page du navigateur et saisissez **https://portal.azure.com** dans la barre d’adresse. Connectez-vous avec les informations d’identification Azure fournies par l’hôte de laboratoire autorisé (ALH).  Cela vous amène à la page d’accueil des services Azure.

1. Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **Sentinel** puis sélectionnez **Microsoft Sentinel** à partir des résultats de la recherche.  

1. Sur la page Microsoft Sentinel, vous devriez voir un espace de travail Log Analytics répertorié.  Cela indique qu’une instance de Microsoft Sentinel a été créée et qu’un espace de travail Log Analytics y a été ajouté. Si ce n’est pas le cas, suivez les étapes ci-dessous.
    1. Dans la zone de recherche bleue en haut de la page, entrez **Log Analytics** et sélectionnez-le dans les résultats de recherche.
1. Sélectionnez **+ Créer**.
1. Dans l’onglet Informations de base de la création d’espace de travail Log Analytics, saisissez les informations suivantes :
    1. Abonnement : conservez la valeur par défaut. Il s’agit de l’abonnement Azure fourni par l’hébergeur de labo autorisé (ALH).
    1. Groupe de ressources : sélectionnez **SC900-Sentinel-RG**. Si ce groupe de ressources n’est pas répertorié, créez-le en sélectionnant **En créer un nouveau**, entrez **SC900-Sentinel-RG**, puis sélectionnez **Ok**.
    1. Nom : **SC900-Sentinel-workspace**.
    1. Région : **USA Est** (une autre région par défaut peut être sélectionnée en fonction de votre emplacement)
    1. Sélectionnez **Vérifier + Créer** (aucune étiquette n’est configurée).
    1. Vérifiez les informations saisies, puis sélectionnez **Créer**.
    1. La création du nouvel espace de travail peut prendre une à deux minutes.
    1. Une fois créé, sélectionnez **Accéder à la ressource** pour afficher les informations relatives à l’espace de travail.
1. À ce stade, l’instance de Microsoft Sentinel n’a pas encore été créée. Pour créer une instance de Sentinel, vous devez vous rendre sur la page Microsoft Sentinel. Utilisez la barre de recherche bleue en haut de la page pour rechercher **Microsoft Sentinel** et sélectionnez-le dans les résultats de recherche.
1. Pour ajouter l’espace de travail à Microsoft Sentinel, vous devez vous rendre sur la page Microsoft Sentinel. Utilisez la barre de recherche bleue en haut de la page pour rechercher **Microsoft Sentinel**
    1. Depuis la page Microsoft Sentinel, sélectionnez **+ Créer**.
    1. Vous pouvez maintenant ajouter l’espace de travail que vous venez de créer. Sélectionnez **SC900-Sentinel-workspace**, puis sélectionnez **Ajouter**.  Cela peut prendre quelques minutes, le temps que l’essai gratuit de Microsoft Sentinel s’active.  Une fois l’activation terminée, sélectionnez **Ok**.


1. Laissez cette page ouverte, car vous en aurez besoin pour la prochaine tâche.

### Partie 2 de la démonstration

Comme pour toutes les ressources Azure, vous voulez vous assurer que les utilisateurs disposent des autorisations appropriées pour accéder à vos ressources Microsoft Sentinel. Ici, vous allez afficher les étapes d’attribution d’un rôle et les rôles disponibles à utiliser avec Microsoft Sentinel.  

1. Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **Groupe de ressources** puis sélectionnez **Groupe de ressources** à partir des résultats de la recherche. Assigner le rôle pour le niveau de groupe de ressources garantira que le rôle s’applique à toutes les ressources qui sont déployées pour prendre en charge Microsoft Sentinel.

1. Depuis la page des groupes de ressources, sélectionnez le groupe de ressources que vous avez créé avec Microsoft Sentinel, **SC900-Sentinel-RG**.

1. Sur la page SC900-Sentinel-RG, sélectionnez **Contrôle d’accès (IAM)** dans le volet de navigation de gauche.

1. Sur la page contrôle d’accès, sélectionnez **Afficher mon accès**.  Vous verrez probablement une attribution de rôle personnalisé déjà configurée pour cet abonnement et les autorisations nécessaires vous seront accordées.  Ce rôle personnalisé aurait été configuré par l’hébergeur de labo autorisé (HLA) fournissant l’environnement de labo. Toutefois, à des fins de démonstration, il est recommandé d’afficher les rôles spécifiques à Sentinel.  Fermez la fenêtre des attributions en sélectionnant le **X** en haut à droite de l’écran.

    1. Sélectionnez **+ Ajouter**, puis **Ajouter une affectation de rôle** sur la page Contrôle d’accès.

    1. La fenêtre Ajouter une affectation de rôle s’ouvre.  Dans la barre de recherche, saisissez **Microsoft Sentinel** pour afficher les rôles associés à Microsoft Sentinel.
    1. Dans l’un des rôles répertoriés, sélectionnez **afficher** pour afficher les détails de ce rôle.  Nous vous recommandons d’affecter le moins de privilèges possible au rôle.  

    1. Fermez la fenêtre en sélectionnant le **X** en haut à droite de la fenêtre.

1. Dans la page de contrôle d’accès, fermez la fenêtre en sélectionnant le **X** en haut à droite de la fenêtre.

1. En haut à gauche de la fenêtre, juste en dessous de la barre bleue qui indique Microsoft Azure, sélectionnez **Accueil** pour revenir à la page d’accueil des services Azure.

1. Gardez l’onglet Azure ouvert dans votre navigateur.

### Partie 3 de la démonstration

Dans cette partie de la démonstration, vous allez examiner les étapes de la connexion à une source de données. De nombreux connecteurs de données sont déployés dans le cadre d’une solution Microsoft Sentinel avec du contenu associé comme des règles d’analyse, des classeurs et des guides opérationnels. Le hub de contenu Microsoft Sentinel est l’emplacement centralisé pour découvrir et gérer du contenu prêt à l’emploi (intégré). Cette étape consiste à utiliser le hub de contenu pour déployer la solution Microsoft Defender pour le cloud pour Microsoft Sentinel.  Cette solution vous permet d’ingérer des Alertes de sécurité signalées dans Microsoft Defender pour le cloud.

1. Depuis la page d’accueil des services Azure, sélectionnez Microsoft Sentinel, puis sélectionnez l’instance que vous avez créée, **SC900-Sentinel-workspace**.

1. Dans le volet de navigation gauche, développez **Gestion de contenu**, puis sélectionnez **Hub de contenu**.

1. Prenez le temps de faire défiler les pages pour découvrir la longue liste des solutions disponibles et les options permettant de filtrer la liste.  Pour cette tâche, vous recherchez **Microsoft Defender pour le cloud**.  Sélectionnez-le dans la liste.  Dans la fenêtre latérale qui s’ouvre, lisez la description, puis sélectionnez **Installer**.  Une fois l’installation terminée, la colonne d’état dans la fenêtre principale s’affiche comme étant installée.

1. Sur le côté droit de la page Microsoft Defender pour le cloud se situe la description et les notes associées à la solution à partir du Hub de contenu et ce qui est inclus dans cette solution.  Dans la fenêtre principale, vous trouverez les composants de la solution.  Dans ce cas, il existe deux connecteurs de données et une règle de données. Le triangle orange indique qu’une configuration est nécessaire. Cochez la case à côté de **Microsoft Defender pour le cloud basé sur l’abonnement (hérité)**.  Une fenêtre s’ouvre à droite de la page.  Sélectionnez **Ouvrir la page du connecteur**.

1. Notez les instructions de configuration.  Cochez la case à côté du nom de l’abonnement, puis sélectionnez **Se connecter**.  L’état passera alors à « connecté ».  Le connecteur est maintenant activé, même si l’affichage du connecteur dans la page des connecteurs de données peut prendre un certain temps.  

1. Affichez maintenant des informations sur la règle d’analytique.  En haut de la page (dans la barre de navigation), sélectionnez **Microsoft Defender pour le cloud**. Désélectionnez la case à côté de Microsoft Defender pour le cloud, car vous avez déjà configuré le connecteur (la disparition de l’icône d’avertissement peut prendre un certain temps). Cochez la case à côté de la mention **Détecter l’activité de suppression CoreBackUp à partir des alertes de sécurité associées**.  La page Règles d’analyse s’affiche.  Sélectionnez à nouveau la règle **Détecter l’activité de suppression CoreBackUp à partir des alertes de sécurité associées**. Fenêtre s’ouvrant à droite qui fournit des informations sur la règle et ce qu’elle effectue.  Sélectionnez **Créer une règle**.  
    1. Bien que les détails de la logique de règle dépassent l’étendue des principes de base, suivez chaque onglet dans la création de règle afin d’afficher le type d’informations qui peut être configuré
    1. Quand vous atteignez l’onglet Vérifier + créer, sélectionnez **Enregistrer**.

1. Revenez à la page Sentinel en sélectionnant **Microsoft Sentinel | Hub de contenu** à partir de la barre de navigation en haut de la page, au-dessus de la mention « Règles d’analyse ».

1. Notez qu’à l’aide du hub de contenu, une solution peut être facilement et rapidement déployée.

1. Laissez cette page ouverte, car vous en aurez besoin pour la tâche suivante.

### Partie 4 de la démonstration

Dans cette partie de la démonstration, vous allez examiner certaines des options disponibles dans Sentinel.

1. Dans le volet de navigation gauche, sélectionnez **Hunting** (Repérage).  En haut de la page, sélectionnez l’onglet **requêtes**. Lisez la description de ce qu’est une requête de repérage. Les requêtes de repérage peuvent être ajoutées via le hub de contenu. Toutes les requêtes précédemment installées sont répertoriées ici. Sélectionnez **Accéder au hub de contenu**.  Le hub de contenu répertorie le contenu qui inclut des requêtes dans le cadre d’une solution ou en tant que requête autonome.  Faites défiler vers le bas pour afficher les options disponibles.

1. Dans le volet de navigation de gauche, sélectionnez **MITRE ATT&CK**.  MITRE ATT&CK est un base de connaissances accessible publiquement regroupant les tactiques et les techniques couramment utilisées par les attaquants. Avec Microsoft Sentinel vous pouvez afficher les détections déjà actives dans votre espace de travail, et celles que vous pouvez configurer, afin de comprendre la couverture de sécurité de votre organisation, en fonction des tactiques et des techniques issues du framework MITRE ATT&CK®.  Sélectionnez une cellule dans la matrice et notez les informations disponibles sur le côté droit de l’écran.  

1. Dans le volet de navigation situé à gauche, sélectionnez **Communauté**. La page de la communauté comprend des insights et des mises à jour de cybersécurité de Microsoft Research, un lien vers une liste de blogs Microsoft Sentinel, un lien vers les forums Microsoft Sentinel, des liens vers les dernières éditions du Hub Microsoft Sentinel et bien plus encore. Explorer ceci à volonté.

1. Dans le volet de navigation de gauche, sélectionnez **Analyse**.  Il devrait y avoir deux règles actives, une qui est disponible par défaut et la règle que vous avez créée dans la tâche précédente. Sélectionnez la règle par défaut **Détection avancée des attaques en plusieurs étapes**.  Notez les informations détaillées.  Microsoft Sentinel utilise Fusion, un moteur de corrélation basé sur des algorithmes évolutifs d’apprentissage automatique pour détecter automatiquement des attaques multiphases (également appelées menaces persistantes avancées) en identifiant des combinaisons de comportements anormaux et d’activités suspectes observés à différents stades de la chaîne de destruction. Sur la base de ces découvertes, Microsoft Sentinel génère des incidents qui seraient autrement difficiles à intercepter.

1. Dans le volet de navigation de gauche, sélectionnez **Automation**.  Ici, vous pouvez créer des règles d’automatisation simples, intégrer des playbooks existants ou créer des playbooks.  Sélectionnez **+ Créer**, puis **Règle d’automatisation**.  Notez la fenêtre qui s’ouvre sur le côté droit de l’écran et les options disponibles pour créer des conditions et des actions.  Sélectionnez **Annuler** en bas de l’écran.

1. Dans le volet de navigation de gauche, sélectionnez **Classeur**. Lisez la description du classeur Microsoft Sentinel.  Les classeurs peuvent être ajoutés via le hub de contenu. Tous les classeurs précédemment installés sont répertoriés ici. Sélectionnez **Accéder au hub de contenu**.  Le hub de contenu répertorie le contenu qui inclut des classeurs, soit en tant que partie d’une solution, soit en tant que classeur autonome. Faites défiler vers le bas pour afficher les options disponibles.

1. Fermez la fenêtre en sélectionnant le **X** en haut à droite de la fenêtre.

1. Dans le coin supérieur gauche de la fenêtre, juste en dessous de la barre bleue, sélectionnez **Accueil** pour revenir à la page d’accueil du portail Azure.  

### Révision

Dans cette démonstration, vous avez exploré les étapes de connexion de Microsoft Sentinel à des sources de données, configuré un workbook et examiné plusieurs options disponibles dans Microsoft Sentinel.
