<!---
---
Labo : Parcours d’apprentissage : « Décrire les fonctionnalités de Microsoft Entra » Module : « Décrire les fonctionnalités de gestion des accès de Microsoft Entra ID » Unité : « Décrire l’accès conditionnel »
---
--->

# Labo : Accès conditionnel Microsoft Entra

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra
- Module : Décrire les fonctionnalités de gestion des accès de Microsoft Entra ID
- Unité : Décrire l’accès conditionnel

## Scénario du labo

Dans ce labo, vous découvrirez l’authentification multifacteur (MFA) à accès conditionnel du point de vue d’un administrateur et d’un utilisateur.  En tant qu’administrateur, vous allez créer une stratégie qui impose aux utilisateurs de passer par l’authentification multifacteur quand ils accèdent à une application de gestion Microsoft Azure basée sur le cloud.  Du point de vue de l’utilisateur, vous verrez l’impact de la stratégie d’accès conditionnel, y compris le processus d’inscription à la MFA.

**Durée estimée** : 30 minutes

### Tâche 1

Dans cette tâche, en tant qu’administrateur, vous réinitialiserez le mot de passe de l’utilisateur Charline Berger.  Cette étape est nécessaire pour pouvoir se connecter initialement en tant qu’utilisateur dans les tâches ultérieures.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse, entrez **https://entra.microsoft.com** et connectez-vous avec vos informations d’identification.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Dans le volet de navigation de gauche, développez **Identité**, développez **Utilisateurs**, puis sélectionnez **Tous les utilisateurs**.

1. Sélectionnez **Charline Berger** dans la liste des utilisateurs.

1. Sélectionnez **Réinitialiser le mot de passe**  en haut de la page. Comme vous ne vous êtes jamais connecté en tant que Charline Berger, vous ne connaissez pas le mot de passe de cette utilisatrice et vous devez le réinitialiser.

1. À l’ouverture de la fenêtre de réinitialisation du mot de passe, sélectionnez **Réinitialiser le mot de passe**.  IMPORTANT : Notez le nouveau mot de passe. Vous en aurez besoin pour vous connecter en tant qu’utilisateur lors d’une tâche ultérieure.

1. Fermez la fenêtre de réinitialisation du mot de passe en sélectionnant le **X** en haut à droite de la page, puis fermez la fenêtre Charline Berger en sélectionnant le **X** dans le coin supérieur droit de la page.

1. Dans le volet de navigation de gauche, sélectionnez **Accueil** pour retourner au centre d’administration Microsoft Entra.

1. Gardez cette fenêtre ouverte.

### Tâche 2

Dans cette tâche, vous allez suivre le processus de création d’une stratégie d’accès conditionnel dans Azure AD.

1. Ouvrez l’onglet du navigateur pour la page d’accueil du centre d’administration Microsoft Entra.   Si vous avez déjà fermé l’onglet de navigateur, ouvrez Microsoft Edge et entrez **https://entra.microsoft.com** dans la barre d’adresse, puis connectez-vous avec les informations d’identification d’administrateur Microsoft 365 fournies par l’hôte ALH.

1. Dans le volet de navigation de gauche, développez **Protection**, puis sélectionnez **Accès conditionnel**.

1. La page de présentation de l’accès conditionnel s’affiche.  Ici, vous verrez des vignettes montrant le résumé de la stratégie et les alertes générales.  Dans le volet de navigation de gauche, sélectionnez **Stratégies**.

1. Dans le volet de navigation de gauche, sélectionnez **Stratégies**. Toutes les stratégies d’accès conditionnel sont répertoriées ici. Sélectionnez **+ Nouvelle stratégie**.

1. Dans le champ Nom, saisissez **Stratégie de test MFA**.

1. Sous Utilisateurs, sélectionnez **0 utilisateur et groupe sélectionné**.

1. L’option pour inclure ou exclure des utilisateurs ou des groupes apparaît.  Assurez-vous que l’option **Inclure** est sélectionnée (soulignée).

1. Sélectionnez l’option pour **Sélectionner des utilisateurs et des groupes** et sélectionnez **Utilisateurs et groupes**.  La fenêtre Sélectionner des utilisateurs et des groupes s’ouvre.  

1. Dans la barre de recherche, saisissez **Charline**.  Sélectionnez **Charline Berger** sous la barre de recherche, puis appuyez sur le bouton **Sélectionner** au bas de la page.  Remarque : attribuer la stratégie aux utilisateurs d’un groupe est une pratique courante.  Dans ce labo, nous attribuons la stratégie à un utilisateur spécifique afin de gagner du temps.

1. Sous Ressources cibles, sélectionnez **Aucune ressource cible sélectionnée**.

1. Dans le champ sous la mention **Sélectionner ce à quoi cette stratégie s’applique**, sélectionnez la flèche vers le bas et notez les options disponibles.  Conservez le paramètre par défaut, **Applications cloud**.  Vérifiez que l’onglet **Inclure** est souligné.  Sélectionnez **Sélectionner les applications**, puis, sous la mention **Sélectionner**, sélectionnez **Aucune**.  La fenêtre Sélectionner des applications cloud s’ouvre.

1. Dans la barre de recherche, saisissez **Azure**.  Dans les résultats de la recherche qui apparaissent sous la zone de recherche, sélectionnez **Gestion Microsoft Azure**, puis appuyez sur **Sélectionner** au bas de la page.  Notez l’avertissement.  

1. Sous Conditions, sélectionnez **0 conditions sélectionnées**.  Notez les différentes options que vous pouvez configurer.  La stratégie vous permet de contrôler l’accès utilisateur en fonction de signaux provenant de conditions telles que le risque utilisateur, la connexion à risque, la plateforme de l’appareil, l’emplacement, les applications clientes ou le filtre pour les appareils.  Explorez ces options configurables, mais ne définissez aucune condition.

1. Définissez maintenant les contrôles d’accès.  Sous Accorder, sélectionnez **0 contrôles sélectionnés**.

1. La fenêtre Accorder s’ouvre.  Assurez-vous que l’option **Accorder l’accès** est sélectionnée, puis sélectionnez **Exiger l’authentification multifacteur**. Faites défiler vers le bas le contenu de la fenêtre de droite et, sous la section Pour plusieurs contrôles, conservez le paramètre par défaut **Demander tous les contrôles sélectionnés**.  Appuyez sur **Sélectionner** en bas de la page.

1. Au bas de la page, sous Activer la stratégie, sélectionnez **Activé**, puis sélectionnez **Créer**.

1. Dans le volet de navigation de gauche, sélectionnez **Stratégies**. La stratégie Pilote MFA devrait apparaître dans la liste des stratégies d’accès conditionnel (si nécessaire, sélectionnez l’**icône Actualiser** dans la barre de commande en haut de la page).

1. Déconnectez-vous en cliquant sur l’icône d’utilisateur à côté de l’adresse e-mail, dans le coin supérieur droit de l’écran, et en sélectionnant **Se déconnecter**. Ensuite, fermez toutes les fenêtres du navigateur.

### Tâche 3

Dans cette tâche, vous verrez l’impact de la stratégie d’accès conditionnel du point de vue d’une utilisatrice, Charline Berger. Vous allez commencer par vous connecter à une application qui n’est pas incluse dans la stratégie d’accès conditionnel (le portail Microsoft 365 sur https://login.microsoftonline.com) ).  Ensuite, vous allez répéter le processus pour une application qui est incluse dans la stratégie d’accès conditionnel (le portail Azure sur https://portal.azure.com) ).  Rappelez-vous que la stratégie exige que l’utilisateur passe par une MFA lorsqu’il accède à une application de gestion Microsoft Azure.  Pour utiliser une MFA, l’utilisateur doit d’abord enregistrer la méthode d’authentification qui sera utilisée comme MFA, par exemple un code envoyé à un appareil mobile ou une application d’authentification.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse, entrez **https://login.microsoftonline.com** .
    1. Connectez-vous en tant que **DebraB@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ est votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Saisissez le mot de passe que vous avez noté lors de la tâche précédente. Sélectionnez **Connexion**.
    1. Le mot de passe que vous avez fourni, en tant qu’administrateur, pour réinitialiser le mot de passe est temporaire. Vous devez donc changer votre mot de passe (cela ne fait pas partie de la stratégie MFA). Entrez le mot de passe actuel, entrez un nouveau mot de passe, puis confirmez le nouveau mot de passe.  Notez ce nouveau mot de passe, car vous en aurez besoin pour accomplir la tâche.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.  Vous devriez être connecté à votre compte Microsoft 365. Aucune MFA n’était nécessaire pour cette application, car elle ne fait pas partie de la stratégie.

1. Vous allez maintenant tenter de vous connecter à une application qui remplit les critères d’une MFA. Ouvrez un nouvel onglet de navigateur, puis entrez **https://portal.azure.com** .

1. Une fenêtre indiquant que des informations supplémentaires sont requises s’affiche.  Sélectionnez **Suivant**.  Notez que cela va lancer le processus d’inscription à la MFA, car vous accédez pour la première fois à l’application cloud qui a été identifiée dans la stratégie d’accès conditionnel.  Ce processus d’inscription ne doit être effectué qu’une seule fois.   L’administrateur peut configurer la méthode d’authentification à utiliser pour éviter que l’utilisateur ne doive suivre le processus d’inscription.

1. Dans la fenêtre Sécuriser votre compte, vous pouvez sélectionner la méthode à utiliser comme MFA.  Vous pouvez utiliser Microsoft Authenticator. Dans cet exercice de labo, vous choisirez une autre méthode afin de gagner du temps.  Sélectionnez **Je veux configurer une autre méthode**.  Dans la fenêtre contextuelle Choisir une autre méthode, sélectionnez la **flèche déroulante vers le bas**, **Téléphone**, puis **Confirmer**.

1. Dans la fenêtre qui s’ouvre, vérifiez que votre pays est sélectionné, puis entrez le numéro de téléphone mobile que vous souhaitez utiliser.  Vérifiez que l’option **Envoyez-moi un code par SMS** est sélectionnée, puis appuyez sur **Suivant**.  Vous allez recevoir un SMS avec un code sur votre téléphone. Vous devrez entrer ce code à l’emplacement indiqué.  Entrez le code que vous avez reçu, puis appuyez sur **Suivant**.  Une fois le code confirmé, le message « SMS vérifié. Votre téléphone a été inscrit. » s’affiche.  Sélectionnez **Suivant**. Ensuite, sélectionnez **Done** (Terminé).  Le processus d’inscription unique est terminé.

1. Vous devez maintenant être en mesure d’accéder au portail Azure.  Le portail Azure est une application de gestion Microsoft Azure et nécessite donc une authentification multifacteur, conformément à la stratégie d’accès conditionnel qui a été créée.  
    1. Si vous recevez un message indiquant que votre connexion a expiré, entrez le mot de passe, puis sélectionnez **Se connecter**.
    1. Une fenêtre s’affiche, vous demandant de vérifier votre identité.  Sélectionnez l’emplacement Texte =X XXXXXXX pour recevoir un code sur votre téléphone mobile, entrez le code, puis sélectionnez **Vérifier**.
    1. Si vous êtes invité à rester connecté, sélectionnez **Non**.

1. Déconnectez-vous en sélectionnant l’icône d’utilisateur à côté de l’adresse e-mail, dans le coin supérieur droit de l’écran, et en sélectionnant Se déconnecter. Ensuite, fermez toutes les fenêtres de navigation.

### Révision

Dans ce labo, vous avez vu le processus de configuration d’une stratégie d’accès conditionnel, qui impose aux utilisateurs de passer par l’authentification multifacteur (MFA) quand ils accèdent à une application de gestion Microsoft Azure basée sur le cloud.  Ensuite, en tant qu’utilisateur, vous avez suivi le processus d’inscription MFA et vu l’impact de la stratégie d’accès conditionnel exigeant l’utilisation d’une MFA pour accéder au portail Azure.
