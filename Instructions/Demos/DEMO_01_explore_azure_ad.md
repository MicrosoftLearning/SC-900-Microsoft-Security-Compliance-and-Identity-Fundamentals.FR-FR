<!---
---
Démo : Titre : « Explorer les paramètres des utilisateurs Microsoft Entra ID » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra ; Module 1 : Décrire la fonction et les types d’identité de Microsoft Entra ID ; Unité 3 : Décrire les types d’identité Microsoft Entra »
---
--->

# Démo : Paramètres utilisateur de Microsoft Entra ID

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra.
- Module : Décrire la fonction et les types d’identité de Microsoft Entra ID.
- Unité : Décrire les types d’identités.

## Scénario de démonstration

Dans cette démo, vous allez accéder à Microsoft Entra ID et passer en revue les différents paramètres pour un utilisateur existant.

1. Ouvrez Microsoft Edge.

1. Dans la barre d’adresse, entrez **admin.microsoft.com** pour accéder au Centre d’administration Microsoft 365.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique communiqué par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Cliquez sur **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous Centres d’administration, sélectionnez **Identité**. (Vous devrez peut-être faire défiler la page vers le bas.)  Une nouvelle page de navigateur s’ouvre sur la page de présentation du centre d’administration Microsoft Entra. Ici, vous voyez les informations de base de votre locataire Contoso. Si vous faites défiler la fenêtre principale vers le bas, vous voyez également des informations sur les alertes, mon flux, les fonctionnalités en vedette, etc.  
    1. Remarque à l’attention du présentateur ou de l’instructeur : vous pouvez également accéder directement au centre d’administration de Microsoft Entra en vous rendant sur **[entra.microsoft.com](https://entra.microsoft.com)**.

1. Dans le volet de navigation gauche, développez **Utilisateurs**, puis sélectionnez **Tous les utilisateurs**.  Sur la page des utilisateurs, vous pouvez voir des options de navigation supplémentaires et la liste des utilisateurs. Votre locataire est déjà configuré avec des utilisateurs.

1. Dans la liste des utilisateurs, sélectionnez **Adele Vance**.

1. Notez que dans le volet de navigation de gauche, l’option **Vue d’ensemble** est surlignée en gris clair.  Montrez les informations affichées sur la page de vue d’ensemble et parlez-en.  Sélectionnez l’onglet **Surveillance** en haut de la page qui affiche les connexions des utilisateurs. (Aucune connexion n’est affichée, sauf si vous vous êtes déjà connecté en tant qu’Adele Vance.)  Sélectionnez ensuite **Propriétés** pour afficher toutes les propriétés de l’objet utilisateur Adele Vance.

1. Dans le volet de navigation de gauche, sélectionnez **Rôles affectés**.  Aucun rôle administratif n’a été attribué à cet utilisateur.  En haut de la page, sélectionnez **+ Ajouter des affectations**, puis, sur la page d’ajout d’affectations, développez le champ Rechercher un rôle sous Sélectionner un rôle pour afficher une liste des types de rôles d’administration disponibles.  N’ajoutez aucun rôle, fermez simplement la page en sélectionnant le **X** en haut à droite de la page.

1. Dans le volet de navigation de gauche, sélectionnez **Groupes**.  Indiquez que cet utilisateur est membre de plusieurs groupes.  Vous pouvez parler ici des types de groupes.  Pour ajouter cet utilisateur à d’autres groupes, sélectionnez **+ Ajouter des appartenances**.  N’ajoutez aucun nouveau groupe : expliquez simplement à quel point il est facile d’ajouter un utilisateur à des groupes existants. Fermez la fenêtre Sélectionner des groupes en cliquant sur le **X** en haut à droite de la page.

1. Dans le volet de navigation de gauche, sélectionnez **Licences**. Remarquez que cet utilisateur se voit affecter des licences Microsoft 365 E5 et une licence EMS.  Pour ajouter une licence, sélectionnez **+ Affectations** en haut de la fenêtre principale.  Affichez les licences de cet utilisateur. Ne changez RIEN.  Fermez cette fenêtre en cliquant sur le **X** en haut à droite de la page.

1. Dans le volet de navigation gauche, sélectionnez **Appareils**.  Rien ne s’affiche, mais expliquez que si des périphériques étaient affectés à cet utilisateur, c’est ici qu’ils s’afficheraient.

1. Dans le volet de navigation de gauche, sélectionnez **Affectations de rôles Azure**.  Signalez les points suivants :
    1. Cet onglet est différent de l’onglet des rôles affectés présenté précédemment, dans la mesure où ce dernier concerne le contrôle d’accès basé sur les rôles dans Microsoft Entra.
    1. Bien que rien ne soit répertorié ici, c’est l’onglet où vous seriez en mesure de voir les affectations de rôles, affectées à Adele, pour les ressources Azure. Par exemple, si vous créez un groupe de ressources Azure et que vous affectez à Adele un rôle spécifique, propriétaire ou contributeur du groupe de ressources entre autres, vous verrez ce rôle ici. Cela fait partie du contrôle d’accès basé sur les rôles d’Azure (Azure RBAC). Cette affectation de rôle est ajoutée et gérée dans le cadre de cette ressource spécifique.

1. Sélectionnez le **X** en haut à droite pour fermer la page. Cette opération vous renvoie à la liste des utilisateurs.

1. Sélectionnez le **X** en haut à droite pour fermer la page. Cette opération vous renvoie à la page principale du centre d’administration de Microsoft Entra.

1. Gardez cet onglet ouvert, car vous l’utilisez dans la prochaine démo.

### Révision

Dans cette démonstration, vous avez présenté les paramètres d’un utilisateur existant et les groupes auxquels il peut être affecté, les rôles disponibles ainsi que l’attribution de licences utilisateur.
