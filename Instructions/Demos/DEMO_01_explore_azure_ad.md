<a name="---"></a><!---
---
Démonstration : Titre : « Découvrir les paramètres utilisateur Azure AD » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités d’Azure Active Directory (Azure AD) - Solution Microsoft Entra ; Module 1 : Décrire les services de base et les types d’identités d’Azure AD ; Unité 4 : Décrire les types d’identités Azure AD »
---
--->

# <a name="demo-azure-ad-user-settings"></a>Démonstration : Paramètres utilisateur Azure AD

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités d’Azure Active Directory (Azure AD) - Solution Microsoft Entra
- Module : Décrire les services de base et les types d’identités d’Azure AD
- Unité : Décrire les types d’identités Azure AD

## <a name="demo-scenario"></a>Scénario de la démonstration

Dans cette démonstration, vous allez accéder à Azure Active Directory et passer en revue les différents paramètres pour un utilisateur existant.  REMARQUE à l’attention du présentateur :  Cette démonstration accède à Azure AD via le locataire Microsoft 365. Une autre option à montrer aux participants est l’accès à Azure AD via le portail Azure. L’objectif d’accéder au portail Microsoft 365 est de montrer que Microsoft 365 inclut l’accès à Azure AD.

1. Ouvrez Microsoft Edge.

1. Dans la barre d’adresse, entrez **admin.microsoft.com** pour accéder au Centre d’administration Microsoft 365.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous les centres d’administration, sélectionnez **Azure Active Directory** (vous devrez peut-être faire défiler la page).  Une nouvelle page de navigation s’ouvre sur la page Mon tableau de bord du Centre d’administration Azure Active Directory. Dans les fenêtres principales du tableau de bord, vous voyez plusieurs vignettes, entre autres la vignette de l’identité de l’organisation (Contoso, le locataire et l’édition Azure AD) et une vignette pour les utilisateurs et groupes.

1. Dans le volet de navigation de gauche, sélectionnez **Utilisateurs**. Vous remarquerez que votre locataire est déjà configuré avec des utilisateurs.

1. Dans la liste des utilisateurs, sélectionnez **Adele Vance**.

1. Vous remarquerez que **Profil** est sélectionné dans le volet de navigation gauche.  Montrez et expliquez les informations affichées sur la page du profil.

1. Dans le volet de navigation de gauche, sélectionnez **Rôles affectés**.  Aucun rôle administratif n’a été attribué à cet utilisateur.  Sélectionnez **+ Ajouter des affectations** en haut de la page pour afficher les types de rôles administratifs disponibles.  N’en ajoutez aucun : fermez simplement la page en cliquant sur le **X** en haut à droite.

1. Dans le volet de navigation gauche, sélectionnez **Groupes**.  Expliquez qu’un utilisateur est membre de plusieurs groupes.  Vous pouvez ici aborder les types de groupes.  Pour ajouter cet utilisateur à d’autres groupes, sélectionnez **+ Ajouter des appartenances**.  N’ajoutez aucun nouveau groupe : expliquez simplement à quel point il est facile d’ajouter un utilisateur à des groupes existants. Fermez la fenêtre des groupes en cliquant sur le **X** en haut à droite de la page.

1. Dans le volet de navigation de gauche, sélectionnez **Licences**. Vous remarquerez que des licences Microsoft 365 E5 et EMS ont été affectées à cet utilisateur.  Pour ajouter une licence, sélectionnez **+ Affectations** en haut de la fenêtre principale.  Affichez les licences disponibles pour cet utilisateur. Ne changez RIEN.  Fermez cette fenêtre en cliquant sur le **X** en haut à droite de la page.

1. Dans le volet de navigation gauche, sélectionnez **Appareils**.  Rien ne s’affiche : vous pouvez cependant expliquer que c’est ici que les appareils affectés à l’utilisateur s’afficheraient s’il y en avait.

1. Dans le volet de navigation de gauche, sélectionnez **Attributions de rôles Azure**.  Expliquez
    1. qu’il s’agit d’un onglet différent de celui des rôles affectés montré auparavant, car l’onglet montré plus tôt était réservé au contrôle d’accès en fonction du rôle dans Azure Active Directory (mettez l’accent sur Active Directory).
    1. Dans cet onglet, vous voyez les attributions de rôles aux utilisateurs pour les ressources Azure. Par exemple, si vous créez un groupe de ressources Azure et que vous affectez un rôle spécifique à Adele tel que propriétaire ou contributrice du groupe de ressources, c’est ici que ce rôle apparaîtrait. Cela fait partie du contrôle d’accès en fonction du rôle Azure (Azure RBAC). Cette affectation de rôle est gérée en tant que partie intégrante de cette ressource spécifique.

1. Dans le volet de navigation de gauche, sélectionnez **Méthode d’authentification**.  Lisez la description : « Vous pouvez ici définir les numéros de téléphone ainsi que les adresses e-mail dont se servent les utilisateurs pour effectuer l’authentification multifacteur, la réinitialisation de mot de passe en libre-service et la réinitialisation du mot de passe d’un utilisateur. » Si un utilisateur est configuré pour la réinitialisation de mot de passe en libre-service (SSPR) ou doit utiliser l’authentification multifacteur (MFA) et que vous, en tant qu’administrateur, vous remplissez ces informations, il sera alors déjà inscrit et n’aura pas besoin d’effectuer les étapes d’inscription pour la SSPR ou la MFA.  Les utilisateurs s’inscrivent généralement eux-mêmes et les administrateurs n’ont besoin de le faire que rarement.

1. Dans le volet de navigation de gauche, sélectionnez **Connexions**.  Vous pouvez consulter ici les activités de connexion de cet utilisateur.  Rien n’apparaît pour cette utilisatrice, car elle ne s’est pas encore connectée.

1. Cliquez sur le **X** en haut à droite de la page. pour revenir à la liste des utilisateurs.  Avant de fermer la liste des utilisateurs, vous pouvez souligner le fait que la MFA s’affiche en haut de la page.  Sélectionnez **Authentification multifacteur**.  Une nouvelle fenêtre de navigateur s’ouvre.  Ici, vous pouvez sélectionner la MFA groupée pour les utilisateurs.  Il s’agit là d’une des façons d’activer la MFA pour les utilisateurs.  Nous allons vous expliquer plus en détail la MFA dans le contexte de l’accès conditionnel, et de quelle façon il offre un contrôle plus granulaire de la MFA.  Fermez l’onglet du navigateur concernant l’authentification multifacteur.

1. Cliquez sur le **X** en haut à droite de la page. Cela vous ramène à la page principale du locataire Contoso.

### <a name="review"></a>Révision

Dans cette démonstration, vous avez présenté les paramètres d’un utilisateur existant et les groupes auxquels il peut être affecté, les rôles disponibles ainsi que l’attribution de licences utilisateur.
