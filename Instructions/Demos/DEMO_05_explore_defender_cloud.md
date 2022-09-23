---
ms.openlocfilehash: ecea12b9b90c6dc3917d0ee93edcdba0436ccd0d
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892459"
---
<a name="---"></a><!---
---
Démonstration : Titre : « Microsoft Defender pour le cloud » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft ; Module 2 : Décrire les fonctionnalités de gestion de la sécurité d’Azure ; Unité 3 : Décrire Microsoft Defender pour le cloud »
---
--->

# <a name="demo-microsoft-defender-for-cloud"></a>Démonstration : Microsoft Defender pour le cloud

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft
- Module : Décrire les fonctionnalités de gestion de la sécurité d’Azure
- Unité : Décrire Microsoft Defender pour le cloud

## <a name="demo-scenario"></a>Scénario de la démonstration

Cette démonstration vous permettra de parcourir Microsoft Defender pour le cloud et de montrer comment le Niveau de sécurité Azure peut être utilisé pour améliorer la posture de sécurité d’une organisation.  REMARQUE : Cette démonstration pas à pas suppose que le présentateur dispose d’autorisations de niveau administrateur pour l’abonnement Azure via un Pass Azure.  Un abonnement Azure, comme un abonnement Cloudslice, géré par l’hôte de labo autorisé limite l’accès et les fonctionnalités : certaines étapes ci-dessous peuvent être indisponibles ou ne pas montrer d’informations.

### <a name="demo-setup"></a>Configuration de la démonstration

Dans cette tâche de configuration, vous allez effectuer une configuration de base de Microsoft Defender pour le cloud pour préparer l’abonnement, et activer et affecter une stratégie par défaut. Faites-le avant de faire la démonstration devant la classe. 

1. Ouvrez l’onglet du navigateur intitulé **Accueil-Microsoft Azure**.  Si vous avez fermé l’onglet, ouvrez une page du navigateur et saisissez portal.azure.com dans la barre d’adresse. Ensuite, reconnectez-vous.

1. Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **Microsoft Defender pour le cloud** puis sélectionnez **Microsoft Defender pour le cloud** à partir des résultats de la recherche.

1. Si vous accédez à Microsoft Defender pour le cloud pour la première fois avec votre abonnement, il est possible que la page Bien démarrer s’affiche et qu’une mise à niveau vous soit proposée.  Faites défiler vers le bas de la page, puis sélectionnez **ignorer**.  Vous serez dirigé vers la page Vue d’ensemble.
    1. En haut de la page, vous verrez une zone d’informations bleu clair qui indique « Nous préparons vos abonnements. L’opération peut prendre quelques instants... »
    1. Une fois l’abonnement prêt, une nouvelle zone d’informations apparaît, indiquant « Un abonnement n’a pas de stratégie par défaut affectée. Pour passer en revue la liste des abonnements, ouvrez la page Stratégie de sécurité. »  Sélectionnez la flèche droite à la fin de la phrase.
        1. Vous vous trouvez maintenant dans la page Paramètres de l’environnement. Sélectionnez **Pass Azure - Parrainage**. 
        1. Dans le volet de navigation gauche, sélectionnez **Stratégie de sécurité**.
        1. Dans la page principale, sous Initiative par défaut, sélectionnez **Affecter une stratégie**.
        1. En bas de la page, sélectionnez **Vérifier + Créer**.
        1. En bas de la page, sélectionnez **Créer**.
        1. En haut de la page, sous Microsoft Azure, sélectionnez **Microsoft Defender pour le cloud** depuis la barre de navigation pour revenir à la page Vue d’ensemble.

### <a name="demo-task"></a>Tâche de démonstration

Dans cette tâche de démonstration, vous allez effectuer une présentation très générale de certaines des fonctionnalités de Microsoft Defender pour le cloud.

1. Les informations en haut de la page Vue d’ensemble de Microsoft Defender pour le cloud incluent le nombre d’abonnements Azure, le nombre de ressources évaluées, le nombre de recommandations actives et les éventuelles alertes de sécurité.  Sur le corps de la page s’affichent des cartes qui représentent le niveau de sécurité, la conformité réglementaire, Insights, etc.  

1. Sélectionnez **Ressources évaluées** en haut de la page.  (Remarque : cela équivaut à avoir sélectionné Inventaire dans le volet de navigation gauche de la page d’accueil de Microsoft Defender pour le cloud.)
    1. Cela vous amène à la page **Inventaire** qui affiche votre abonnement de pass Azure.  Sélectionnez **Pass Azure - Parrainage**.
    1. La page Resource Health vous fournit une liste de recommandations.  Dans cette liste, sélectionnez **Plusieurs propriétaires doivent être attribués à votre abonnement**.
    1. Cliquez sur la flèche de déroulement près des étapes de correction. Prenez note de la présence d’étapes de correction détaillées ainsi que de la possibilité de prendre des mesures.  
    1. Sélectionnez **Microsoft Defender pour le cloud** dans l’angle supérieur gauche de l’écran pour revenir à la page de présentation de Microsoft Defender pour le cloud.

1. Sélectionnez **Recommandations actives** en haut de la page.  (Remarque : cela équivaut à avoir sélectionné Recommandations dans le volet de navigation gauche de la page d’accueil de Microsoft Defender pour le cloud.)
    1. La page des recommandations affiche votre tableau de bord de niveau de sécurité.
    1. Sous ce tableau de bord, vous trouvez une liste de contrôles. Chaque contrôle de sécurité représente un risque de sécurité devant être atténué et inclut également des informations sur le niveau maximal associé à ce contrôle, le niveau actuel, l’augmentation potentielle du niveau et l’état d’intégrité de la ressource.  
    1. Sélectionnez l’un des contrôles, par exemple **Activer la MFA**.  Sélectionnez l’un des sous-éléments, par exemple **La MFA doit être activée sur les comptes disposant de droits de propriétaire sur votre abonnement**.  Une page s’ouvre : elle contient une description, les étapes de correction et les ressources concernées. Quittez cette page en cliquant sur le **X** en haut à droite de l’écran.
    1. Quittez la page des recommandations en cliquant sur le **X** en haut à droite de l’écran. Cela vous ramènera à la page de présentation.

1. Vous revenez à la page vue d’ensemble de Microsoft Defender pour le cloud.  Sur la page principale, sélectionnez **Conformité réglementaire**. (Remarque : cela équivaut à avoir sélectionné Recommandations dans le volet de navigation gauche de la page d’accueil de Microsoft Defender pour le cloud.)
    1. La page de conformité réglementaire fournit une liste de contrôles de conformité.  Sous chaque contrôle apparaît une liste d’évaluations fondées sur l’Azure Security Benchmark qui fournit des recommandations quant à la manière de sécuriser vos solutions cloud dans Azure.
    1. Cliquez sur **IM. Gestion d’identité** puis sélectionnez **IM-6 Utiliser des contrôles d’authentification forte**.  La liste indique les mesures concernant la responsabilité assumée par le client pouvant être prises pour améliorer la situation de conformité.
    1. Cliquez sur le **X** en haut à droite de l’écran pour fermer la page et revenir à la page de conformité réglementaire.
    1. Cliquez sur le **X** en haut à droite de l’écran pour revenir à la page de présentation.

1. Rappelons que Microsoft Defender pour le cloud est proposé en deux modes : sans fonctions de sécurité améliorées (gratuit) et avec des fonctions de sécurité améliorées qui sont disponibles dans les plans Microsoft Defender pour le cloud. Vous découvrez ici comment activer/désactiver les différents plans Microsoft Defender pour le cloud.
    1. Dans la page de vue d’ensemble de Microsoft Defender pour le cloud, sélectionnez **Paramètres d’environnement** dans le volet de navigation gauche.
    1. Sélectionnez le signe supérieur **>** en regard de Groupe racine du locataire pour le développer (ne sélectionnez pas directement le groupe racine du locataire, car cela vous dirigera vers une autre page), puis **Pass Azure - Parrainage**
    1. Sur la page Plans Defender, notez comment vous pouvez sélectionner Activer tout ou sélectionner des plans Defender individuels. Laissez les paramètres tels quels avec tous les plans désactivés.
    1. Sélectionnez le **X** dans le coin supérieur droit de l’écran pour revenir à la page Paramètres de l’environnement.
    1. Cliquez sur le **X** en haut à droite de l’écran pour revenir à la page de présentation.

1. Revenez à la page d’accueil du portail Azure en cliquant sur **Accueil** en haut à gauche de la page.  Ne fermez pas cet onglet : vous en aurez besoin plus tard lors d’une autre démonstration.

## <a name="review"></a>Révision

Cette démonstration vous a permis de parcourir Microsoft Defender pour le cloud et de montrer comment le Niveau de sécurité Azure peut être utilisé pour améliorer la posture de sécurité d’une organisation.
