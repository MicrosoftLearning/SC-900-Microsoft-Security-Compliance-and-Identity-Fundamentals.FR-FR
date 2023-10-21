<!---
---
Démonstration : Titre : « Explorer les paramètres utilisateur de Microsoft Entra ID » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra ; Module 1 : Décrire la fonction et les types d’identité de Microsoft Entra ID ; Unité 3 : Décrire les types d’identité Microsoft Entra »
---
--->

# Démonstration : Paramètres utilisateur de Microsoft Entra ID

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra.
- Module : Décrire la fonction et les types d’identité de Microsoft Entra ID.
- Unité : Décrire les types d’identité.

## Scénario de la démonstration

Dans cette démonstration, vous allez accéder à Microsoft Entra ID et passer en revue les différents paramètres pour un utilisateur existant.

1. Ouvrez Microsoft Edge.

1. Dans la barre d’adresse, entrez **admin.microsoft.com** pour accéder au Centre d’administration Microsoft 365.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous Centres d’administration, sélectionnez **Identité** (vous devez peut-être faire défiler la page vers le bas).  Une nouvelle page de navigateur s’ouvre sur la page de présentation du centre d’administration Microsoft Entra. Ici, vous voyez les informations de base de votre locataire Contoso. Si vous faites défiler la fenêtre principale vers le bas, vous voyez également des informations sur les alertes, mon flux, les fonctionnalités en vedette, etc.  
    1. Remarque pour le présentateur/formateur : vous pouvez également accéder directement au centre d’administration de Microsoft Entra via **[entra.microsoft.com](https://entra.microsoft.com)** .

1. Dans le volet de navigation gauche, développez **Utilisateurs**, puis sélectionnez **Tous les utilisateurs**.  La page Utilisateurs contient des options de navigation supplémentaires et la liste des utilisateurs. Votre locataire est déjà configuré avec des utilisateurs.

1. Dans la liste des utilisateurs, sélectionnez **Adele Vance**.

1. Dans le volet de navigation de gauche, l’option **Vue d’ensemble** est mise en surbrillance en gris clair.  Montrez et expliquez les informations affichées sur la page de présentation.  Sélectionnez l’onglet **Surveillance** en haut de la page qui affiche les connexions utilisateur (aucune connexion ne s’affiche, sauf si vous vous êtes précédemment connecté en tant qu’Adele Vance).  Sélectionnez ensuite **Propriétés** pour afficher toutes les propriétés de l’objet utilisateur Adele Vance.

1. Dans le volet de navigation de gauche, sélectionnez **Rôles affectés**.  Aucun rôle administratif n’a été attribué à cet utilisateur.  En haut de la page, sélectionnez **+ Ajouter des attributions**, puis, dans la page Ajouter des attributions, développez le champ Rechercher un rôle sous Sélectionner un rôle pour afficher la liste des types de rôles d’administration disponibles.  N’en ajoutez aucun : fermez simplement la page en cliquant sur le **X** en haut à droite.

1. Dans le volet de navigation gauche, sélectionnez **Groupes**.  Expliquez qu’un utilisateur est membre de plusieurs groupes.  Vous pouvez ici aborder les types de groupes.  Pour ajouter cet utilisateur à d’autres groupes, sélectionnez **+ Ajouter des appartenances**.  N’ajoutez aucun nouveau groupe : expliquez simplement à quel point il est facile d’ajouter un utilisateur à des groupes existants. Fermez la fenêtre Sélectionner des groupes en sélectionnant la croix (**X**) dans le coin supérieur droit de la page.

1. Dans le volet de navigation de gauche, sélectionnez **Licences**. Vous remarquerez que des licences Microsoft 365 E5 et EMS ont été affectées à cet utilisateur.  Pour ajouter une licence, sélectionnez **+ Affectations** en haut de la fenêtre principale.  Affichez les licences disponibles pour cet utilisateur. Ne changez RIEN.  Fermez cette fenêtre en cliquant sur le **X** en haut à droite de la page.

1. Dans le volet de navigation gauche, sélectionnez **Appareils**.  Rien ne s’affiche : vous pouvez cependant expliquer que c’est ici que les appareils affectés à l’utilisateur s’afficheraient s’il y en avait.

1. Dans le volet de navigation de gauche, sélectionnez **Attributions de rôles Azure**.  Expliquez
    1. qu’il s’agit d’un onglet différent de celui des rôles attribués montré auparavant, car l’onglet montré plus tôt était réservé au contrôle d’accès en fonction du rôle dans Microsoft Entra.
    1. Bien que rien ne soit répertorié ici, il s’agit de l’onglet dans lequel vous pouvez afficher les attributions de rôles, attribuées à Adele, pour les ressources Azure. Par exemple, si vous créez un groupe de ressources Azure et que vous affectez un rôle spécifique à Adele tel que propriétaire ou contributrice du groupe de ressources, c’est ici que ce rôle apparaîtrait. Cela fait partie du contrôle d’accès en fonction du rôle Azure (Azure RBAC). Cette attribution de rôle est ajoutée et gérée en tant que partie intégrante de cette ressource spécifique.

1. Dans le volet de navigation de gauche, sélectionnez **Méthode d’authentification**.  Lisez la description : « Vous pouvez ici définir les numéros de téléphone ainsi que les adresses e-mail dont se servent les utilisateurs pour effectuer l’authentification multifacteur, la réinitialisation de mot de passe en libre-service et la réinitialisation du mot de passe d’un utilisateur. » Si un utilisateur est configuré pour la réinitialisation de mot de passe en libre-service (SSPR) ou doit utiliser l’authentification multifacteur (MFA) et que vous, en tant qu’administrateur, vous remplissez ces informations, il sera alors déjà inscrit et n’aura pas besoin d’effectuer les étapes d’inscription pour la SSPR ou la MFA.  Les utilisateurs s’inscrivent généralement eux-mêmes et les administrateurs n’ont besoin de le faire que rarement.

1. Cliquez sur le **X** en haut à droite de la page. pour revenir à la liste des utilisateurs.

1. Cliquez sur le **X** en haut à droite de la page. Vous revenez à la page principale du centre d’administration Microsoft Entra.

1. Laissez cet onglet de navigateur ouvert pour l’utiliser lors de la prochaine démonstration.

### Révision

Dans cette démonstration, vous avez présenté les paramètres d’un utilisateur existant et les groupes auxquels il peut être affecté, les rôles disponibles ainsi que l’attribution de licences utilisateur.
