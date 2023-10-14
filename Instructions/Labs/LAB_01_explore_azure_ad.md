<!---
---
Labo : Titre : « Explorer les paramètres des utilisateurs Microsoft Entra ID » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra ; Module 1 : Décrire la fonction et les types d’identité de Microsoft Entra ID ; Unité 3 : Décrire les types d’identité Microsoft Entra »
---
--->

# Labo : Explorer Microsoft Entra ID

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra.
- Module : Décrire la fonction et les types d’identité de Microsoft Entra ID.
- Unité : Décrire les types d’identités.

## Scénario du labo

Dans ce labo, vous accédez à Microsoft Entra ID (anciennement appelé Azure Active Directory).  En plus, vous créerez un utilisateur et vous configurerez les différents paramètres, y compris l’ajout de licences.  

**Durée estimée** : 10-15 minutes

### Tâche 1

En tant qu’abonné à Microsoft 365, vous utilisez déjà Microsoft Entra ID (anciennement appelé Azure AD).  Dans cette tâche, vous apprenez à créer un utilisateur dans Microsoft Entra ID et découvrez certains services qui peuvent être gérés au niveau de l’utilisateur.

1. Ouvrez le navigateur Microsoft Edge. Dans la barre d’adresses, entrez **[admin.microsoft.com](https://admin.microsoft.com)** et connectez-vous avec les informations d’identification Microsoft 365 fournies par votre hôte de labo autorisé (ALH).
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ est votre ID de locataire unique communiqué par votre ALH), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Sous Centres d’administration, sélectionnez **Identité** (vous devez peut-être sélectionner **Tout afficher** et faire défiler vers le bas).  Une nouvelle page de navigateur s’ouvre sur la page de présentation du centre d’administration Microsoft Entra. Ici, vous voyez les informations de base de votre locataire Contoso. Si vous faites défiler la fenêtre principale vers le bas, vous voyez également des informations sur les alertes, mon flux, les fonctionnalités en vedette, etc.

1. Dans le volet de navigation gauche, développez **Utilisateurs**, puis sélectionnez **Tous les utilisateurs**. Vous remarquerez que votre locataire est déjà configuré avec des utilisateurs.

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

    1. Sélectionnez **Ajouter un groupe**.

    1. La fenêtre qui s’ouvre affiche tous les groupes disponibles.  

    1. Prenez note de la liste des groupes disponibles.  Dans la liste, sélectionnez **Opérations**.  En bas de la page, sélectionnez le bouton **Sélectionner**.  Cela peut prendre quelques secondes, mais vous devez voir le groupe des opérations s’afficher dans la page des attributions.

    1. En haut de la page, sélectionnez **Ajouter un rôle**.  Une fenêtre s’ouvre et affiche tous les rôles d’annuaire disponibles.  Consultez les options disponibles, mais n’ajoutez pas de nouveaux rôles.  Fermez la page en sélectionnant le **X** en haut à droite de la page des rôles d’annuaire.
    1. En bas de la page, sélectionnez **Vérifier + Créer**. Un récapitulatif des paramètres s’affiche.  En bas de la page, sélectionnez **Créer**.

1. Vous êtes revenu dans la page des utilisateurs.  Au bout de quelques secondes, Sara Perez est listée.  Vous devez peut-être sélectionner l’icône **Actualiser** en haut de la page.

1. Dans la liste d’utilisateurs, sélectionnez l’utilisateur que vous venez de créer, **Sara Perez**.  La page **Vue d’ensemble** s’ouvre.

1. Le volet de navigation à gauche affiche les différentes options qui peuvent être configurées pour l’utilisateur. Consultez les options disponibles.

1. Dans le volet de navigation de gauche, sélectionnez **Licences**.  Notez qu’il n’y a pas d’affectation de licence trouvée pour cet utilisateur.  REMARQUE : Les licences peuvent être attribuées seulement si une localisation d’utilisation a été configurée. Si vous n’avez pas défini la localisation d’utilisation, revenez à cette étape de la tâche précédente.

    1. Pour ajouter une licence, sélectionnez **+ Affectations** en haut de la fenêtre principale.

    1. Sous Sélectionner les licences, sélectionnez **Office 365 E3** et **Windows 10/11 Entreprise E3**, puis sélectionnez le bouton **Enregistrer** en bas de l’écran. Une notification devrait apparaître en haut à droite de l’écran et afficher la réussite des affectations de licence.

    1. Sélectionnez le **X** en haut à droite de l’écran pour fermer la fenêtre Affectations de licence.

    1. Sélectionnez **l’icône Actualiser** en haut de la page pour confirmer les affectations de licence.

1. Revenez au centre d’administration Microsoft Entra en sélectionnant **Accueil** dans le volet de navigation gauche ou en haut à gauche de l’écran (barre de navigation), au-dessus de Sara Perez | Licences.

1. Vous avez créé et configuré un utilisateur dans Microsoft Entra ID.

1. Déconnectez-vous de tous les onglets du navigateur ouverts. Déconnectez-vous en sélectionnant l’icône d’utilisateur à côté de l’adresse e-mail, en haut à droite de l’écran, et sélectionnez **Se déconnecter**. Fermez toutes les fenêtres de navigateur.

### Tâche 2

Lors de cette tâche, vous vous connectez pour la première fois en tant que Sara Perez.

1. Ouvrez Microsoft Edge.

2. Dans la barre d’adresse, entrez **https://login.microsoft.com** .

3. Connectez-vous avec **sara@WWLxZZZZZ.onmicrosoft.com** , (où ZZZZZZ est votre ID de locataire unique indiqué par votre ALH)
4. Entrez le mot de passe temporaire que vous avez défini dans la tâche précédente.

5. Vous êtes maintenant invité à mettre à jour votre mot de passe. Dans le champ Mot de passe actuel, entrez le mot de passe temporaire de la tâche précédente.

6. Dans le champ Nouveau mot de passe, entrez un nouveau mot de passe, confirmez le mot de passe, puis sélectionnez **Se connecter**.  Notez votre nouveau mot de passe, car vous en avez besoin pour l’exercice de labo suivant sur SSPR.

7. Vous devez maintenant être connecté à Microsoft 365.

8. Déconnectez-vous en sélectionnant l’icône en haut à droite de la fenêtre Microsoft 365 qui représente un cercle avec les lettres SP à l’intérieur (à côté de l’icône de point d’interrogation), puis en sélectionnant **Se déconnecter**. Ensuite, fermez le navigateur.

### Révision

Dans ce labo, vous avez commencé votre découverte d’Azure AD. Puisque les abonnés à Microsoft 365 utilisent automatiquement Azure AD, vous avez découvert que vous accédez aux fonctionnalités et aux services d’Azure AD via le portail d’administration Microsoft 365 ou le portail Azure.  Choisissez l’approche que vous préférez pour accéder au même endroit.  Vous avez présenté le processus de création d’un utilisateur et les différents paramètres configurables, y compris les groupes auxquels l’utilisateur peut être affecté, les rôles disponibles et l’attribution de licences utilisateur.
