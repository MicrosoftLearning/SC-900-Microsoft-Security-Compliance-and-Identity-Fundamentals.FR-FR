---
ms.openlocfilehash: 7f6827f55ddc30dac37ab7da750a9331477650f1
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892422"
---
<a name="---"></a><!---
---
Démonstration : Titre : « Étiquettes de confidentialité dans Microsoft Purview » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft ; Module 3 : Décrire la protection des informations et la gestion du cycle de vie des données dans Microsoft Purview ; Unité 4 : Décrire les étiquettes de confidentialité »
---
--->

# <a name="demo-sensitivity-labels-in-microsoft-purview"></a>Démonstration : Étiquettes de confidentialité dans Microsoft Purview

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft
- Module : Décrire la protection des informations et la gestion de cycle de vie des données dans Microsoft Purview
- Unité : Décrire les étiquettes de confidentialité

## <a name="demo-scenario"></a>Scénario de la démonstration

Lors de cette démonstration, vous présenterez les fonctionnalités des étiquettes de confidentialité.  Vous expliquerez les paramètres des étiquettes de confidentialité existantes qui ont été créées et la stratégie correspondante pour publier l’étiquette.   Ensuite, vous verrez comment appliquer une étiquette et l’effet de celle-ci, depuis la perspective d’un utilisateur.  **REMARQUE** : La première fois que vous utilisez Word en ligne avec votre locataire Microsoft 365, l’option Sensibilité peut apparaître sur le ruban au bout de 15 minutes.  Les présentateurs doivent exécuter la partie 2 de la démonstration avant la classe afin que le délai soit suffisant pour que l’option s’affiche.

### <a name="demo-part-1"></a>Partie 1 de la démonstration

Lors de cette démonstration, vous présentez les paramètres d’une étiquette de confidentialité existante et la stratégie correspondante pour la publier.

1. Ouvrez Microsoft Edge. Saisissez **admin.microsoft.com** dans la barre d’adresse.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Saisissez le mot de passe d’administrateur communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**. Vous accédez ainsi à la page du Centre d’administration Microsoft 365.

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous les Centres d’administration, sélectionnez **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.  

1. Dans le volet de navigation situé à gauche du portail de conformité Microsoft Purview, sélectionnez **Tout afficher**.

1. Dans le volet de navigation à gauche, sélectionnez **Protection des données**.

1. La zone d’informations jaune indique que votre organisation n’a pas activé la capacité à traiter du contenu dans des fichiers Office en ligne qui disposent d’étiquettes de confidentialité chiffrées appliquées et qui sont enregistrées dans OneDrive et SharePoint.  Sélectionnez **Activer maintenant**.  Une fois activé, il peut y avoir un délai avant que le paramètre ne soit propagé à travers le système.

1. Vérifiez que l’onglet **Étiquettes** situé en haut de la page est sélectionné (souligné).

1. Au milieu de la page, notez comment trois étiquettes sont déjà créées.  Sélectionnez **Confidentiel - Finance**.  Une fenêtre avec des informations à propos de cette étiquette s’ouvre.  Remarquez comment cette étiquette est définie pour prendre en charge le chiffrement et le marquage de contenu.  Sélectionnez **Modifier l’étiquette** en haut de la page pour afficher certains des paramètres de base.

    1. Vous commencez la configuration en fournissant un nom et une description pour votre étiquette.  Ne changez rien.  Sélectionnez **Suivant** au bas de la page.

    1. Notez l’étendue de cette étiquette.  L’étendue est définie sur Fichiers et e-mails, ce qui vous permet de configurer les paramètres de chiffrement et de marquage de contenu afin de protéger les e-mails et les fichiers du bureau étiquetés.  Ne changez rien.  Sélectionnez **Suivant** au bas de la page.

    1. Pour l’étendue sélectionnée, Fichiers et e-mails, vous pouvez décider de chiffrer et/ou de marquer le contenu.  Notez comment les paramètres de protection pour les fichiers et les e-mails sont définis à la fois pour le chiffrement et pour le marquage du contenu des fichiers.  Passez en revue la définition de chacun d’entre eux.  Ne changez rien.  Sélectionnez **Suivant** au bas de la page.

    1. La fenêtre de chiffrement affiche la configuration pour les paramètres de chiffrement.  Ne changez rien.  Passez en revue la zone d’informations sous Configuration des paramètres de chiffrement ainsi que les paramètres configurés. Notez comment l’accès utilisateur au contenu est défini pour ne jamais expirer.  Vous pouvez aussi attribuer des autorisations à des utilisateurs et groupes spécifiques afin qu’ils puissent interagir avec le contenu auquel cette étiquette est appliquée.  Le locataire est défini sous Utilisateurs et groupes. Ainsi, tous les utilisateurs de votre locataire peuvent afficher le contenu qui dispose de cette étiquette.  L’équipe responsable des finances apparaît également et ses membres disposent d’autorisations pour co-éditer.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.

    1. Sur la page de marquage de contenu, remarquez la zone d’informations en haut de l’écran.  Les marquages de contenu seront appliqués aux documents, mais uniquement les en-têtes et les pieds de page seront appliqués aux e-mails. En d’autres termes, les filigranes ne sont pas appliqués aux e-mails.  Le marquage de contenu associé à cette étiquette est un filigrane.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.

    1. Vous êtes à présent dans la fenêtre d’étiquetage automatique pour les fichiers et les e-mails.  Lisez la description de l’étiquetage automatique en haut de la page ainsi que la zone d’informations en dessous.  Notez également que cette étiquette est définie pour l’étiquetage automatique sous certaines conditions. Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.

    1. La prochaine fenêtre définit les paramètres de protection pour les équipes, les groupes et les sites pour lesquels cette étiquette est appliquée. Ce n’est pas activé, sélectionnez **Suivant** au bas de la page.

    1. La prochaine fenêtre est un aperçu de la fonctionnalité qui permet d’appliquer automatiquement cette étiquette aux colonnes de la base de données d’Azure (comme SQL, Synapse, etc.) qui contiennent les types d’informations sensibles que vous choisissez.  Cette fonctionnalité n’est pas activée. Sélectionnez **Annuler** en bas de la page pour quitter l’assistant de configuration de l’étiquette et retourner à la page de protection des données.

1. En haut de la page de protection des données, sélectionnez **Stratégies d’étiquettes**.  C’est au travers des stratégies d’étiquettes que les étiquettes de confidentialité peuvent être publiées.  

1. Sélectionnez **Confidentiel-Stratégie financière**.  Une fenêtre avec des informations à propos de la stratégie s’ouvre.  Cette stratégie sert à publier les étiquettes Confidentiel-Stratégie financière et à protéger les données qui contiennent les données financières pour Contoso.  Remarquez également comment cette stratégie est publiée pour tous.  

1. Sélectionnez **Modifier** la stratégie en haut de la fenêtre.

    1. Lisez la description sous « Choisir les étiquettes de confidentialité à publier ».  Notez l’étiquette qui est indiquée.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.

    1. Lisez la description sous « Publier aux utilisateurs et groupes ».  Notez que cette étiquette est disponible pour tous les utilisateurs.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.

    1. Passez en revue les paramètres de stratégie.  Ne modifiez pas les paramètres.  Sélectionnez **Suivant** au bas de la page.

    1. La dernière option de configuration consiste à nommer votre stratégie.  Ne modifiez pas les paramètres.  Sélectionnez **Annuler** en bas de la page pour quitter la configuration de la stratégie et retourner à la page de protection des données.

1. Depuis la page de protection des données, sélectionnez l’étiquetage automatique.  Il n’y a pas de stratégie d’étiquetage automatique configurée.  Ne modifiez pas les paramètres.  Si vous vous demandez pourquoi il n’y a pas de stratégie ici, alors que la configuration d’étiquette est définie sur étiquetage automatique pour les fichiers et les e-mails, revenez aux étapes où vous avez parcouru les paramètres de configuration d’étiquette. Passez en revue les descriptions et les zones d’informations associées à l’étiquetage automatique pour les fichiers et les e-mails.  Conseil :  Dans l’onglet d’étiquetage automatique pour le labo de confidentialité, il est indiqué :  « Afin d’appliquer automatiquement cette étiquette aux fichiers qui sont déjà enregistrés (dans SharePoint ou OneDrive) ou aux e-mails qui ont déjà été traités par Exchange, vous devez créer une stratégie d’étiquetage automatique. »

1. Dans le volet de navigation de gauche, sélectionnez Accueil pour revenir au portail de conformité Microsoft Purview.

1. Laissez cette page ouverte, vous en aurez besoin pour la tâche suivante.

### <a name="demo-part-2"></a>Partie 2 de la démonstration

Lors de cette étape, vous présenterez le processus d’application d’une étiquette depuis la perspective d’un utilisateur (dans ce cas-ci, l’utilisateur est l’administrateur) et afficherez le marquage de contenu qui est généré par l’étiquette.

1. Dans la page d’accueil du portail de conformité Microsoft Purview, sélectionnez l’icône **Lanceur d’application**, à côté de l’indication Contoso Electronics. **cliquez avec le bouton droit sur l’icône Word**  et sélectionnez **Ouvrir dans un nouvel onglet**.  

1. Sélectionnez **+ Nouveau document**, puis saisissez du texte sur la page.  Sur la barre bleue en haut de la page, sélectionnez la flèche vers le bas à côté de DocumentXX - Enregistré et, dans la barre du nom du fichier, saisissez **Étiquette de test**.

1. Dans la barre de menu supérieure, sélectionnez **Sensibilité**. Si vous ne voyez pas immédiatement cette option, réactualisez la page. À partir du menu déroulant, sélectionnez **Confidentiel - Finance**.

1. Dans la barre de menu supérieure, sélectionnez **Affichage**, puis sélectionnez **Mode lecture**.

1. Notez comment le document inclut le filigrane.  

1. Fermez les onglets Microsoft Word qui sont ouverts dans votre navigateur pour quitter Word.

### <a name="demo-part-3-optional"></a>Partie 3 de la démonstration (facultative)

En plus du marquage de contenu, le paramètre de protection d’étiquette a été défini pour le chiffrement. Grâce à la configuration des autorisations qui ont été accordées pour cette étiquette, les membres du groupe responsable des finances peuvent co-éditer les documents qui disposent de cette étiquette et les utilisateurs dans le locataire Contoso peuvent les voir (ou n’importe quel document ou e-mail qui dispose de cette étiquette).  Dans cette section, vous enverrez ce document à une adresse e-mail à laquelle vous avez accès (par exemple une adresse personnelle ou votre e-mail Microsoft) et qui ne fait PAS partie du domaine WWLxZZZZ.OnMicrosoft.com. Voyez ensuite ce qu’il se passe quand vous essayez d’ouvrir la pièce jointe.  

1. Dans la page d’accueil du portail de conformité Microsoft Purview, sélectionnez l’icône **Lanceur d’application**, à côté de l’indication Contoso Electronics. **cliquez avec le bouton droit sur l’icône Outlook** et sélectionnez **Ouvrir dans un nouvel onglet**.

1. En haut à gauche de l’écran, sélectionnez **Nouveau message**.  Saisissez une adresse e-mail à laquelle vous avez accès et qui ne fait pas partie du domaine WWLxZZZZ.OnMicrosoft.com et saisissez **Test** dans la ligne d’objet.

1. Sélectionnez **Attacher**.

1. Sélectionnez **Parcourir les emplacements cloud**.

1. À partir de la liste qui apparaît, sélectionnez le document que vous avez créé et auquel vous avez appliqué l’étiquette **Étiquette de test**. Sélectionnez **Suivant**, puis **Joindre en tant que copie**.  Appuyez sur **Envoyer**.

1. Consultez l’adresse e-mail à laquelle vous avez envoyé le document.  Notez que l’e-mail peut être envoyé directement dans votre dossier Courrier indésirable.  Lorsque vous essayez d’ouvrir le fichier Word joint, une notification s’affiche et vous indique que vous ne disposez pas de l’autorisation pour ouvrir ce document.

1. Fermez les onglets de votre navigateur.

### <a name="review"></a>Révision

Lors de cette démonstration, vous avez présenté les étiquettes de confidentialité.  Vous avez présenté les paramètres des étiquettes de confidentialité existantes qui avaient déjà été créées et la stratégie correspondante pour publier l’étiquette. Ensuite, vous avez présenté comment appliquer une étiquette et l’effet de celle-ci, depuis la perspective d’un utilisateur.
