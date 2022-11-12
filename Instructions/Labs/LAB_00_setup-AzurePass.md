---
ms.openlocfilehash: c4ec8d47505dc2feec2c42433278e03cc6f83740
ms.sourcegitcommit: 804b98d288b1db2c11a5154b4ded954e87f5ae55
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2022
ms.locfileid: "148119021"
---
<a name="---"></a><!---
---
Labo : Titre : « Installation »
---
--->

# <a name="lab-setup"></a>Labo : Installation

## <a name="lab-scenario"></a>Scénario du labo

Ce labo d’installation se compose de deux tâches distinctes.  La première tâche s’applique et est recommandée seulement si votre environnement lab inclut l’utilisation d’un Pass Azure. La deuxième tâche est axée sur l’activation du journal d’audit Microsoft.

**Durée estimée** : 5-10 minutes



### <a name="setup-part-1---redeem-azure-pass"></a>Partie 1 de la configuration - Utiliser un Pass Azure

Cette tâche s’applique et est recommandée seulement si l’environnement lab que vous utilisez inclut un Pass Azure. Dans cette tâche, vous allez utiliser votre Pass Azure avec les mêmes informations d’identification que votre locataire Microsoft 365.  Vous bénéficiez ainsi d’une expérience plus fluide lorsque vous basculez entre Microsoft 365 et Azure.

1. Si vous avez des fenêtres de navigation ouvertes, il est recommandé de fermer tous les navigateurs.

1. Effectuez un clic droit sur l’icône Microsoft Edge et sélectionnez **Nouvelle fenêtre InPrivate** pour ouvrir une nouvelle session de navigation InPrivate.

1. Dans la barre d’adresse, saisissez **www.microsoftazurepass.com**.  

1. Sélectionnez le bouton **démarrer** pour commencer.

    1. Dans la fenêtre de connexion, entrez l’e-mail **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Saisissez le mot de passe d’administrateur communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.  Si vous êtes invité à rester connecté, sélectionnez **Oui**.
    1. Sélectionnez **Confirmer le compte Microsoft** si la bonne adresse e-mail est indiquée.
    1. Saisissez votre code promo dans la barre du code promo et cliquez sur **Réclamer le code promo**.  
    1. Sur la page « Votre profil », conservez toutes les informations par défaut, sélectionnez **J’accepte le contrat d’abonnement, les détails de l’offre, et la déclaration de confidentialité**. Sélectionnez ensuite **S’inscrire**.
    1. Si une fenêtre de sondage s’ouvre, vous pouvez la fermer en sélectionnant le **X** ou y répondre comme il convient avant de sélectionner **Soumettre**.

1. L’activation de votre compte peut prendre plusieurs minutes.  Une fois qu’il est activé, vous êtes redirigé vers la page d’accueil du portail Azure. Une fenêtre Bienvenue dans Microsoft Azure s’ouvre. Sélectionnez **Peut-être plus tard**. Il se peut que la fenêtre contextuelle « Optimisez vos charges de travail en cloud grâce à des recommandations personnalisées » s’ouvre. Sélectionnez le **X** en haut à droite de la fenêtre.

1. Laissez l’onglet de la page d’accueil du portail Azure ouvert. Vous y reviendrez lors de la démonstration suivante.

### <a name="setup-part-2---enable-microsoft-365-audit-log"></a>Partie 2 de la configuration - Activer le journal d’audit de Microsoft 365

Lors de cette tâche de configuration, vous activerez la fonction de journal d’audit dans Microsoft 365.  Bien que la documentation indique que le journal d’audit est activé par défaut, la plupart des locataires de labo n’ont pas cette fonctionnalité activée. Il peut se passer plusieurs heures avant que l’activation ne fasse effet.  Il est utile d’activer cette fonctionnalité, car Microsoft 365 utilise les journaux d’audit pour les informations concernant les utilisateurs, les activités identifiées dans les stratégies et les informations concernant les analyses.

1. Ouvrez Microsoft Edge. Saisissez **admin.microsoft.com** dans la barre d’adresse.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Saisissez le mot de passe d’administrateur communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**. Vous accédez ainsi à la page du Centre d’administration Microsoft 365.

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous les Centres d’administration, sélectionnez **Conformité**.  Le navigateur ouvre une nouvelle page : il s’agit de la page d’accueil du Centre de conformité Microsoft 365.  

1. Dans le volet de navigation à gauche, sélectionnez **Audit**.  Remarque : la fonctionnalité d’audit est également accessible depuis la page d’accueil de Microsoft 365 Defender (précédemment dénommé Centre de sécurité Microsoft 365).

1. Vérifiez que l’onglet **Recherche** est sélectionné (souligné).

1. Quand vous arrivez sur la page Audit, attendez 2 à 3 minutes.  Si Audit n’est PAS activé, vous verrez une barre bleue en haut de la page qui indique Commencer à enregistrer les activités des utilisateurs et des administrateurs.  Sélectionnez **Commencer à enregistrer les activités des utilisateurs et des administrateurs**.  Si vous êtes invité à confirmer que le paramètre de l’organisation doit être mis à jour, sélectionnez **Oui**. Une fois que l’audit est activé, la barre bleue disparaît.  S’il n’y a pas de barre bleue, alors l’audit est déjà activé et aucune autre action n’est nécessaire.  Vous pouvez également vérifier si l’audit est activé en passant par PowerShell, mais cela n’entre pas dans le cadre de ce cours.

1. Retournez à la page d’accueil du Centre de conformité Microsoft 365 en sélectionnant **Accueil** depuis le volet de navigation à gauche.

### <a name="review"></a>Révision

Lors de cette configuration, vous avez utilisé votre Pass Azure avec les mêmes informations d’identification que votre locataire Microsoft 365.  Vous avez aussi activé la fonction de journal d’audit dans Microsoft 365.
