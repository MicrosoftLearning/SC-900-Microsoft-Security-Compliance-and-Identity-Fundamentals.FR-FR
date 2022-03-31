---
Demo:
  title: Réinitialisation de mot de passe en libre-service dans Azure Active Directory
  module: 'Module 2 Lesson 2: Describe the capabilities of Microsoft Identity and access management solutions: Describe the different authentication methods of Azure AD'
ms.openlocfilehash: 8b5ab5e9ba2670841d8bcf897cbfb4f6e76c9265
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/14/2022
ms.locfileid: "137894149"
---
# <a name="demo-azure-active-directory-self-service-password-reset-sspr"></a>Démonstration : Réinitialisation de mot de passe en libre-service (SSPR) dans Azure Active Directory

### <a name="demo-scenario"></a>Scénario de la démonstration

Cette démonstration vous permettra de parcourir les divers paramètres associés à l’activation de la réinitialisation de mot de passe en libre-service.

1. Accédez à l’onglet Contoso - Microsoft Azure ouvert dans votre navigateur. Si vous avez fermé l’onglet, ouvrez une page du navigateur et saisissez portal.azure.com dans la barre d’adresse. Ensuite, sélectionnez Azure Active Directory. Vous devriez être connecté en tant qu’administrateur dans le portail Azure : si ce n’est pas le cas, reconnectez-vous.

1. Dans le volet de navigation de gauche, sélectionnez Réinitialisation de mot de passe.

1. L’onglet des propriétés apparaît en surbrillance.  Dans la fenêtre Propriétés, vous remarquerez que SSPR peut être activé pour Aucun, Sélectionné ou Tous.
    1. Survolez l’icône d’information près de l’intitulé « Réinitialisation de mot de passe activée » avec votre curseur. Expliquez que vous pouvez choisir « Sélectionné » pour limiter la réinitialisation de mot de passe à un groupe limité d’utilisateurs, ou encore choisir Aucun ou Tous.
    1. Survolez l’icône d’information près de l’intitulé « Sélectionner un groupe » avec votre curseur et expliquez que c’est ici que vous identifiez le groupe d’utilisateurs autorisés à réinitialiser leurs propres mots de passe.   Vous devez inclure des utilisateurs dans le groupe : vous ne pouvez pas sélectionner des utilisateurs de manière individuelle.  En outre, si vous changez de groupe, celui que vous sélectionnez remplace alors le groupe actuellement répertorié.  C’est pourquoi il est conseillé de simplement ajouter des utilisateurs au groupe SSPR.
    1. Vous remarquerez qu’une zone d’informations bleu clair s’affiche. Expliquez la raison de sa présence aux participants : elle précise que ces paramètres s’appliquent uniquement aux utilisateurs finaux dans l’organisation. Les administrateurs bénéficient toujours du libre-service pour la réinitialisation de leur mot de passe, et doivent utiliser deux méthodes d’authentification pour réinitialiser leur mot de passe.

1. Dans le volet de navigation de gauche de la réinitialisation de mot de passe, sélectionnez Méthodes d’authentification.
    1. Survolez l’icône d’information près de l’intitulé « Nombre de méthodes nécessaires à la réinitialisation » avec votre curseur.  Expliquez que cette option permet de définir le nombre de méthodes d’identification alternatives qu’un utilisateur dans ce répertoire doit disposer pour réinitialiser son mot de passe.   Ne modifiez pas ce paramètre.
    1. Expliquez les différentes « méthodes à la disposition des utilisateurs » et précisez notamment que SSPR prend en charge les questions de sécurité. Sélectionnez Questions de sécurité pour afficher les options d’utilisation des questions de sécurité. Une fois vos explications à ce propos terminées, revenez en arrière et sélectionnez Questions de sécurité afin de retirer la coche.

1. Dans le volet de navigation gauche de la réinitialisation de mot de passe, sélectionnez Enregistrement.
    1. Survolez l’icône d’information près de l’intitulé « Exiger l’enregistrement des utilisateurs lors de leur connexion » avec votre curseur.   Expliquez cela aux utilisateurs.  
    1. Survolez l’icône d’information près de l’intitulé « Nombre de jours avant que les utilisateurs ne doivent confirmer de nouveau leurs informations d’authentification » avec votre curseur.   Expliquez cela aux utilisateurs.  

1. Dans le volet de navigation gauche de la réinitialisation de mot de passe, sélectionnez Notifications.  Survolez l’icône d’information avec votre curseur pour obtenir une description et expliquez les deux paramètres.

1. Prenez note de la manière dont le volet de navigation de la réinitialisation de mot de passe inclut également des options servant à afficher les journaux d’audit ainsi que les informations et données d’utilisation.

1. Cliquez sur le X en haut à droite de la page. Cela vous ramène à la page principale du locataire Contoso.

1. Gardez cette page du navigateur ouverte pour la démonstration suivante.

#### <a name="review"></a>Révision

Dans cette démonstration, vous avez montré les paramètres associés à la réinitialisation de mot de passe en libre-service. 

