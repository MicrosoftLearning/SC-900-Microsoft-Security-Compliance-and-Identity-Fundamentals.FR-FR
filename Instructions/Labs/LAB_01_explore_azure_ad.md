---
ms.openlocfilehash: e70692d55a6d1ef5d89fde484234bf937cef981d
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892243"
---
<a name="---"></a><!---
---
Labo : Titre : « Découvrir Azure Active Directory » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités d’Azure Active Directory (Azure AD) - Solution Microsoft Entra ; Module 1 : Décrire les services de base et les types d’identités d’Azure AD ; Unité 4 : Décrire les types d’identités Azure AD »
---
--->

# <a name="lab-explore-azure-active-directory"></a>Labo : Découvrir Azure Active Directory

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités d’Azure Active Directory (Azure AD) - Solution Microsoft Entra
- Module : Décrire les services de base et les types d’identités d’Azure AD
- Unité : Décrire les types d’identités Azure AD

## <a name="lab-scenario"></a>Scénario du labo

Dans ce labo, vous accéderez à Azure Active Directory.  En plus, vous créerez un utilisateur et configurerez les différents paramètres, y compris l’ajout de licences.  

**Durée estimée** : 10-15 minutes

### <a name="task-1"></a>Tâche 1

En tant qu’abonné à Microsoft 365, vous utilisez déjà Azure AD.  Lors de cette tâche, vous accéderez à Azure AD via le portail d’administration Microsoft 365 et via le portail Azure.

1. Ouvrez Microsoft Edge.

2. Dans la barre d’adresse, saisissez **admin.microsoft.com** pour accéder au Centre d’administration Microsoft 365.

3. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Saisissez le mot de passe d’administrateur communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

4. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

5. Sous les centres d’administration, sélectionnez **Azure Active Directory** (vous devrez peut-être faire défiler la page).  Une nouvelle page de navigation s’ouvre sur la page Mon tableau de bord du Centre d’administration Azure Active Directory. Depuis les fenêtres principales du tableau de bord, vous verrez plusieurs vignettes, y compris la vignette de l’identité de l’organisation (Contoso, le locataire et l’édition Azure AD), une vignette pour les utilisateurs et groupes, etc.

6. Depuis le volet de navigation à gauche, sélectionnez **Azure Active Directory**.  Dans la fenêtre principale, vous verrez un autre volet de navigation qui contient tous les services disponibles dans Azure AD. À droite, vous verrez les informations à propos du locataire Contoso, des liens vers des types d’identités que vous pouvez créer et des services recommandés.  

7. Ouvrez maintenant une nouvelle fenêtre de navigateur et, dans la barre d’adresse, saisissez **portal.azure.com**.  Comme vous êtes déjà connecté en tant que admin@WWLxZZZZZZ.onmicrosoft.com et que vous avez employé ces mêmes informations d’identification pour utiliser votre Pass Azure, vous devriez être connecté en tant qu’administrateur quand vous accédez au portail Azure.  Vous pouvez vérifier cela en consultant l’e-mail qui apparaît en haut à droite de la page quand vous passez votre souris sur l’icône d’utilisateur.

8. La page d’arrivée du portail Azure affiche les services Azure, y compris Azure Active Directory, les machines virtuelles, les comptes de stockage, les bases de données, etc.  Sélectionnez **Azure Active Directory**.  

9. Vous voyez maintenant Azure Active Directory pour votre locataire Contoso Microsoft 365.    Quelle que soit l’approche que vous utilisez pour accéder aux services Azure Active Directory (le portail d’administration Microsoft 365 ou le portail Azure), vous arrivez au même endroit : le locataire Contoso Azure Active Directory. Ici, vous pouvez gérer tous les services Azure AD.

10. Gardez cet onglet de navigation ouvert pour la tâche suivante.

### <a name="task-2"></a>Tâche 2

Lors de cette tâche, vous apprendrez comment créer un nouvel utilisateur dans Azure Active Directory et vous découvrirez certains services qui peuvent être gérés au niveau de l’utilisateur.

1. Accédez à l’onglet Contoso - Microsoft Azure ouvert dans votre navigateur. Si vous avez fermé l’onglet, ouvrez une page du navigateur et saisissez portal.azure.com dans la barre d’adresse. Ensuite, sélectionnez Azure Active Directory.  Vous devriez être connecté en tant qu’administrateur dans le portail Azure : si ce n’est pas le cas, reconnectez-vous.

2. Dans le volet de navigation de gauche, sélectionnez **Utilisateurs**.  Vous remarquerez que votre locataire est déjà configuré avec des utilisateurs.

3. En haut de la page, sélectionnez **+ Nouvel utilisateur**.

4. **Créer un utilisateur** devrait déjà être sélectionné. S’il ne l’est pas, sélectionnez-le.

5. Remplissez les champs **Identité** de la manière suivante :

    1. Nom d’utilisateur : **sara**.

    2. Champ Nom : **Sara Perez**.

    3. Prénom : **Sara**.

    4. Nom : **Perez**.

6. Remplissez les champs **Mot de passe** de la manière suivante :

    1. Sélectionnez **Me permettre de créer le mot de passe**.

    1. Mot de passe initial : **Naja8996**. Lorsque Sara se connectera pour la première fois, elle sera invitée à modifier son mot de passe.

7. Configurez **Groupes et rôles**.

    1. À côté de Groupes, sélectionnez **0 groupes sélectionnés**.  Cela affiche les groupes disponibles.  Prenez note de la liste des groupes disponibles.

    2. Sélectionnez **Opérations**, vous aurez peut-être besoin de faire défiler la page, puis appuyez sur **Sélectionner**. Notez comment le texte à côté des groupes s’est mis à jour et affiche maintenant 1 groupes sélectionnés.  

    3. À côté de Rôles, sélectionnez **Utilisateur**. La liste des rôles d’annuaire apparaît.  Faites défiler pour afficher les différents rôles intégrés, pour afficher les différents rôles, mais ne modifiez pas le rôle d’utilisateur.  Fermez cette fenêtre en sélectionnant le **X** en haut à droite de l’écran.

8. Configurez les **paramètres**

    1. Bloquer la connexion :  **Non** (conservez le paramètre par défaut).

    1. Emplacement d’utilisation : **États-Unis** (sélectionnez le menu déroulant et faites défiler pour trouver cette option).  La configuration de l’emplacement d’utilisation est nécessaire pour assigner des licences.

9. En bas de la page, sélectionnez le bouton **Créer**.

10. Vérifiez que l’utilisateur apparaît dans la liste d’utilisateurs (les noms sont classés par ordre alphabétique).

11. Depuis la liste d’utilisateurs, sélectionnez l’utilisateur que vous venez de créer, **Sara Perez**.  La page du profil s’ouvre.

12. Le volet de navigation à gauche affiche les différentes options qui peuvent être configurées pour l’utilisateur.  Sélectionnez **Groupes**.  C’est ici que vous pouvez voir des informations supplémentaires concernant le groupe.  Vérifiez que le groupe Opérations apparaît dans la liste (l’affectation de groupe peut prendre quelques minutes à s’afficher).  Remarque : vous verrez également le groupe Contoso, bien que nous n’ayons affecté qu’un groupe lors de la création de l’utilisateur.  C’est le résultat d’une stratégie préconfigurée dans le locataire qui affecte automatiquement les nouveaux utilisateurs au groupe Contoso.

13. Dans le volet de navigation gauche, sélectionnez **Licences**.  Notez qu’il n’y a pas d’affectation de licence trouvée pour cet utilisateur.  

14. Pour ajouter une licence, sélectionnez **+ Affectations** en haut de la fenêtre principale.

15. Sous Sélectionner les licences, sélectionnez **Office 365 E3** et **Windows 10 Entreprise E3**, puis cliquez sur le bouton **Enregistrer** en bas de l’écran. Une notification devrait apparaître en haut à droite de l’écran et afficher la réussite des affectations de licence.

16. Sélectionnez le **X** en haut à droite de l’écran pour fermer la fenêtre Affectations de licence.

17. Sélectionnez **l’icône Actualiser** en haut de la page pour confirmer les affectations de licence.

18. Revenez à la page de vue d’ensemble Azure Active Directory Contoso, en sélectionnant **Contoso** en haut à gauche de l’écran (la barre de navigation), au-dessus de Sara Perez | Licenses.

19. Vous avez créé et configuré un utilisateur dans Azure Active Directory.

20. Déconnectez-vous de tous les onglets de navigation en cliquant sur l’icône d’utilisateur à côté de l’adresse e-mail en haut à droite de l’écran. Ensuite, fermez toutes les fenêtres de navigation.

### <a name="task-3"></a>Tâche 3

Lors de cette tâche, vous vous connecterez pour la première fois en tant que Sara Perez.

1. Ouvrez Microsoft Edge.

2. Dans la barre d’adresse, saisissez **login.microsoft.com**.

3. Connectez-vous en tant que **sara@WWLxZZZZZ.onmicrosoft.com** , (où ZZZZZZ est votre ID de locataire unique fourni par votre fournisseur d’hébergement lab).

4. Saisissez le mot de passe temporaire **Naja8996**.

5. Vous êtes maintenant invité à mettre à jour votre mot de passe. Dans le champ Mot de passe actuel, saisissez **Naja8996**.

6. Dans le champ Nouveau mot de passe, saisissez **SC900-Lab**.  Dans le champ Confirmer le mot de passe, saisissez SC900-Lab, puis sélectionnez Se connecter.  Remarque : en général, il est recommandé d’utiliser un mot de passe plus sécurisé. Ce mot de passe est choisi par commodité et uniquement pour les besoins de ce labo.

7. Vous devez maintenant être connecté à Microsoft 365.

8. **Déconnectez-vous** de tous les onglets de navigation en cliquant sur l’icône d’utilisateur à côté de l’adresse e-mail en haut à droite de l’écran. Ensuite, fermez toutes les fenêtres de navigation.

### <a name="review"></a>Révision

Dans ce labo, vous avez commencé votre découverte d’Azure AD. Puisque les abonnés à Microsoft 365 utilisent automatiquement Azure AD, vous avez découvert que vous accédez aux fonctionnalités et aux services d’Azure AD via le portail d’administration Microsoft 365 ou le portail Azure.  Choisissez l’approche que vous préférez pour accéder au même endroit.  Vous avez vu le processus de création d’un nouvel utilisateur et les différents paramètres qui peuvent être configurés, y compris les groupes auxquels l’utilisateur peut être affecté, la disponibilité des rôles et l’affectation de licences d’utilisateur.
