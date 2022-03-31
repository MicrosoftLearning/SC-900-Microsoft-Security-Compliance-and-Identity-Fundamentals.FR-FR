---
lab:
  title: Explorer Microsoft Defender pour le cloud
  module: 'Module 3 Lesson 2: Describe the capabilities of Microsoft security solutions: Describe security management capabilities of Azure'
ms.openlocfilehash: 208e11a7e82497fbb900b4fa024fb6fb367d458e
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/14/2022
ms.locfileid: "137893992"
---
# <a name="lab-explore-microsoft-defender-for-cloud"></a>Labo : Explorer Microsoft Defender pour le cloud

## <a name="lab-scenario"></a>Scénario du labo
Dans ce labo, vous allez découvrir Microsoft Defender pour le cloud et apprendre à utiliser le Niveau de sécurité Azure pour améliorer la posture de sécurité de votre organisation.

**Durée estimée** : 30 minutes

#### <a name="task-1-in-this-task-you-will-take-a-brief-tour-of-microsoft-defender-for-cloud"></a>Tâche 1 : Dans cette tâche, vous allez faire une brève visite de Microsoft Defender pour le cloud.
1.  Ouvrez Microsoft Edge. Dans la barre d’adresse, saisissez **portal.azure.com**.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Saisissez le mot de passe d’administrateur communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Dans le coin supérieur gauche de l’écran, en regard de l’endroit où Microsoft Azure est indiqué, sélectionnez l’icône de menu Afficher le portail (les trois lignes horizontales également appelées « icône hamburger ») puis, dans le volet de navigation gauche, sous Favoris, sélectionnez **Microsoft Defender pour le cloud**.  S’il n’est pas répertorié sous Favoris, dans la zone de recherche, entrez **Microsoft Defender pour le cloud**, puis dans la liste des résultats, sélectionnez **Microsoft Defender pour le cloud**.

1. Notez les informations disponibles sur la page vue d’ensemble de Microsoft Defender pour le cloud.  

1. Il est possible qu’une zone d’informations bleue s’affiche en haut de la page. Cela signifie que vous consultez des informations limitées.  Sélectionnez **Cliquer ici**.
    1. Attribuez-vous le rôle nécessaire pour assurer la visibilité au niveau du locataire.  Sélectionnez **Administrateur de sécurité**, puis **Obtenir l’accès** au bas de la page.
    1. Le message suivant s’affichera probablement : Le groupe d’administration racine n’existe pas.  Conformément à la description, le système créera le groupe pour vous.  L’exécution peut prendre jusqu’à 15 minutes (mais se produit généralement plus rapidement).  Une fois l’accès accordé, sélectionnez **Microsoft Defender pour le cloud** dans l’angle supérieur gauche de la page, au-dessus de l’indication Obtenir des autorisations, puis actualisez la page Vue d’ensemble de Microsoft Defender pour le cloud.

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

1. Sur la page principale, sélectionnez **Conformité réglementaire**. La page de conformité réglementaire fournit une liste de contrôles de conformité.  Sous chaque contrôle apparaît une liste d’évaluations fondées sur l’Azure Security Benchmark qui fournit des recommandations quant à la manière de sécuriser vos solutions cloud dans Azure.
    1. Cliquez sur **IM. Gestion d’identité** puis sélectionnez **IM-6 Utiliser des contrôles d’authentification forte**.  La liste indique les mesures concernant la responsabilité assumée par le client pouvant être prises pour améliorer la situation de conformité.
    1. Sélectionnez le **X** dans le coin supérieur droit pour fermer la page et revenir à la page de présentation de Microsoft Defender pour le cloud. 
    1. Laissez la page vue d’ensemble de Microsoft Defender pour le cloud ouverte ; vous allez utiliser dans la tâche suivante.


#### <a name="task-2-in-this-task-you-will-navigate-to-azure-secure-score-and-explore-recommendations-that-can-improve-your-secure-score"></a>Tâche 2 : Dans cette tâche, vous accéderez au Niveau de sécurité Azure et découvrirez les recommandations permettant d’améliorer votre niveau de sécurité. 

1. Dans la page vue d’ensemble de Microsoft Defender pour le cloud, sélectionnez la carte **Degré de sécurisation**.
1. Sélectionnez **Pass Azure - Parrainage**.  Notez votre niveau de sécurité.
1. Dans la page Recommandations, sélectionnez **Implémenter les bonnes pratiques de sécurité** pour développer la liste. Remarquez que l’état d’intégrité de ses ressources est rouge.
1. Sélectionnez l’élément **Plusieurs propriétaires doivent être affectés à votre abonnement**, dont l’état d’intégrité des ressources est rouge. 
1. En dessous de **Ressources affectées**, vérifiez que Ressources non saines est sélectionné/souligné, puis sélectionnez l’abonnement Azure listé.
1. En haut de la page Contrôle d’accès (IAM), sélectionnez **+ Ajouter**. Ensuite, dans la liste déroulante, sélectionnez **Ajouter une attribution de rôle**.
    1. Sur le côté gauche de la page, sélectionnez **Propriétaire** (il doit s’agir du premier élément répertorié) afin que la ligne soit mise en surbrillance en gris, puis sélectionnez **Suivant** en bas de la page.
    1. En regard de Membres, sélectionnez **+ Sélectionner des membres**. 
    1. Dans la fenêtre Sélectionner les membres qui s’ouvre sur le côté droit de l’écran, sélectionnez **Alex Wilber**, puis appuyez sur **Sélectionner** en bas de la page.  
    1. Dans la page Ajouter une attribution de rôle, vérifiez qu’Alex Wilber est listé en tant que membre, puis sélectionnez **Suivant** et **Vérifier + attribuer**.
    1. La mise à jour du statut peut prendre jusqu’à 24 heures. Ensuite, votre niveau de sécurité sera également mis à jour dans la mesure où tous les éléments du groupe Gérer les accès et les autorisations sont respectés.
    1. Dans l’angle supérieur gauche de la page, au-dessus de Pass Azure, sélectionnez **Microsoft Defender pour le cloud** pour retourner à la page de vue d’ensemble de Microsoft Defender pour le cloud.
1. Gardez cette page ouverte pour la prochaine tâche.


#### <a name="task-3--recall-that-microsoft-defender-for-cloud-is-offered-in-two-modes-without-enhanced-security-features-free-and-with-enhanced-security-features-which-are-available-through-the-microsoft-defender-for-cloud-plans-in-this-task-you-discover-how-to-enabledisable-the-various-microsoft-defender-for-cloud-plans"></a>Tâche 3 :  Rappelons que Microsoft Defender pour le cloud est proposé en deux modes : sans fonctions de sécurité améliorées (gratuit) et avec des fonctions de sécurité améliorées qui sont disponibles dans les plans Microsoft Defender pour le cloud. Dans cette tâche, vous découvrez comment activer ou désactiver les différents plans Microsoft Defender pour le cloud.

1.  Dans la page de vue d’ensemble de Microsoft Defender pour le cloud, sélectionnez **Paramètres d’environnement** dans le volet de navigation gauche.
1. Sélectionnez le signe supérieur **>** en regard de Groupe racine du locataire pour le développer (ne sélectionnez pas directement le groupe racine du locataire, car cela vous dirigera vers une autre page), puis **Pass Azure - Parrainage**
1.  Sur la page Plans Defender, notez comment vous pouvez sélectionner Activer tout ou sélectionner des plans Defender individuels. Laissez les paramètres tels quels avec tous les plans désactivés.
1.  Vous pouvez maintenant fermer l’onglet du navigateur pour quitter le portail Azure.


#### <a name="review"></a>Révision
Dans ce labo, vous avez découvert Microsoft Defender pour le cloud et appris à utiliser le Niveau de sécurité Azure pour améliorer la posture de sécurité de votre organisation.

