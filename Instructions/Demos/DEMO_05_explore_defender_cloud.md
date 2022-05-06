---
Demo:
  title: Microsoft Defender pour le cloud'
  module: 'Module 3 Lesson 2: Describe the capabilities of Microsoft security solutions: Describe security management capabilities of Azure'
ms.openlocfilehash: b9cf202b9aef7f700b08c1dd6f55444d328fac9a
ms.sourcegitcommit: 25998048c2e354ea23d6f497205e8a062d34ac80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2022
ms.locfileid: "144557336"
---
# <a name="demo-microsoft-defender-for-cloud"></a>Démonstration : Microsoft Defender pour le cloud

## <a name="demo-scenario"></a>Scénario de la démonstration

Cette démonstration vous permettra de parcourir Microsoft Defender pour le cloud et de montrer comment le Niveau de sécurité Azure peut être utilisé pour améliorer la posture de sécurité d’une organisation.

1. Ouvrez l’onglet du navigateur intitulé **Accueil-Microsoft Azure**.  Si vous avez fermé l’onglet, ouvrez une page du navigateur et saisissez portal.azure.com dans la barre d’adresse. Ensuite, reconnectez-vous.

1. Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **Microsoft Defender pour le cloud** puis sélectionnez **Microsoft Defender pour le cloud** à partir des résultats de la recherche.

1. Si vous accédez à Microsoft Defender pour le cloud pour la première fois avec votre abonnement, il est possible que la page Bien démarrer s’affiche et qu’une mise à niveau vous soit proposée.  Faites défiler vers le bas de la page, puis sélectionnez **ignorer**.

1. Notez les informations disponibles sur la page vue d’ensemble de Microsoft Defender pour le cloud.  Remarque : Il est possible qu’une zone d’informations bleue s’affiche en haut de la page. Cela signifie que vous consultez des informations limitées.  Ne cliquez pas dessus : traiter cette requête peut prendre jusqu’à 15 minutes et ne change rien au cours de cette démonstration.

1. Les informations en haut de la page incluent le nombre d’abonnements Azure, le nombre de ressources évaluées, le nombre de recommandations actives et les éventuelles alertes de sécurité.  Sur le corps de la page s’affichent des cartes qui représentent le niveau de sécurité, la conformité réglementaire, Insights, etc.  

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

1. Vous revenez à la page vue d’ensemble de Microsoft Defender pour le cloud.  Depuis la page principale, sélectionnez **Niveau de sécurité** (cela équivaut à sélectionner Niveau de sécurité dans le volet de navigation gauche).
    1. Cela vous amène au tableau de bord du niveau de sécurité,  qui répertorie également tous les groupes d’administration et tous les abonnements disponibles.  Sélectionnez votre abonnement Azure - Pass Azure - Parrainage.
    1. Vous arrivez sur la page des recommandations, qui s’est déjà affichée un peu plus tôt.
    1. Quittez la page des recommandations en cliquant sur le **X** en haut à droite de l’écran.
    1. Quittez la page du niveau de sécurité en cliquant sur le **X** en haut à droite de l’écran. Cela vous ramènera à la page de présentation.

1. Vous revenez à la page vue d’ensemble de Microsoft Defender pour le cloud.  Sur la page principale, sélectionnez **Conformité réglementaire**. (Remarque : cela équivaut à avoir sélectionné Recommandations dans le volet de navigation gauche de la page d’accueil de Microsoft Defender pour le cloud.)
    1. La page de conformité réglementaire fournit une liste de contrôles de conformité.  Sous chaque contrôle apparaît une liste d’évaluations fondées sur l’Azure Security Benchmark qui fournit des recommandations quant à la manière de sécuriser vos solutions cloud dans Azure.
    1. Cliquez sur **IM. Gestion d’identité** puis sélectionnez **IM-6 Utiliser des contrôles d’authentification forte**.  La liste indique les mesures concernant la responsabilité assumée par le client pouvant être prises pour améliorer la situation de conformité.
    1. Cliquez sur le **X** en haut à droite de l’écran pour fermer la page et revenir à la page de conformité réglementaire.
    1. Cliquez sur le **X** en haut à droite de l’écran pour revenir à la page de présentation.

1. Revenez à la page d’accueil du portail Azure en cliquant sur **Accueil** en haut à gauche de la page.  Ne fermez pas cet onglet : vous en aurez besoin plus tard lors d’une autre démonstration.

## <a name="review"></a>Révision

Cette démonstration vous a permis de parcourir Microsoft Defender pour le cloud et de montrer comment le Niveau de sécurité Azure peut être utilisé pour améliorer la posture de sécurité d’une organisation.
