---
lab:
  title: "Explorer Microsoft\_Sentinel"
  module: Describe the security capabilities of Microsoft Sentinel
---

# Labo : Explorer Microsoft Sentinel

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft
- Module : Décrire les fonctionnalités de sécurité de Microsoft Sentinel
- Unité : Décrire les fonctionnalités de détection et d’atténuation des menaces dans Microsoft Sentinel

## Scénario de labo

Dans ce labo, vous allez découvrir le processus de création d’une instance Microsoft Sentinel.  Vous définirez également les autorisations afin de garantir l’accès aux ressources qui seront déployées pour prendre en charge Microsoft Sentinel.  Une fois cette configuration de base effectuée, vous suivrez les étapes de connexion de Microsoft Sentinel à vos sources de données, configurerez un classeur et présenterez brièvement certaines des fonctionnalités clés disponibles dans Microsoft Sentinel.

**Durée estimée :** 60 minutes

### Tâche 1

Pour créer une instance de Microsoft Sentinel, vous devez d’abord créer un espace de travail Log Analytics, utilisé pour stocker les données de Microsoft Sentinel.  Une fois que vous disposez d’un espace de travail Log Analytics, vous pouvez créer une instance Microsoft Sentinel et y ajouter l’espace de travail Log Analytics.  Dans cette tâche, vous allez suivre chacune de ces étapes.

1. Vous devriez être sur la page d’accueil des services Azure.  Si ce n’est pas le cas, ouvrez Microsoft Edge et, dans la barre d’adresse, entrez **portal.azure.com**, puis connectez-vous avec vos informations d’identification d’administrateur du portail Azure.

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
1. Laissez cette page ouverte, car vous en aurez besoin pour la tâche suivante.

### Tâche 2

Une fois l’instance Microsoft Sentinel créée et l’espace de travail Log Analytics qui lui est associé attribué, il est important que les utilisateurs responsables du support de Microsoft Sentinel disposent des autorisations nécessaires.  Pour cela, vous devez attribuer à l’utilisateur désigné les autorisations de rôle requises.  Dans cette tâche, vous allez afficher les rôles Microsoft Sentinel intégrés disponibles.

1. Dans la zone de recherche bleue, entrez **groupes de ressources**, puis sélectionnez **Groupes de ressources** dans les résultats de la recherche. 

1. Depuis la page des groupes de ressources, sélectionnez le groupe de ressources que vous avez créé avec Microsoft Sentinel, **SC900-Sentinel-RG**.  Le fait de travailler au niveau du groupe de ressources garantit que tout rôle sélectionné s’appliquera à toutes les ressources qui font partie de l’instance Microsoft Sentinel créée dans la tâche précédente.

1. Sur la page SC900-Sentinel-RG, sélectionnez **Contrôle d’accès (IAM)** dans le volet de navigation de gauche.

1. Sur la page contrôle d’accès, sélectionnez **Afficher mon accès**.  Pour l’abonnement Azure qui vous est fourni par l’hébergeur de labo autorisé, un rôle a été défini pour vous permettre de gérer toutes les ressources nécessaires, comme indiqué dans la description. Toutefois, il est important de comprendre les rôles spécifiques à Sentinel disponibles.  Fermez la fenêtre des attributions en sélectionnant le **X** en haut à droite de l’écran.

1. Dans la page Contrôle d’accès, sélectionnez l’onglet **Rôles** en haut de la page.
    1. Dans la zone de recherche, entrez **Microsoft Sentinel** pour voir les rôles intégrés associés à Microsoft Sentinel.
    1. Dans l’un des rôles répertoriés, sélectionnez **afficher** pour afficher les détails de ce rôle.  Nous vous recommandons d’affecter le moins de privilèges possible au rôle.  
    1. Fermez la fenêtre en sélectionnant le **X** en haut à droite de la fenêtre.

1. Dans la page de contrôle d’accès, fermez la fenêtre en sélectionnant le **X** en haut à droite de la fenêtre.

1. En haut à gauche de la fenêtre, juste en dessous de la barre bleue qui indique Microsoft Azure, sélectionnez **Accueil** pour revenir à la page d’accueil des services Azure.

1. Gardez l’onglet Azure ouvert dans votre navigateur.

### Tâche 3

L’objectif de cette tâche est de vous guider tout au long des étapes de la connexion à une source de données. De nombreux connecteurs de données sont déployés dans le cadre d’une solution Microsoft Sentinel avec du contenu associé comme des règles d’analyse, des classeurs et des guides opérationnels. Le hub de contenu Microsoft Sentinel est l’emplacement centralisé pour découvrir et gérer du contenu prêt à l’emploi (intégré). Cette étape consiste à utiliser le hub de contenu pour déployer la solution Microsoft Defender pour le cloud pour Microsoft Sentinel.  Cette solution vous permet d’ingérer des Alertes de sécurité signalées dans Microsoft Defender pour le cloud.

1. Depuis la page d’accueil des services Azure, sélectionnez Microsoft Sentinel, puis sélectionnez l’instance que vous avez créée, **SC900-Sentinel-workspace**.

1. Dans le volet de navigation gauche, développez **Gestion de contenu**, puis sélectionnez **Hub de contenu**.

1. Prenez le temps de faire défiler les pages pour découvrir la longue liste des solutions disponibles et les options permettant de filtrer la liste.  Pour cette tâche, vous recherchez **Microsoft Defender pour le cloud**.  Sélectionnez-le dans la liste.  Dans la fenêtre latérale qui s’ouvre, lisez la description, puis sélectionnez **Installer**.  Une fois l’installation terminée, la colonne d’état dans la fenêtre principale s’affiche comme étant installée.

1. Une fois de plus, sélectionnez **Microsoft Defender pour le cloud** dans la liste. Dans la fenêtre à droite, sélectionnez **Gérer**.

1. Sur le côté droit de la page Microsoft Defender pour le cloud se situe la description et les notes associées à la solution à partir du Hub de contenu et ce qui est inclus dans cette solution.  Dans la fenêtre principale, vous trouverez les composants de la solution.  Dans ce cas, il existe deux connecteurs de données et une règle de données. Le triangle orange indique qu’une configuration est nécessaire. Cochez la case à côté de **Microsoft Defender pour le cloud basé sur l’abonnement (hérité)**.  Une fenêtre s’ouvre à droite de la page.  Sélectionnez **Ouvrir la page du connecteur**.

1. Notez les instructions de configuration.  Cochez la case à côté du nom de l’abonnement, puis sélectionnez **Se connecter**.  Une fenêtre contextuelle peut s’afficher indiquant que seuls les abonnements sur lesquels vous disposez d’autorisations de Lecteur de sécurité commenceront à diffuser en continu les alertes de Microsoft Defender pour le cloud.  Cliquez sur **OK**.  L’état passera alors à connecté.  Le connecteur est maintenant activé, même si l’affichage du connecteur dans la page des connecteurs de données peut prendre un certain temps.  

1. Affichez maintenant des informations sur la règle d’analytique.  En haut de la page (dans la barre de navigation), sélectionnez **Microsoft Defender pour le cloud**. Désélectionnez la case à côté de Microsoft Defender pour le cloud, car vous avez déjà configuré le connecteur (la disparition de l’icône d’avertissement peut prendre un certain temps). Cochez la case à côté de la mention **Détecter l’activité de suppression CoreBackUp à partir des alertes de sécurité associées**.  La page Règles d’analyse s’affiche.  Sélectionnez à nouveau la règle **Détecter l’activité de suppression CoreBackUp à partir des alertes de sécurité associées**. Fenêtre s’ouvrant à droite qui fournit des informations sur la règle et ce qu’elle effectue.  Sélectionnez **Créer une règle**.  
    1. Bien que les détails de la logique de règle dépassent l’étendue des principes de base, suivez chaque onglet dans la création de règle afin d’afficher le type d’informations qui peut être configuré
    1. Quand vous atteignez l’onglet Vérifier + créer, sélectionnez **Enregistrer**.

1. Revenez à la page Sentinel en sélectionnant **Microsoft Sentinel | Hub de contenu** à partir de la barre de navigation en haut de la page, au-dessus de la mention « Règles d’analyse ».

1. Laissez cette page ouverte, car vous en aurez besoin pour la tâche suivante.


### Tâche 4

Dans cette tâche, vous allez parcourir certaines des options disponibles dans Sentinel.

1. Dans le volet de navigation gauche, développez **Gestion des menaces** et explorez les options répertoriées dans la gestion des menaces.
    1. Sélectionnez **Incidents**.  Bien qu’aucun incident ne soit trouvé, consultez la section **Qu’est-ce que c’est ?**.
    1. Sélectionnez **Repérage**, puis passez en revue les informations fournies dans l’onglet **Repérages (préversion)**.
    1. Sélectionnez **Notebooks** et passez en revue la section **Qu’est-ce que c’est ?**.
    1. Sélectionnez **Veille des menaces** et passez en revue les informations de la page.
    1. Sélectionnez **MITRE ATT&CK**.  MITRE ATT&CK est un base de connaissances accessible publiquement regroupant les tactiques et les techniques couramment utilisées par les attaquants. Avec Microsoft Sentinel vous pouvez afficher les détections déjà actives dans votre espace de travail, et celles que vous pouvez configurer, afin de comprendre la couverture de sécurité de votre organisation, en fonction des tactiques et des techniques issues du framework MITRE ATT&CK®.  Sélectionnez une cellule dans la matrice et notez les informations disponibles sur le côté droit de l’écran. **Remarque** : Vous devrez peut-être sélectionner le bouton « **<<**  » à l’extrême droite de la fenêtre pour afficher le panneau d’informations.

1. Dans le volet de navigation gauche, développez **Gestion de contenu**, puis sélectionnez **Communauté**. La page de la communauté comprend des insights et des mises à jour de cybersécurité de Microsoft Research, un lien vers une liste de blogs Microsoft Sentinel, un lien vers les forums Microsoft Sentinel, des liens vers les dernières éditions du Hub Microsoft Sentinel et bien plus encore. Explorer ceci à volonté.


1. Dans le volet de navigation gauche, développez **Configuration** et explorez les options répertoriées :
    1. Sélectionnez **Analyse**.  Il devrait y avoir deux règles actives, une qui est disponible par défaut et la règle que vous avez créée dans la tâche précédente. Sélectionnez la règle par défaut **Détection avancée des attaques en plusieurs étapes**.  Passez en revue les informations détaillées. **Remarque** : Vous devrez peut-être sélectionner le bouton « **<<**  » à l’extrême droite de la fenêtre pour afficher le panneau d’informations.
    1. Dans le volet de navigation de gauche, sélectionnez **Automation**.  Ici, vous pouvez créer des règles d’automatisation simples, intégrer des playbooks existants ou créer des playbooks.  Sélectionnez **+ Créer**, puis **Règle d’automatisation**.  Notez la fenêtre qui s’ouvre sur le côté droit de l’écran et les options disponibles pour créer des conditions et des actions.  Sélectionnez **Annuler** en bas de l’écran.

1. Fermez la fenêtre en sélectionnant le **X** en haut à droite de la fenêtre.

1. Dans le coin supérieur gauche de la fenêtre, dans la bannière bleue, sélectionnez **Mircosoft Azure** pour revenir à la page d’accueil du portail Azure.

1. Déconnectez-vous et fermez tous les onglets ouverts du navigateur.

### Révision

Dans ce labo, vous avez parcouru les étapes de connexion de Microsoft Sentinel à des sources de données, vous avez configuré un classeur et vous avez parcouru plusieurs options disponibles dans Microsoft Sentinel.
