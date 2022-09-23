---
ms.openlocfilehash: eeee584ece9bb3ec4edcba5fa2e76a13dd9459c4
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892603"
---
<a name="---"></a><!---
---
Labo : Titre : « Explorer Microsoft Defender pour le cloud » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft ; Module 2 : Décrire les fonctionnalités de gestion de la sécurité d’Azure ; Unité 3 : Décrire Microsoft Defender pour le cloud »
---
--->

# <a name="lab-explore-microsoft-defender-for-cloud"></a>Labo : Explorer Microsoft Defender pour le cloud

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de sécurité Microsoft
- Module : Décrire les fonctionnalités de gestion de la sécurité d’Azure
- Unité : Décrire Microsoft Defender pour le cloud

## <a name="lab-scenario"></a>Scénario du labo

Dans ce labo, vous allez découvrir Microsoft Defender pour le cloud et apprendre à utiliser le Niveau de sécurité Azure pour améliorer la posture de sécurité de votre organisation.  REMARQUE : Cette démonstration pas à pas suppose que le présentateur dispose d’autorisations de niveau administrateur pour l’abonnement Azure via un Pass Azure.  Un abonnement Azure, comme un abonnement Cloudslice, géré par l’hôte de labo autorisé limite l’accès et les fonctionnalités : certaines étapes ci-dessous peuvent être indisponibles ou ne pas montrer d’informations.

**Durée estimée** : 30 minutes

### <a name="setup"></a>Programme d’installation

Dans cette tâche, vous allez effectuer une configuration de base de Microsoft Defender pour le cloud pour préparer l’abonnement, et activer et affecter une stratégie par défaut.

1. Ouvrez Microsoft Edge. Dans la barre d’adresse, saisissez **portal.azure.com**.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Saisissez le mot de passe d’administrateur communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Dans le coin supérieur gauche de l’écran, en regard de l’endroit où Microsoft Azure est indiqué, sélectionnez l’icône de menu Afficher le portail (les trois lignes horizontales également appelées « icône hamburger ») puis, dans le volet de navigation gauche, sous Favoris, sélectionnez **Microsoft Defender pour le cloud**.  S’il n’est pas répertorié sous Favoris, dans la zone de recherche, entrez **Microsoft Defender pour le cloud**, puis dans la liste des résultats, sélectionnez **Microsoft Defender pour le cloud**.

1. Si vous accédez à Microsoft Defender pour le cloud pour la première fois avec votre abonnement, il est possible que la page Bien démarrer s’affiche et qu’une mise à niveau vous soit proposée.  Faites défiler vers le bas de la page, puis sélectionnez **ignorer**.  Vous serez dirigé vers la page Vue d’ensemble.
    1. En haut de la page, vous verrez une zone d’informations bleu clair qui indique « Nous préparons vos abonnements. L’opération peut prendre quelques instants... »
    1. Une fois l’abonnement prêt, une nouvelle zone d’informations peut apparaître, indiquant « Un abonnement n’a pas de stratégie par défaut affectée. Pour passer en revue la liste des abonnements, ouvrez la page Stratégie de sécurité. »  Sélectionnez la flèche droite à la fin de la phrase ou sélectionnez **Paramètres de l’environnement** dans le volet de navigation gauche.
        1. Vous vous trouvez maintenant dans la page Paramètres de l’environnement. Sélectionnez **Pass Azure - Parrainage**.  Remarque :  Si votre environnement Azure est basé sur un abonnement Azure géré par l’hôte de labo autorisé, au lieu d’un Pass Azure, vous le verrez référencé. Développez l’option en sélectionnant le signe « supérieur à » jusqu’à ne plus pouvoir développer les options : vous voyez alors l’abonnement.
        1. Dans le volet de navigation gauche, sélectionnez **Stratégie de sécurité**.
        1. Dans la page principale, sous Initiative par défaut, sélectionnez **Affecter une stratégie**.
        1. En bas de la page, sélectionnez **Vérifier + Créer**.
        1. En bas de la page, sélectionnez **Créer**.  Ceci affecte Azure Security Benchmark en tant qu’initiative de stratégie par défaut.  Actualisez l’écran (l’opération peut prendre quelques minutes).
        1. Quittez la page Paramètres de l’environnement en sélectionnant le **X** sur la page.  
        1. Dans la page Services Azure, sélectionnez **Microsoft Defender pour le cloud** pour revenir à la page Vue d’ensemble.

### <a name="task-1"></a>Tâche 1

Dans cette tâche, vous allez effectuer une présentation très générale de certaines des fonctionnalités de Microsoft Defender pour le cloud.

1. Dans la page Vue d’ensemble de Microsoft Defender pour le cloud, remarquez les informations qui y sont disponibles.  Les informations en haut de la page incluent le nombre d’abonnements Azure, le nombre de ressources évaluées, le nombre de recommandations actives et les éventuelles alertes de sécurité.  Sur le corps de la page s’affichent des cartes qui représentent le niveau de sécurité, la conformité réglementaire, Insights, etc.

1. Sélectionnez **Ressources évaluées** en haut de la page.  (Remarque : cela équivaut à avoir sélectionné Inventaire dans le volet de navigation gauche de la page d’accueil de Microsoft Defender pour le cloud.)
    1. Cela vous amène à la page **Inventaire** qui affiche votre abonnement de pass Azure.  Sélectionnez **Pass Azure - Parrainage**.
    1. La page Resource Health vous fournit une liste de recommandations.  Dans cette liste, sélectionnez **Plusieurs propriétaires doivent être attribués à votre abonnement**.
    1. Cliquez sur la flèche de déroulement près des étapes de correction. Prenez note de la présence d’étapes de correction détaillées ainsi que de la possibilité de prendre des mesures.  
    1. Sélectionnez **Microsoft Defender pour le cloud** dans l’angle supérieur gauche de l’écran pour revenir à la page de présentation de Microsoft Defender pour le cloud.

1. Sélectionnez **Recommandations actives** en haut de la page.  (Remarque : cela équivaut à avoir sélectionné Recommandations dans le volet de navigation gauche de la page d’accueil de Microsoft Defender pour le cloud.)
    1. La page des recommandations affiche votre tableau de bord de niveau de sécurité.
    1. Sous ce tableau de bord, vous trouvez une liste de contrôles. Chaque contrôle de sécurité représente un risque de sécurité devant être atténué et inclut également des informations sur le niveau maximal associé à ce contrôle, le niveau actuel, l’augmentation potentielle du niveau et l’état d’intégrité de la ressource.  
    1. Sélectionnez un des contrôles, comme **Implémenter les bonnes pratiques de sécurité**.  Sélectionnez un des sous-éléments, comme **Plusieurs propriétaires doivent être attribués à votre abonnement**.  Une page s’ouvre : elle contient une description, les étapes de correction et les ressources concernées. Quittez cette page en cliquant sur le **X** en haut à droite de l’écran.
    1. Quittez la page des recommandations en cliquant sur le **X** en haut à droite de l’écran. Cela vous ramènera à la page de présentation.

1. Sur la page principale, sélectionnez **Conformité réglementaire**. La page de conformité réglementaire fournit une liste de contrôles de conformité.  Sous chaque contrôle apparaît une liste d’évaluations fondées sur l’Azure Security Benchmark qui fournit des recommandations quant à la manière de sécuriser vos solutions cloud dans Azure.
    1. Cliquez sur **IM. Gestion d’identité** puis sélectionnez **IM-6 Utiliser des contrôles d’authentification forte**.  La liste indique les mesures concernant la responsabilité assumée par le client pouvant être prises pour améliorer la situation de conformité.
    1. Sélectionnez le **X** dans le coin supérieur droit pour fermer la page et revenir à la page de présentation de Microsoft Defender pour le cloud.
    1. Laissez la page vue d’ensemble de Microsoft Defender pour le cloud ouverte ; vous allez utiliser dans la tâche suivante.

### <a name="task-2"></a>Tâche 2

Rappelons que Microsoft Defender pour le cloud est proposé en deux modes : sans fonctions de sécurité améliorées (gratuit) et avec des fonctions de sécurité améliorées qui sont disponibles dans les plans Microsoft Defender pour le cloud. Dans cette tâche, vous découvrez comment activer ou désactiver les différents plans Microsoft Defender pour le cloud.

1. Dans la page de vue d’ensemble de Microsoft Defender pour le cloud, sélectionnez **Paramètres d’environnement** dans le volet de navigation gauche.
1. Sélectionnez le signe supérieur **>** en regard de Groupe racine du locataire pour le développer (ne sélectionnez pas directement le groupe racine du locataire, car cela vous dirigera vers une autre page), puis **Pass Azure - Parrainage**
1. Sur la page Plans Defender, notez comment vous pouvez sélectionner Activer tout ou sélectionner des plans Defender individuels. Laissez les paramètres tels quels avec tous les plans désactivés.
1. Fermez tous les onglets ouverts du navigateur.

### <a name="review"></a>Révision

Dans ce labo, vous avez découvert Microsoft Defender pour le cloud et appris à utiliser le Niveau de sécurité Azure pour améliorer la posture de sécurité de votre organisation.
