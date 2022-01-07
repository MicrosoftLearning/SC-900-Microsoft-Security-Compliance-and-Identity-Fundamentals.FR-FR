---
lab:
    title: 'Explorer le portail Microsoft 365 Defender'
    module: 'Module 3, leçon 5 : Décrire les fonctionnalités des solutions de sécurité Microsoft : Décrire les fonctionnalités de gestion de la sécurité de Microsoft 365'
---


# Labo : Explorer le portail Microsoft 365 Defender

## Scénario du labo
Ce labo va vous présenter le portail Microsoft 365 Defender grâce au contenu affiché sur la page d’arrivée. Vous découvrirez également les options du volet de navigation. Celles-ci permettent d’accéder rapidement aux fonctionnalités qui font partie de la solution de détection et de réponse étendues (XDR) de Microsoft : Microsoft Defender pour point de terminaison et Microsoft Defender pour Office 365 (messagerie et collaboration).  Enfin, vous découvrirez comment le Niveau de sécurité Microsoft permet aux organisations d’améliorer leur posture de sécurité.


**Durée estimée** : 10-15 minutes

#### Tâche 1 :  Découvrez la page d’arrivée de Microsoft 365 Defender.

1. Ouvrez Microsoft Edge. Saisissez **admin.microsoft.com** dans la barre d’adresse.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, saisissez **admin@WWLxZZZZZZ.onmicrosoft.com** (ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
   
    1. Saisissez le mot de passe d’administrateur fourni par votre fournisseur d’hébergement de labo. Sélectionnez **Se connecter**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**. Vous accédez ainsi à la page du Centre d’administration Microsoft 365.

1. Sélectionnez **Sécurité** dans le volet de navigation de gauche du centre d’administration Microsoft 365.  Si l’option Sécurité ne figure pas dans la liste, sélectionnez **Tout afficher**, puis sélectionnez **Sécurité**.  Une nouvelle page de navigation s’ouvre sur la page d’accueil du portail Microsoft 365 Defender.  

1. Si c’est la première fois que accédez au portail Microsoft 365 Defender, il se peut qu’une fenêtre contextuelle s’ouvre et vous propose une présentation rapide du portail.  Nous vous conseillons d’accepter.  Sélectionnez **Présentation rapide**.  Lisez la description présente dans chaque fenêtre contextuelle, puis sélectionnez **Suivant**. Poursuivez la visite jusqu’à la fin, avant de sélectionner **Terminé**.

1. Le volet de navigation de gauche contient des liens et accès aux informations qui font partie de la solution de détection et de réponse étendues (XDR) de Microsoft. Ce volet comprend les incidents et les alertes, le repérage, le centre d’actions, l’analyse des menaces, le niveau de sécurité, le repérage, etc.  Il inclut aussi un accès rapide à Microsoft Defender pour point de terminaison (les liens figurent sous Points de terminaison) et à Defender pour Office 365 (les liens figurent sous Messagerie et collaboration).  Découvrez ces options en sélectionnant certains de ces liens.   Pour revenir à la page d’accueil du portail Microsoft 365 Defender, sélectionnez **Accueil** dans le volet de navigation de gauche.  Remarque : vous ne verrez peut-être que peu d’informations dans ces onglets, car aucun appareil n’est associé et vous n’avez peut-être pas de menaces ou d’alertes actives.

1. La page d’accueil du portail Microsoft 365 Defender affiche les cartes les plus courantes dont les équipes de sécurité ont besoin. La composition des cartes et des données dépend du rôle d’utilisateur. Faites défiler la page pour afficher l’ensemble de cartes par défaut pour votre rôle en tant qu’administrateur général.

1. Les cartes affichées peuvent être personnalisées selon vos préférences.  Sélectionnez **+ Ajouter des cartes**. Une fenêtre s’ouvre et vous indique que vous avez déjà toutes les cartes sur votre page d’accueil.  Fermez la fenêtre en cliquant sur le **X** en haut à droite de la fenêtre.

1. Sélectionner les points de suspension en haut à droite d’une carte vous permet d’effectuer plus d’actions.  

1. Vous pouvez aussi déplacer les cartes. Passez le curseur de votre souris sur la barre du titre d’une carte. Lorsque vous obtenez un curseur en forme de croix, sélectionnez la carte et déplacez-la où vous le souhaitez.

1. En sélectionnant le titre d’une carte, vous accédez à des informations complémentaires pour ce sujet. Vous Explorerez cette opération lors de la tâche suivante.  Gardez la fenêtre de navigation ouverte.

#### Tâche 2 : Cette tâche va vous présenter comment le Niveau de sécurité Microsoft permet aux organisations d’améliorer leur état de sécurité.

1. Depuis la page d’accueil du portail Microsoft 365 Defender, sélectionnez **Niveau de sécurité Microsoft**, à partir de la barre de titre de la carte (le texte deviendra bleu).  Vous pouvez aussi sélectionner **Niveau de sécurité** depuis le volet de navigation de gauche.

1. La page Niveau de sécurité Microsoft s’ouvre sous l’onglet Présentation.  Le Niveau de sécurité Microsoft est une mesure de la posture de sécurité d’une organisation. Le niveau de sécurité de votre organisation est indiqué sous forme de pourcentage, ainsi que le nombre de points obtenus sur le total des points possibles, le tout par catégorie. Sélectionnez **Inclure**, en regard de la mention Votre niveau de sécurité.  Une fenêtre contextuelle s’affiche pour vous permettre de renseigner le score réalisable, le score prévu et le score de la licence actuelle dans la ventilation du score de sécurité de votre organisation.  Sélectionnez à nouveau **Inclure** pour fermer la fenêtre.

1. La page de vue d’ensemble inclut aussi les meilleures actions d’amélioration, le score de comparaison, l’historique et les ressources supplémentaires.

1. Sélectionnez **Actions d’amélioration** en haut de la page.  Vous constaterez que des informations sur chaque élément sont affichées dans le tableau, y compris l’impact du score et le nombre de points accumulés.  

1. Plus d’informations sont disponibles lorsque vous sélectionnez l’un des éléments.  Sélectionnez **Exiger l’authentification multifacteur pour les rôles administratifs**.  Sélectionnez **Modifier le statut et le plan d’action**.  Dans la fenêtre qui s’affiche, notez les options de statut disponibles. Cliquez sur la croix **X** en haut à droite pour fermer cette fenêtre

1. Au bas de la page, sélectionnez **Gérer dans Microsoft Azure**.  Un nouvel onglet de navigateur s’ouvre et vous arrivez directement sur la page des stratégies d’accès conditionnel.  Si vous avez suivi l’exercice du labo Accès conditionnel, vous devriez voir s’afficher la politique. Retournez à l’onglet Niveau de sécurité Microsoft sur votre navigateur pour revenir à la page d’actions d’amélioration pour exiger l’authentification multifacteur pour les rôles administratifs. En haut à droite de la fenêtre, cliquez sur le **X** pour la fermer et retourner à la page d’actions d’amélioration.

1. Sélectionnez l’onglet **Historique** en haut de la page.  Certaines activités peuvent afficher des points négatifs.  Comme décrit dans le champ d’activité, cela peut être dû au fait qu’un élément a été retiré, car il n’était plus pertinent.  Sélectionnez un élément à partir du tableau d’historique.  Une page détaillant l’élément sélectionné s’affiche.  Examinez les options disponibles.  Pour quitter la page Détails et revenir sur la page Historique, cliquez sur la croix **X** affichée en haut à droite de la page.

1. En haut de la page, sélectionnez **Mesures et tendances**.  Notez les informations disponibles.  En haut à droite de la page, sélectionnez **l’icône de calendrier**.  Vous pouvez réduire l’affichage à une plage de dates personnalisée.  **L’icône de filtre** vous permet de filtrer l’affichage par identité, appareils ou applications.  Fermez la fenêtre et sélectionnez **Accueil** dans le volet de navigation de gauche pour retourner à la page d’accueil de Microsoft 365 Defender.

1. Fermez la page du navigateur.

#### Révision
Dans ce labo, vous avez découvert le portail Microsoft 365 Defender en parcourant le contenu affiché sur la page d’accueil, vous avez parcouru les options du volet de navigation qui fournissent un accès rapide aux fonctionnalités qui font partie de la solution de détection et de réponse étendues (XDR) de Microsoft, de Microsoft Defender pour Points de terminaison et de Microsoft Defender pour Office 365 (messagerie et collaboration).  Enfin, vous avez découvert comment le Niveau de sécurité Microsoft permet aux organisations d’améliorer leur état de sécurité.
