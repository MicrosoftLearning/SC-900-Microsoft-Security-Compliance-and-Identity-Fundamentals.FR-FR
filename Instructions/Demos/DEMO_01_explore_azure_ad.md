---
Demo:
    title: 'Paramètres utilisateur d’Azure Active Directory'
    module: 'Module 2, leçon 1 : Décrire les fonctionnalités des solutions de gestion des accès et des identités Microsoft : Explorer les services et les types d’identités Azure AD'
---

# Démonstration : Paramètres utilisateur d’Azure Active Directory

### Scénario de la démonstration

Dans cette démonstration, vous accéderez à Azure Active Directory et parcourrez les différents paramètres pour un utilisateur existant.

1. Accédez à l’onglet **Accueil - Microsoft Azure** ouvert dans votre navigateur.  Si vous avez fermé l’onglet, lancez Microsoft Edge et saisissez portal.azure.com dans la barre d’adresse. Connectez-vous ensuite à l’aide des mêmes informations d’identification d’administrateur que votre locataire Microsoft 365.

1. La page de destination du portail Azure affiche les services Azure. Cliquez sur **Azure Active Directory**. S’il n’apparaît pas immédiatement, saisissez « Azure Active Directory » dans la zone de recherche près de l’intitulé « Microsoft Azure ».  Vous pouvez également montrer comment y accéder par l’intermédiaire de l’icône de menu pour afficher le portail (les trois lignes horizontales, également appelées menu à tiroir, dans la barre bleue en haut de la page) qui se situe à gauche de l’intitulé « Microsoft Azure ».

1. Dans le volet de navigation de gauche, sélectionnez **Utilisateurs**. Vous remarquerez que votre locataire est déjà configuré avec des utilisateurs.

1. Dans la liste des utilisateurs, sélectionnez **Adele Vance**.

1. Vous remarquerez que **Profil** est sélectionné dans le volet de navigation de gauche.  Montrez et expliquez les informations affichées sur la page du profil.

1. Dans le volet de navigation de gauche, sélectionnez **Rôles affectés**.  Aucun rôle administratif n’a été affecté à cet utilisateur.  Sélectionnez **+ Ajouter des affectations** en haut de la page pour afficher les types de rôles administratifs disponibles.  N’en ajoutez aucun : fermez simplement la page en cliquant sur le **X** en haut à droite.

1. Dans le volet de navigation de gauche, sélectionnez **Groupes**.  Expliquez qu’un utilisateur est membre de plusieurs groupes.  Vous pouvez ici aborder les types de groupes.  Pour ajouter cet utilisateur à d’autres groupes, vous pouvez juste sélectionner **+ Ajouter des appartenances**.  N’ajoutez aucun nouveau groupe : expliquez simplement à quel point il est facile d’ajouter un utilisateur à des groupes existants. Fermez la fenêtre des groupes en cliquant sur le **X** en haut à droite de la page.

1. Dans le volet de navigation de gauche, sélectionnez **Licences**. Vous remarquerez que des licences Microsoft 365 E5 et EMS ont été affectées à cet utilisateur.  Pour ajouter une licence, sélectionnez **+ Affectations** en haut de la fenêtre principale.  Affichez les licences disponibles pour cet utilisateur. Ne changez RIEN.  Fermez cette fenêtre en cliquant sur le **X** en haut à droite de la page.

1. Dans le volet de navigation de gauche, sélectionnez **Appareils**.  Rien ne s’affiche : vous pouvez cependant expliquer que c’est ici que les appareils affectés à l’utilisateur s’afficheraient s’il y en avait.

1. Dans le volet de navigation de gauche, sélectionnez **Attributions de rôles Azure**.  Expliquez
    1. qu’il s’agit d’un onglet différent de celui des rôles affectés montré auparavant, car l’onglet montré plus tôt était réservé au contrôle d’accès en fonction du rôle dans Azure Active Directory (mettez l’accent sur Active Directory).
    1. Cet onglet vous permet de consulter les affectations de rôles aux utilisateurs pour les ressources Azure. Par exemple, si vous créez un groupe de ressources Azure et que vous affectez un rôle spécifique à Adele tel que propriétaire ou contributrice du groupe de ressources, c’est ici que ce rôle apparaîtrait. Cela fait partie du contrôle d’accès en fonction du rôle Azure (Azure RBAC). Cette affectation de rôle est gérée en tant que partie intégrante de cette ressource spécifique.

1. Dans le volet de navigation de gauche, sélectionnez **Méthode d’authentification**.  Lisez la description : « Vous pouvez ici définir les numéros de téléphone ainsi que les adresses e-mail dont se servent les utilisateurs pour effectuer l’authentification multifacteur, la réinitialisation de mot de passe en libre-service et la réinitialisation du mot de passe d’un utilisateur. » Si un utilisateur est configuré pour SSPR ou doit utiliser la MFA et qu’en tant qu’administrateur, vous remplissez ce champ, ils seront alors déjà enregistrés et n’auront pas besoin de suivre les étapes d’enregistrement pour SSPR ou la MFA.  Les utilisateurs s’enregistrent souvent eux-mêmes et les administrateurs n’ont besoin de le faire que très rarement.

1. Dans le volet de navigation de gauche, sélectionnez **Connexions**.  Vous pouvez consulter ici les activités de connexion de cet utilisateur.  Rien n’apparaît pour cette utilisatrice, car elle ne s’est pas encore connectée.

1. Cliquez sur le **X** en haut à droite de la page. pour revenir à la liste des utilisateurs.  Avant de fermer la liste des utilisateurs, vous pouvez souligner le fait que la MFA s’affiche en haut de la page.  Sélectionnez **Authentification multifacteur**.  Une nouvelle fenêtre de navigateur s’ouvre.  Ici, vous pouvez sélectionner la MFA groupée pour les utilisateurs.  Il s’agit là d’une des façons d’activer la MFA pour les utilisateurs.  Nous vous montrerons des détails supplémentaires concernant la MFA dans le contexte de l’accès conditionnel, qui offre un contrôle plus granulaire de la MFA.  Fermez l’onglet du navigateur concernant l’authentification multifacteur.

1. Cliquez sur le **X** en haut à droite de la page. Cela vous ramène à la page principale du locataire Contoso.

### Révision

Dans cette démonstration, vous avez montré comment naviguer dans les paramètres d’un utilisateur existant et les groupes auxquels il peut être affecté, la disponibilité des rôles ainsi que l’affectation de licences utilisateur.