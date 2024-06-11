---
lab:
  title: Accès conditionnel Microsoft Entra
  module: Describe the access management capabilities of Microsoft Entra ID
---

# Labo : Accès conditionnel à Microsoft Entra

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra
- Module : décrire les fonctionnalités de gestion des accès de Microsoft Entra ID
- Leçon : décrire l’accès conditionnel

## Scénario du labo

Dans ce labo, vous découvrirez l’authentification multifacteur (MFA) à accès conditionnel du point de vue d’un administrateur et d’un utilisateur.  En tant qu’administrateur, vous allez créer une stratégie qui exigera qu’un utilisateur passe par l’authentification multifacteur lorsqu’il accède à l’un des portails Microsoft Admin.  Du point de vue de l’utilisateur, vous verrez l’impact de la stratégie d’accès conditionnel, y compris le processus d’inscription à la MFA.

**Durée estimée** : 30 minutes

### Tâche 1

Dans cette tâche, en tant qu’administrateur, vous réinitialiserez le mot de passe de l’utilisateur Debra Berger.  Cette étape est nécessaire pour que vous puissiez vous connecter initialement en tant qu’utilisateur dans les tâches suivantes.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse, saisissez **https://entra.microsoft.com** et connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique communiqué par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Cliquez sur **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Dans le volet de navigation gauche, développez **Identités**, développez **Utilisateurs**, puis sélectionnez **Tous les utilisateurs**.

1. Sélectionnez **Debra Berger** dans la liste des utilisateurs.

1. Sélectionnez **Réinitialiser le mot de passe** en haut de la page. Comme vous ne vous êtes jamais connecté en tant que Charline Berger, vous ne connaissez pas le mot de passe de cette utilisatrice et vous devez le réinitialiser.

1. Lorsque la fenêtre de réinitialisation du mot de passe s’ouvre, sélectionnez **Réinitialiser le mot de passe**.  IMPORTANT : Notez le nouveau mot de passe. Vous en aurez besoin pour vous connecter en tant qu’utilisateur lors d’une tâche ultérieure.

1. Fermez la fenêtre de réinitialisation du mot de passe en sélectionnant le **X** en haut à droite de la page, puis fermez la fenêtre Charline Berger en sélectionnant le **X** dans le coin supérieur droit de la page.

1. Dans le volet de navigation de gauche, sélectionnez **Accueil** pour revenir au centre d’administration Microsoft Entra.

1. Gardez cette fenêtre ouverte.

### Tâche 2

Dans cette tâche, vous allez suivre le processus de création d’une stratégie d’accès conditionnel dans Microsoft Entra ID.

1. Ouvrez l’onglet du navigateur de la page d’accueil du centre d’administration Microsoft Entra.   Si vous avez déjà fermé l’onglet du navigateur, ouvrez Microsoft Edge et, dans la barre d’adresse, saisissez **https://entra.microsoft.com** et connectez-vous avec les informations d’identification d’administrateur Microsoft 365 fournies par l’ALH.

1. Dans le volet de navigation gauche, développez **Protection**, puis sélectionnez **Accès conditionnel**.

1. La page de présentation de l’accès conditionnel s’affiche.  Ici, vous verrez des vignettes montrant le résumé de la stratégie et les alertes générales.  Dans le volet de navigation de gauche, sélectionnez **Stratégies**.

1. Dans le volet de navigation de gauche, sélectionnez **Stratégies**. Toute stratégie d’accès conditionnel existante est répertoriée ici. Sélectionnez **+ Nouvelle stratégie**.

1. Dans le champ Nom, saisissez **Stratégie de test de MFA**.

1. Sous Utilisateurs, sélectionnez **0 utilisateur et groupe sélectionné**.

1. L’option pour inclure ou exclure des utilisateurs ou des groupes apparaît.  Vérifiez que **Inclure** est sélectionné (souligné).

1. Sélectionnez l’option **Sélectionner les utilisateurs et les groupes** et sélectionnez **Utilisateurs et groupes**.  La fenêtre Sélectionner les utilisateurs ou les groupes s’ouvre.  

1. Dans la barre de recherche, entrez **Debra**.  Sélectionnez **Debra Berger** sous la barre de recherche, puis appuyez sur le bouton **Sélectionner** en bas de la page.  Notez qu’il est courant d’affecter la stratégie aux utilisateurs d’un groupe.  Dans ce labo, nous attribuons la stratégie à un utilisateur spécifique afin de gagner du temps.

1. Sous Ressources cibles, sélectionnez **Aucune ressource cible sélectionnée**.

1. Dans le champ situé en dessous de la mention **Sélectionner ce à quoi cette stratégie s’applique**, sélectionnez la flèche vers le bas et notez les options disponibles.  Conservez le paramètre par défaut, **Logiciels cloud**.  Vérifiez que l’onglet **Inclure** est souligné.  Sélectionnez **Sélectionner des applications**, puis sous **Sélectionner**, sélectionnez **Aucune**.  La fenêtre Logiciels cloud s’ouvre.

1. Dans la barre de recherche, entrez **Azure**.  Dans les résultats de recherche qui apparaissent sous la zone de recherche, sélectionnez **Portails Microsoft Admin**, puis appuyez sur **Sélectionner** en bas de la page.  Notez l’avertissement.  

1. Sous Conditions, sélectionnez **0 condition sélectionnée**.  Remarquez les différentes options configurables.  La stratégie vous permet de contrôler l’accès des utilisateurs sur la base de signaux provenant de conditions, notamment : le risque lié à l’utilisateur, le risque lié à la connexion, la plateforme de l’appareil, l’emplacement, les applications client ou le filtre pour les appareils.  Explorez ces options configurables, mais ne définissez aucune condition.

1. Définissez maintenant les contrôles d’accès.  Sous Accorder, sélectionnez **0 contrôle sélectionné**.

1. La fenêtre Accorder s’ouvre.  Assurez-vous que l’option **Accorder l’accès** est sélectionnée, puis sélectionnez **Exiger l’authentification multifacteur**. Faites défiler vers le bas le contenu de la fenêtre de droite et, sous la section Pour plusieurs contrôles, conservez le paramètre par défaut **Demander tous les contrôles sélectionnés**.  Appuyez sur **Suivant** en bas de la page.

1. Au bas de la page, sous Activer la stratégie, sélectionnez **Activé**, puis sélectionnez **Créer**.

1. Dans le volet de navigation de gauche, sélectionnez **Stratégies**. La stratégie pilote MFA doit apparaître dans la liste des stratégies d’accès conditionnel. (Si nécessaire, sélectionnez l’icône **Actualiser** dans la barre de commandes en haut de la page).

1. Déconnectez-vous en sélectionnant l’icône d’utilisateur à côté de l’adresse e-mail, dans le coin supérieur droit de l’écran, et en sélectionnant **Se déconnecter**. Ensuite, fermez toutes les fenêtres de navigation.

### Tâche 3

Dans cette tâche, vous verrez l’impact de la stratégie d’accès conditionnel du point de vue d’une utilisatrice, Charline Berger. Vous allez commencer par vous connecter à une application qui n’est pas incluse dans la stratégie d’accès conditionnel (le portail Microsoft 365 sur https://login.microsoftonline.com)).  Ensuite, vous répéterez le processus pour une application qui est incluse dans la stratégie d’accès conditionnel (le Portail Azure sur https://portal.azure.com)).  Rappelez que la stratégie exige que l’utilisateur passe par MFA lorsqu’il accède à l’un des portails Microsoft Admin, y compris le Portail Azure.  Pour utiliser la MFA, l’utilisateur doit d’abord enregistrer la méthode d’authentification qui sera utilisée, par exemple un code envoyé à un appareil mobile ou une application d’authentification.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse, entrez **https://login.microsoftonline.com** .
    1. Connectez-vous en tant que **DebraB@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ est votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Saisissez le mot de passe que vous avez noté dans la tâche précédente. Cliquez sur **Connexion**.
    1. Le mot de passe que vous avez fourni, en tant qu’administrateur, pour réinitialiser le mot de passe est temporaire. Vous devez donc changer votre mot de passe (cela ne fait pas partie de la stratégie MFA). Entrez le mot de passe actuel, entrez un nouveau mot de passe, puis confirmez le nouveau mot de passe.  Notez le nouveau mot de passe, car vous en aurez besoin pour accomplir la tâche.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.  Vous devez être connecté à votre compte Microsoft 365. La MFA n’était pas nécessaire pour cette application, car elle ne fait pas partie de la stratégie.

1. Vous allez maintenant tenter de vous connecter à une application qui remplit les critères d’une MFA. Ouvrez un nouvel onglet de navigateur et saisissez **https://portal.azure.com**.

1. Une fenêtre indiquant que des informations supplémentaires sont requises s’affiche.  Cliquez sur **Suivant**.  Notez que cela va lancer le processus d’inscription à la MFA, car vous accédez pour la première fois à l’application cloud qui a été identifiée dans la stratégie d’accès conditionnel.  Ce processus d’inscription n’est requis qu’une seule fois.   Au lieu de demander à l’utilisateur de suivre le processus d’enregistrement, l’administrateur peut configurer la méthode d’authentification à utiliser.

1. Dans la fenêtre Sécuriser votre compte, vous avez la possibilité de sélectionner la méthode à utiliser pour la MFA.  Microsoft Authenticator est une option. Dans cet exercice de labo, vous choisirez une autre méthode afin de gagner du temps.  Sélectionnez **Je veux configurer une autre méthode**.  Dans la fenêtre contextuelle Choisir une autre méthode, sélectionnez la **flèche déroulante**, **Téléphone**, puis **Confirmer**.

1. Dans la fenêtre qui s’ouvre, vérifiez que votre pays est sélectionné, puis entrez le numéro de téléphone mobile que vous souhaitez utiliser.  Vérifiez que l’option **Envoyez-moi un code par SMS** est sélectionnée, puis appuyez sur **Suivant**.  Vous allez recevoir un SMS avec un code sur votre téléphone. Vous devrez entrer ce code à l’emplacement indiqué.  Entrez le code que vous avez reçu, puis appuyez sur **Suivant**.  Une fois le code confirmé, le message « SMS vérifié. Votre téléphone a été inscrit. » s’affiche.  Cliquez sur **Suivant**. Ensuite, sélectionnez **Done** (Terminé).  Ceci conclut le processus d’inscription unique.

1. Vous devriez maintenant pouvoir accéder au Portail Azure.  Le Portail Azure est un portail Microsoft Admin et nécessite donc une authentification multifacteur, conformément à la stratégie d’accès conditionnel qui a été créée.  
    1. Si vous recevez un message indiquant que votre connexion a expiré, entrez le mot de passe et sélectionnez **Se connecter**.
    1. Une fenêtre s’affiche, vous demandant de vérifier votre identité.  Sélectionnez l’emplacement Texte =X XXXXXXX pour recevoir un code sur votre téléphone mobile, entrez le code, puis sélectionnez **Vérifier**.
    1. Si vous êtes invité à rester connecté, sélectionnez **Non**.

1. Déconnectez-vous en sélectionnant l’icône d’utilisateur à côté de l’adresse e-mail, dans le coin supérieur droit de l’écran, et en sélectionnant Se déconnecter. Ensuite, fermez toutes les fenêtres de navigation.

### Révision

Dans ce labo, vous avez vu le processus de configuration d’une stratégie d’accès conditionnel, qui impose aux utilisateurs de passer par l’authentification multifacteur (MFA) quand ils accèdent à n’importe quel portail Microsoft Admin.  Ensuite, en tant qu’utilisateur, vous avez suivi le processus d’enregistrement pour la MFA et vu l’impact de la stratégie d’accès conditionnel qui vous obligeait à utiliser la MFA pour accéder au Portail Azure.
