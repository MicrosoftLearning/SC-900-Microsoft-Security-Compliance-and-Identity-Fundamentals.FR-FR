---
lab:
  title: 'Découvrir Azure Active Directory'
  module: 'Module 1 : Décrire les services de base et les types d’identités d’Azure AD'
---



# <a name="lab-explore-azure-active-directory"></a>Labo : Découvrir Azure Active Directory

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités d’Azure Active Directory (Azure AD) - Solution Microsoft Entra
- Module : Décrire les services de base et les types d’identités d’Azure AD
- Unité : Décrire les types d’identités Azure AD

## <a name="lab-scenario"></a>Scénario du labo

Dans ce labo, vous accéderez à Azure Active Directory.  En plus, vous créerez un utilisateur et vous configurerez les différents paramètres, y compris l’ajout de licences.  

**Durée estimée** : 10-15 minutes

### <a name="task-1"></a>Tâche 1

En tant qu’abonné à Microsoft 365, vous utilisez déjà Azure AD.  Lors de cette tâche, vous accédez à Azure AD via le portail d’administration Microsoft 365 et via le portail Azure.

1. Dans le navigateur Microsoft Edge, sélectionnez l’onglet Intitulé Accueil - Centre d’administration Microsoft 365.

1. Si vous avez précédemment fermé cet onglet de navigateur, suivez les étapes ci-dessous :
    1. Dans la barre d’adresse, entrez **admin.microsoft.com** et connectez-vous avec vos informations d’identification d’administrateur comme ceci :
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.
    1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous les centres d’administration, sélectionnez **Azure Active Directory** (vous devrez peut-être faire défiler la page).  Une nouvelle page de navigation s’ouvre sur la page Mon tableau de bord du Centre d’administration Azure Active Directory. Dans les fenêtres principales du tableau de bord, vous voyez plusieurs vignettes, entre autres la vignette de l’identité de l’organisation (Contoso, le locataire et l’édition Azure AD) et une vignette pour les utilisateurs et groupes.

1. Depuis le volet de navigation à gauche, sélectionnez **Azure Active Directory**.  Dans la fenêtre principale, vous voyez un autre volet de navigation qui liste tous les services disponibles dans Azure AD. À droite, vous voyez les informations à propos du locataire Contoso, des liens vers des types d’identités que vous pouvez créer et des services recommandés.  

1. Ouvrez maintenant une nouvelle fenêtre de navigateur et, dans la barre d’adresse, saisissez **portal.azure.com**.  Comme vous êtes déjà connecté sous le compte admin@WWLxZZZZZZ.onmicrosoft.com et que vous avez employé ces mêmes informations d’identification pour utiliser votre Pass Azure, vous devez en principe être connecté en tant qu’administrateur quand vous accédez au portail Azure.  Vous pouvez vérifier cela en consultant l’e-mail qui apparaît en haut à droite de la page quand vous passez votre souris sur l’icône d’utilisateur.

1. La page d’arrivée du portail Azure affiche les services Azure, y compris Azure Active Directory, les machines virtuelles, les comptes de stockage, les bases de données, etc.  Sélectionnez **Plus de services**, puis sélectionnez **Azure Active Directory**. Si vous ne le voyez pas immédiatement, vous pouvez entrer Azure Active Directory dans la barre de recherche bleue et le sélectionner à partir de là.  

1. Vous voyez maintenant Azure Active Directory pour votre locataire Contoso Microsoft 365.    Quelle que soit l’approche que vous utilisez pour accéder aux services Azure Active Directory (le portail d’administration Microsoft 365 ou le portail Azure), vous arrivez au même endroit : le locataire Contoso Azure Active Directory. Ici, vous pouvez gérer tous les services Azure AD.

1. Gardez cet onglet de navigation ouvert pour la tâche suivante.

### <a name="task-2"></a>Tâche 2

Lors de cette tâche, vous apprendrez comment créer un nouvel utilisateur dans Azure Active Directory et vous découvrirez certains services qui peuvent être gérés au niveau de l’utilisateur.

1. Accédez à l’onglet Contoso - Microsoft Azure ouvert dans votre navigateur. Si vous avez fermé l’onglet, ouvrez une page du navigateur et saisissez portal.azure.com dans la barre d’adresse. Ensuite, sélectionnez Azure Active Directory.  Vous devriez être connecté en tant qu’administrateur dans le portail Azure : si ce n’est pas le cas, reconnectez-vous.

1. Dans le volet de navigation de gauche, sélectionnez **Utilisateurs**.  Vous remarquerez que votre locataire est déjà configuré avec des utilisateurs.

1. En haut de la page, sélectionnez **+ Nouvel utilisateur** et, dans la zone déroulante, sélectionnez **Créer un utilisateur**.

1. L’option **Créer un utilisateur** doit normalement être déjà sélectionnée. Sinon, sélectionnez-la.

1. Remplissez les champs **Identité** de la manière suivante :

    1. Nom d’utilisateur : **sara**.

    1. Champ Nom : **Sara Perez**.

    1. Prénom : **Sara**.

    1. Nom : **Perez**.

1. Remplissez les champs **Mot de passe** de la manière suivante :

    1. Sélectionnez **Me permettre de créer le mot de passe**.

    1. Mot de passe initial : **Naja8996**. Lorsque Sara se connectera pour la première fois, elle sera invitée à changer son mot de passe.

1. Configurez **Groupes et rôles**.

    1. À côté de Groupes, sélectionnez **0 groupes sélectionnés**.  Cela affiche les groupes disponibles.  Prenez note de la liste des groupes disponibles.

    1. Sélectionnez **Opérations**, vous aurez peut-être besoin de faire défiler la page, puis appuyez sur **Sélectionner**. Notez comment le texte à côté des groupes s’est mis à jour et affiche maintenant 1 groupes sélectionnés.  

    1. À côté de Rôles, sélectionnez **Utilisateur**. La liste des rôles d’annuaire apparaît.  Faites défiler pour afficher les différents rôles intégrés, pour afficher les différents rôles, mais ne modifiez pas le rôle d’utilisateur.  Fermez cette fenêtre en sélectionnant le **X** en haut à droite de l’écran.

1. Configurez les **paramètres**

    1. Bloquer la connexion :  **Non** (conservez le paramètre par défaut).

    1. Emplacement d’utilisation : sélectionnez la liste déroulante, puis sélectionnez **États-Unis** (faites défiler le contenu vers le bas pour trouver cette option) ou le pays dans lequel vous vous trouvez.  La configuration de l’emplacement d’utilisation est nécessaire pour assigner des licences.

1. En bas de la page, sélectionnez le bouton **Créer**.

1. Vérifiez que l’utilisateur apparaît dans la liste des utilisateurs (les noms sont classés par ordre alphabétique). Vous devrez peut-être actualiser la page du navigateur.

1. Dans la liste d’utilisateurs, sélectionnez l’utilisateur que vous venez de créer, **Sara Perez**.  La page du profil s’ouvre.

1. Le volet de navigation à gauche affiche les différentes options qui peuvent être configurées pour l’utilisateur.  Sélectionnez **Groupes**.  C’est ici que vous pouvez voir des informations supplémentaires concernant le groupe.  Vérifiez que le groupe Opérations apparaît dans la liste (l’affectation de groupe peut prendre quelques minutes à s’afficher).  Remarque : vous voyez également le groupe Contoso, bien que nous n’ayons attribué qu’un groupe lors de la création de l’utilisateur.  C’est le résultat d’une stratégie préconfigurée dans le locataire qui affecte automatiquement les nouveaux utilisateurs au groupe Contoso.

1. Dans le volet de navigation de gauche, sélectionnez **Licences**.  Notez qu’il n’y a pas d’affectation de licence trouvée pour cet utilisateur.  

1. Pour ajouter une licence, sélectionnez **+ Affectations** en haut de la fenêtre principale.

1. Sous Sélectionner les licences, sélectionnez **Office 365 E3** et **Windows 10/11 Entreprise E3**, puis sélectionnez le bouton **Enregistrer** en bas de l’écran. Une notification devrait apparaître en haut à droite de l’écran et afficher la réussite des affectations de licence.

1. Sélectionnez le **X** en haut à droite de l’écran pour fermer la fenêtre Affectations de licence.

1. Sélectionnez **l’icône Actualiser** en haut de la page pour confirmer les affectations de licence.

1. Revenez à la page de vue d’ensemble Azure Active Directory Contoso, en sélectionnant **Contoso** en haut à gauche de l’écran (la barre de navigation), au-dessus de Sara Perez | Licenses.

1. Vous avez créé et configuré un utilisateur dans Azure Active Directory.

1. Déconnectez-vous de tous les onglets du navigateur ouverts.  Dans le portail Azure, déconnectez-vous en sélectionnant l’icône de l’utilisateur en regard de l’adresse e-mail dans le coin supérieur droit de l’écran, puis en sélectionnant **Se déconnecter**. Dans Microsoft 365, déconnectez-vous en sélectionnant l’icône en haut à droite de la fenêtre Microsoft 365 qui représente un cercle avec les lettres SP à l’intérieur (à côté de l’icône de point d’interrogation), puis en sélectionnant **Se déconnecter**. Ensuite, fermez toutes les fenêtres du navigateur.

### <a name="task-3"></a>Tâche 3

Lors de cette tâche, vous vous connectez pour la première fois en tant que Sara Perez.

1. Ouvrez Microsoft Edge.

2. Dans la barre d’adresse, entrez **login.microsoft.com**.

3. Connectez-vous en tant que **sara@WWLxZZZZZ.onmicrosoft.com** , (où ZZZZZZ est votre ID de locataire unique fourni par votre fournisseur d’hébergement lab).

4. Saisissez le mot de passe temporaire **Naja8996**.

5. Vous êtes maintenant invité à mettre à jour votre mot de passe. Dans le champ Mot de passe actuel, saisissez **Naja8996**.

6. Dans le champ Nouveau mot de passe, saisissez **SC900-Lab**.  Dans le champ Confirmer le mot de passe, saisissez SC900-Lab, puis sélectionnez Se connecter.  Remarque : en général, il est recommandé d’utiliser un mot de passe plus sécurisé. Ce mot de passe est choisi par commodité et uniquement pour les besoins de ce labo.

7. Vous devez maintenant être connecté à Microsoft 365.

8. Déconnectez-vous en sélectionnant l’icône en haut à droite de la fenêtre Microsoft 365 qui représente un cercle avec les lettres SP à l’intérieur (à côté de l’icône de point d’interrogation), puis en sélectionnant **Se déconnecter**. Ensuite, fermez le navigateur.

### <a name="review"></a>Révision

Dans ce labo, vous avez commencé votre découverte d’Azure AD. Puisque les abonnés à Microsoft 365 utilisent automatiquement Azure AD, vous avez découvert que vous accédez aux fonctionnalités et aux services d’Azure AD via le portail d’administration Microsoft 365 ou le portail Azure.  Choisissez l’approche que vous préférez pour accéder au même endroit.  Vous avez présenté le processus de création d’un utilisateur et les différents paramètres configurables, y compris les groupes auxquels l’utilisateur peut être affecté, les rôles disponibles et l’attribution de licences utilisateur.
