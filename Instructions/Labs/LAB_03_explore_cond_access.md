---
lab:
  title: Accès conditionnel Microsoft Entra
  module: Describe the access management capabilities of Microsoft Entra
---

# Labo : Accès conditionnel à Microsoft Entra

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra
- Module : décrire les fonctionnalités de gestion des accès de Microsoft Entra
- Leçon : décrire l’accès conditionnel

## Scénario du labo

Dans ce labo, vous découvrirez l’authentification multifacteur (MFA) à accès conditionnel du point de vue d’un administrateur et d’un utilisateur.  En tant qu’administrateur, vous allez créer une stratégie qui exigera qu’un utilisateur passe par l’authentification multifacteur lorsqu’il accède à l’un des portails Microsoft Admin.  Du point de vue de l’utilisateur, vous verrez l’impact de la stratégie d’accès conditionnel, y compris le processus d’inscription à la MFA.

**Durée estimée** : 30 minutes

### Tâche 1

Dans cette tâche, en tant qu’administrateur, vous réinitialiserez le mot de passe de l’utilisateur Debra Berger.  Cette étape est nécessaire pour que vous puissiez vous connecter initialement en tant qu’utilisateur dans les tâches suivantes.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse, saisissez **https://entra.microsoft.com** et connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique communiqué par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Cliquez sur **Connexion**.
    1. Selon votre hébergeur de labo et si c’est la première fois que vous vous connectez au locataire, vous serez peut-être invité à terminer le processus d’inscription MFA. Si c’est le cas, suivez les invites à l’écran pour configurer la MFA.
    1. Une fois connecté, vous êtes redirigé vers la page Centre d’administration Microsoft 365.

1. Dans le volet de navigation gauche, développez **Identités**, développez **Utilisateurs**, puis sélectionnez **Tous les utilisateurs**.

1. Sélectionnez **Debra Berger** dans la liste des utilisateurs.

1. Sélectionnez **Réinitialiser le mot de passe** en haut de la page. Comme vous ne vous êtes jamais connecté en tant que Charline Berger, vous ne connaissez pas le mot de passe de cette utilisatrice et vous devez le réinitialiser.

1. Lorsque la fenêtre de réinitialisation du mot de passe s’ouvre, sélectionnez **Réinitialiser le mot de passe**.  IMPORTANT : Notez le nouveau mot de passe. Vous en aurez besoin pour vous connecter en tant qu’utilisateur lors d’une tâche ultérieure.

1. Fermez la fenêtre de réinitialisation du mot de passe en sélectionnant le **X** en haut à droite de la page, puis fermez la fenêtre Charline Berger en sélectionnant le **X** dans le coin supérieur droit de la page.

1. Dans le volet de navigation de gauche, sélectionnez **Accueil** pour revenir au centre d’administration Microsoft Entra.

1. Gardez cette fenêtre ouverte.

### Tâche 2

Dans cette tâche, vous allez suivre le processus de création d’une stratégie d’accès conditionnel dans Microsoft Entra ID.

1. Ouvrez l’onglet du navigateur de la page d’accueil du centre d’administration Microsoft Entra.   Si vous avez déjà fermé l’onglet du navigateur, ouvrez Microsoft Edge et, dans la barre d’adresse, saisissez **`https://entra.microsoft.com`** et connectez-vous avec les informations d’identification d’administrateur Microsoft 365 fournies par l’ALH.

1. Dans le volet de navigation gauche, développez **Protection**, puis sélectionnez **Accès conditionnel**.

1. La page de présentation de l’accès conditionnel s’affiche. Lorsque vous accédez à la page de présentation, l’onglet **Prise en main** est sélectionné (souligné). Sélectionnez l’onglet **Présentation**. Ici, vous verrez des vignettes montrant le résumé de la stratégie et les alertes générales.  Dans le volet de navigation de gauche, sélectionnez **Stratégies**.

1. Dans le volet de navigation de gauche, sélectionnez **Stratégies**. Toute stratégie d’accès conditionnel existante est répertoriée ici. Sélectionnez **+ Nouvelle stratégie**.

1. Dans le champ Nom, entrez **Bloquer les portails d’administratio**n.

1. Sous Utilisateurs, sélectionnez **0 utilisateur et groupe sélectionné**.

1. L’option pour inclure ou exclure des utilisateurs ou des groupes apparaît.  Vérifiez que **Inclure** est sélectionné (souligné).

1. Sélectionnez l’option **Sélectionner les utilisateurs et les groupes** et sélectionnez **Utilisateurs et groupes**.  La fenêtre Sélectionner les utilisateurs ou les groupes s’ouvre.  

1. Dans la barre de recherche, entrez **Debra**.  Sélectionnez **Debra Berger** sous la barre de recherche, puis appuyez sur le bouton **Sélectionner** en bas de la page.  Notez qu’il est courant d’affecter la stratégie aux utilisateurs d’un groupe.  Dans ce labo, nous attribuons la stratégie à un utilisateur spécifique afin de gagner du temps.

1. Sous Ressources cibles, sélectionnez **Aucune ressource cible sélectionnée**.

1. Dans le champ situé en dessous de la mention **Sélectionner ce à quoi cette stratégie s’applique**, sélectionnez la flèche vers le bas et notez les options disponibles.  Conservez le paramètre par défaut, **Logiciels cloud**.  Vérifiez que l’onglet **Inclure** est souligné.  Sélectionnez **Sélectionner des applications**, puis sous **Sélectionner**, sélectionnez **Aucune**.  La fenêtre Logiciels cloud s’ouvre.

1. Sélectionnez **Portails d’administration Microsoft**, puis appuyez sur **Sélectionner** en bas de la page.  Notez l’avertissement.  

1. Sous Réseau, sélectionnez **N’importe quel réseau ou emplacement**.  Passez en revue les options, mais n’en sélectionnez aucune.

1. Sous Conditions, sélectionnez **0 condition sélectionnée**.  Remarquez les différentes options configurables.  La stratégie vous permet de contrôler l’accès des utilisateurs sur la base de signaux provenant de conditions, notamment : le risque lié à l’utilisateur, le risque lié à la connexion, la plateforme de l’appareil, l’emplacement, les applications client ou le filtre pour les appareils.  Explorez ces options configurables, mais ne définissez aucune condition.

1. Définissez maintenant les contrôles d’accès.  Sous Accorder, sélectionnez **0 contrôle sélectionné**.

1. La fenêtre Accorder s’ouvre.  Sélectionnez **Bloquer l’accès**. Appuyez sur **Suivant** en bas de la page.

1. Au bas de la page, sous Activer la stratégie, sélectionnez **Activé**, puis sélectionnez **Créer**.

1. Dans le volet de navigation de gauche, sélectionnez **Stratégies**. La stratégie **Bloquer les portails d’administrateur** que vous venez de créer doit apparaître dans la liste des stratégies d’accès conditionnel (Si nécessaire, sélectionnez l’**icône Actualiser** dans la barre de commandes en haut de la page).

1. Déconnectez-vous en sélectionnant l’icône d’utilisateur à côté de l’adresse e-mail, dans le coin supérieur droit de l’écran, et en sélectionnant **Se déconnecter**. Ensuite, fermez toutes les fenêtres de navigation.

### Tâche 3

Dans cette tâche, vous verrez l’impact de la stratégie d’accès conditionnel du point de vue d’une utilisatrice, Charline Berger. Vous allez commencer par vous connecter à une application qui n’est pas incluse dans la stratégie d’accès conditionnel (le portail Microsoft 365 sur https://login.microsoftonline.com)).  Ensuite, vous répéterez le processus pour une application qui est incluse dans la stratégie d’accès conditionnel (le Portail Azure sur https://portal.azure.com)).  Rappelez-vous que la stratégie bloque l'accès de tous les portails Microsoft Admin, y compris le portail Azure.  REMARQUE : pour des raisons de sécurité, tous les comptes d’utilisateur accédant à n’importe quel portail sont requis pour l’authentification multifacteur.  L’exigence d’authentification multifacteur est indépendante de cet exercice de labo.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse, entrez **https://login.microsoftonline.com** .
    1. Connectez-vous en tant que **DebraB@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ est votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Saisissez le mot de passe que vous avez noté dans la tâche précédente. Cliquez sur **Connexion**.
    1. Le mot de passe que vous avez fourni, en tant qu’administrateur, pour réinitialiser le mot de passe est temporaire. Vous devez donc le changer. Entrez le mot de passe actuel, entrez un nouveau mot de passe, puis confirmez le nouveau mot de passe.  Notez le nouveau mot de passe, car vous en aurez besoin pour accomplir la tâche.
    1. Comme c’est la première fois que vous vous connectez en tant que Debra Berger, vous serez peut-être invité à installer l’authentification multifacteur. Suivez les invites à l’écran pour installer l’authentification multifacteur.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.  Vous devez être connecté à votre compte Microsoft 365.

1. Vous allez maintenant tenter de vous connecter à une application qui remplit les critères d’une MFA. Ouvrez un nouvel onglet de navigateur et entrez **https://portal.azure.com**, qui est le portail d’administration pour Azure.  Une fenêtre contextuelle s’affiche indiquant « Vous n’avez pas accès à cela ».  Il s’agit d’un résultat de la stratégie d’accès conditionnel qui bloque votre accès à tous les portails d’administration Microsoft.

1. Déconnectez-vous en sélectionnant l’icône d’utilisateur à côté de l’adresse e-mail, dans le coin supérieur droit de l’écran, et en sélectionnant Se déconnecter. Ensuite, fermez toutes les fenêtres de navigation.

### Révision

Dans ce labo, vous avez compris le processus d'installation d’une stratégie d’accès conditionnel, qui bloque l'accès des portails administrateur Microsoft aux utilisateurs définis dans la stratégie.  Ensuite, en tant qu’utilisateur, vous avez mesuré l’impact de la stratégie d’accès conditionnel lors de l’accès au Portail Azure.
