---
lab:
  title: "Explorer les paramètres utilisateur de Microsoft Entra\_ID"
  module: Describe the function and identity types of Microsoft Entra ID
---

# Labo : Explorer les paramètres utilisateur de Microsoft Entra ID

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra.
- Module : Décrire la fonction et les types d’identité de Microsoft Entra ID.
- Unité : Décrire les types d’identités.

## Scénario du labo

Dans ce labo, vous accédez à Microsoft Entra ID (anciennement appelé Azure Active Directory).  En plus, vous créerez un utilisateur et vous configurerez les différents paramètres, y compris l’ajout de licences.  

**Durée estimée** : 30 minutes

### Tâche 1

En tant qu’abonné à Microsoft 365, vous utilisez déjà Microsoft Entra ID (anciennement appelé Azure AD).  Dans cette tâche, vous apprenez à créer un utilisateur dans Microsoft Entra ID et découvrez certains services qui peuvent être gérés au niveau de l’utilisateur.

1. Ouvrez le navigateur Microsoft Edge. Dans la barre d’adresses, entrez **[admin.microsoft.com](https://admin.microsoft.com)** et connectez-vous avec les informations d’identification Microsoft 365 fournies par votre hôte de labo autorisé (ALH).
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ est votre ID de locataire unique communiqué par votre ALH), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Cliquez sur **Connexion**.
    1. Comme c’est votre première connexion, il peut vous être demandé d'installer l’authentification multifacteur. Suivez les invites à l’écran pour installer l’authentification multifacteur.
    1. Si vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Sous Centres d’administration, sélectionnez **Identité** (vous devez peut-être sélectionner **Tout afficher** et faire défiler vers le bas).  Une nouvelle page de navigateur s’ouvre sur la page de présentation du centre d’administration Microsoft Entra.

1. Dans le volet de navigation gauche, développez **Utilisateurs**, puis sélectionnez **Tous les utilisateurs**. Notez que votre locataire est déjà configuré avec des utilisateurs.

1. En haut de la page, sélectionnez **+ Nouvel utilisateur** et, dans la zone déroulante, sélectionnez **Créer un utilisateur**.

1. Vous êtes maintenant sous l’onglet **Informations de base** de la page Créer un utilisateur. Renseignez les champs de la façon suivante :
    1. Nom d’utilisateur principal : **sara**.

    1. Pseudonyme de messagerie : gardez la valeur par défaut, dérivée du nom d’utilisateur principal.

    1. Nom d’affichage : **Sara Perez**.

    1. Mot de passe : décochez la case qui indique de générer automatiquement le mot de passe et entrez un mot de passe temporaire qui respecte les exigences de mot de passe. Notez-le, car vous en avez besoin pour effectuer la tâche suivante.

    1. Compte activé : laissez la coche pour que le compte soit activé.

    1. En bas de la page, sélectionnez **Suivant : Propriétés**.

1. Ici, vous configurez quelques-uns des champs de l’onglet **Propriétés**.

    1. Prénom : Sara

    1. Nom : Perez

    1. Types d’utilisateur : laissez la valeur par défaut **Membre**, mais notez que dans la liste déroulante, vous avez la possibilité de sélectionner Invité.

    1. Localisation d’utilisation : choisissez le pays/la région où vous vous trouvez.  Notez que pour accéder au champ de localisation d’utilisation, vous devez faire défiler la page vers le bas, car il s’agit du dernier champ de la page.  **REMARQUE** : Si vous ne le faites pas, vous ne pouvez pas attribuer de licence dans les étapes suivantes.

    1. Sélectionnez **Suivant : Affectations**.

1. Vous êtes maintenant sous l’onglet **Attributions**, où vous ajoutez une attribution de groupe et consultez les options disponibles pour ajouter un rôle.

    1. Sélectionnez **Ajouter au groupe**.

    1. La fenêtre qui s’ouvre affiche tous les groupes disponibles.  

    1. Remarquez la liste des groupes disponibles.  Dans la liste, sélectionnez **Opérations**.  En bas de la page, sélectionnez le bouton **Sélectionner**.  Cela peut prendre quelques secondes, mais vous devez voir le groupe des opérations s’afficher dans la page des attributions.

    1. En haut de la page, sélectionnez **Ajouter un rôle**.  Une fenêtre s’ouvre et affiche tous les rôles d’annuaire disponibles.  Consultez les options disponibles, mais n’ajoutez pas de nouveaux rôles.  Fermez la page en sélectionnant le **X** en haut à droite de la page des rôles d’annuaire.
    1. En bas de la page, sélectionnez **Vérifier + Créer**. Un récapitulatif des paramètres s’affiche.  En bas de la page, sélectionnez **Créer**.

1. Vous êtes revenu dans la page des utilisateurs.  Au bout de quelques secondes, Sara Perez est listée.  Vous devez peut-être sélectionner l’icône **Actualiser** en haut de la page.

1. Dans la liste d’utilisateurs, sélectionnez l’utilisateur que vous venez de créer, **Sara Perez**.  La page **Vue d’ensemble** s’ouvre.

1. Le volet de navigation de gauche présente les différentes options qui peuvent être configurées pour l’utilisateur. Consultez les options disponibles.

1. Dans le volet de navigation de gauche, sélectionnez **Licences**.  Notez qu’aucune attribution de licence n’a été trouvée pour cet utilisateur et qu’il y a une icône d’avertissement qui indique : « L’ajout, la suppression et le retraitement des attributions de licences sont disponibles uniquement dans le centre d’administration M365 ».  Vous allez effectuer ces tâches au cours de la prochaine unité.  REMARQUE : Les licences peuvent être attribuées seulement si une localisation d’utilisation a été configurée. Si vous n’avez pas défini l’emplacement d’utilisation, revenez immédiatement à cette étape.

### Tâche 2

Dans cette tâche, vous allez attribuer une licence à l’utilisateur que vous venez de créer à l’aide du centre d’administration Microsoft 365.

1. Ouvrez l’onglet du navigateur **Accueil - Centre d’administration Microsoft 365**.

1. Dans le volet de navigation de gauche, dans Utilisateurs, sélectionnez **Utilisateurs actifs**.  Dans la liste des utilisateurs, sélectionnez **Sara Perez**.  Une fenêtre s’ouvre et affiche des informations sur l’utilisateur.  

    1. Sélectionnez l’onglet **Licences et applications**.
    1. Pour chacune des licences répertoriées, vous pouvez voir le nombre de licences disponibles.  Étant donné qu’il n’y a pas de licences Microsoft 365 E5 disponibles (elles ont déjà été attribuées à d’autres utilisateurs), attribuez les licences **Microsoft Power Apps - Développeur** et **Microsoft Power Automate - Gratuit** en cochant les cases situées à côté de celles-ci.
    1. Sélectionnez **Enregistrer les modifications**. Une notification dans le coin supérieur droit de l’écran devrait indiquer que les licences sont bien affectées.
    1. Fermez la page en cliquant sur le **X** dans le coin supérieur droit de la page.

1. Revenez au centre d’administration Microsoft Entra en sélectionnant **Accueil** dans le volet de navigation gauche ou en haut à gauche de l’écran (barre de navigation), au-dessus de Sara Perez | Licences.

1. Vous avez ainsi attribué des licences à l’utilisateur.

1. Déconnectez-vous de tous les onglets du navigateur ouverts. Déconnectez-vous en sélectionnant l’icône d’utilisateur à côté de l’adresse e-mail, en haut à droite de l’écran, et sélectionnez **Se déconnecter**. Fermez toutes les fenêtres de navigateur.

### Tâche 3

Lors de cette tâche, vous vous connectez pour la première fois en tant que Sara Perez.

1. Ouvrez Microsoft Edge.

1. Dans la barre d’adresse, entrez **https://login.microsoft.com** .

1. Connectez-vous avec **sara@WWLxZZZZZ.onmicrosoft.com** , (où ZZZZZZ est votre ID de locataire unique indiqué par votre ALH)
1. Entrez le mot de passe temporaire que vous avez défini dans la tâche précédente.

1. Vous êtes maintenant invité à mettre à jour votre mot de passe. Dans le champ Mot de passe actuel, entrez le mot de passe temporaire de la tâche précédente.

1. Dans le champ Nouveau mot de passe, entrez un nouveau mot de passe, confirmez le mot de passe, puis sélectionnez **Se connecter**.  Notez votre nouveau mot de passe, car vous en avez besoin pour l’exercice de labo suivant sur SSPR.

1. Comme c’est votre première connexion en tant que Sara Perez, vous serez peut-être invité à installer l’authentification multifacteur. Suivez les invites à l’écran pour installer l’authentification multifacteur.

1. Vous devriez maintenant être connecté au compte Microsoft de Sara.  Notez que les licences de Sara que vous avez attribuées dans la tâche précédente étaient limitées uniquement à Power Automate - Gratuit et Power Apps pour les développeurs et n’incluaient pas de licence E5.

1. Déconnectez-vous en sélectionnant l’icône en haut à droite de la fenêtre Microsoft 365 qui représente un cercle avec les lettres SP à l’intérieur (à côté de l’icône de point d’interrogation), puis en sélectionnant **Se déconnecter**. Ensuite, fermez le navigateur.

### Révision

Dans ce labo, vous avez commencé votre exploration initiale de Microsoft Entra ID. Puisque les abonnés à Microsoft 365 utilisent automatiquement Microsoft Entra ID, vous avez découvert que vous accédez aux fonctionnalités et aux services Microsoft Entra ID via le portail d’administration Microsoft 365 ou le portail Azure.  Quelle que soit l’approche que vous préférez, vous arriverez au même endroit.  Vous avez présenté le processus de création d’un utilisateur et les différents paramètres configurables, y compris les groupes auxquels l’utilisateur peut être affecté, les rôles disponibles et l’attribution de licences utilisateur.
