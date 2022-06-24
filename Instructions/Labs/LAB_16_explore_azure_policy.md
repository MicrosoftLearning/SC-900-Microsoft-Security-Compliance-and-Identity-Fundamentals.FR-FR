---
lab:
  title: Explorer Azure Policy.
  module: 'Module 4 Lesson 6: Describe the capabilities of Microsoft compliance solutions: Describe Azure Policy'
ms.openlocfilehash: 0a2ead44f5dc74a7684b8d78ea34c85767f8af92
ms.sourcegitcommit: 57e11f5a455d10c8ae3c95bb8a9487b10af3d315
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2022
ms.locfileid: "146542589"
---
# <a name="lab-explore-azure-policy"></a>Labo : Explorer Azure Policy.

## <a name="lab-scenario"></a>Scénario du labo

Azure Policy aide à appliquer des normes organisationnelles et à évaluer la conformité à grande échelle. Azure Policy évalue les ressources dans Azure en comparant les propriétés de ces ressources aux règles d’entreprise. Dans ce labo, vous allez commencer par découvrir la page d’arrivée d’Azure Policy. Ensuite, vous allez créer une stratégie et en étudier les effets.

**Durée estimée** : 20-25 minutes

### <a name="task-1"></a>Tâche 1

Découvrez l’essentiel de la page Azure Policy.

1. Ouvrez Microsoft Edge. Dans la barre d’adresse, saisissez **portal.azure.com**.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.

    1. Saisissez le mot de passe d’administrateur communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Vous vous trouvez maintenant dans le Portail Azure.  Dans la zone de recherche (la barre bleue en haut de la page près de l’intitulé « Microsoft Azure »), saisissez **stratégie**, puis sélectionnez **Stratégie** dans les résultats de recherche. La page d’accueil correspondante s’ouvre et vous donne accès à un tableau de bord.  L’étendue des informations que vous voyez correspond au pass Azure que vous utilisez dans le cadre de ce labo.   Prenez note des informations disponibles sur le tableau de bord.

1. Il y a un élément, appelé ASC par défaut (ASC fait référence à Azure Security Center, qui est maintenant appelé Microsoft Defender pour le cloud) dont l’étendue est Pass Azure - Parrainage.   Sélectionnez **ASC Default**.

1. En haut de la page, sous Éléments principaux, vous en trouverez le nom et la description, ainsi que d’autres informations importantes.  Lisez la description (positionnez le curseur de votre souris dessus). REMARQUE : Le champ de description fait référence à Azure Security Center, qui a été rebaptisé Microsoft Defender pour le cloud.

1. Vous constaterez que les informations fournies par le tableau de bord restent à jour afin de refléter l’élément sélectionné, à savoir ASC Default. Cet élément ASC Default est la définition de l’initiative Benchmark de sécurité Azure.  Rappel : une définition d’initiative est une collection de définitions de stratégie qui sont spécialement conçues pour atteindre un objectif global particulier. Vous pouvez afficher les informations par groupe, par stratégie, par ressource non conforme ou par événement.

1. Quittez la page ASC et revenez à la page d’accueil de la stratégie en sélectionnant le **X** dans le coin supérieur droit de la fenêtre.

1. Dans le volet de navigation situé à gauche, sélectionnez **Prise en main**.  Différentes options sont disponibles, qui permettent notamment de parcourir les stratégies intégrées et de les attribuer à grande échelle. Vous pouvez fournir à votre environnement des définitions de stratégies personnalisées, recommander l’affectation de stratégies, etc.

1. Dans le volet de navigation situé à gauche, sélectionnez **Conformité**.  Comme sur la page d’aperçu, vous trouverez l’état de conformité des stratégies mentionnées et/ou des initiatives.  Sur la page de Conformité à la stratégie, vous pouvez également attribuer une stratégie ou une initiative (cet exercice vous sera proposé lors de la prochaine tâche).

1. Dans le volet de navigation situé à gauche, sélectionnez **Correction**.  Cette page liste les stratégies qui comportent des ressources non conformes.  Si vous en sélectionnez une, vous pouvez déclencher la création d’une tâche corrective.  

1. Dans le volet de navigation situé à gauche, sous l’édition, sélectionnez **Devoirs**,  qui reprend la stratégie et/ou les devoirs d’initiative en cours. Vous pouvez aussi en créer de nouveaux.  Nous reviendrons à cette opération lors de la tâche suivante.  

1. Dans le volet de navigation situé à gauche, sélectionnez **Définitions**,  puis **Machines d’audit au mot de passe non sécurisé**.  Cette définition d’initiative comporte de nombreuses stratégies.  Pour vous familiariser avec les définitions de stratégies, sélectionnez **Audit des machines Windows qui n’ont pas l’antériorité maximale du mot de passe définie sur 70 jours**.  À l’ouverture de la page, la définition de la stratégie apparaît avec une structure JSON (Java Script Object Notation).   Le texte en rouge vous montre les parties de la définition qui caractérisent le nom d’affichage, la description, les paramètres, les règles de la stratégie, etc. NE TOUCHEZ À RIEN.  

1. Quittez la page Définition de la stratégie grâce au **X** dans le coin supérieur droit.

1. Quittez la page Définition d’initiative grâce au **X** dans le coin supérieur droit.

1. Conservez cet onglet (Stratégie - Microsoft Azure) en vue de la prochaine tâche.

### <a name="task-2"></a>Tâche 2

Dans cette tâche, vous allez créer une simple affectation de stratégie consistant à demander un indicateur sur les groupes de ressources.

1. Ouvrez l’onglet Stratégie - Microsoft Azure.

1. Dans le volet de navigation gauche, sous Création, sélectionnez **Affectations**.

1. Sélectionnez **Affecter une stratégie** en haut de la page.

1. L’assistant d’affectation de stratégie s’ouvre pour guider l’administrateur dans le processus d’affectation d’une stratégie.  Sélectionnez les **points de suspension** près du champ Définition de la stratégie.  Une liste des définitions de stratégie disponibles apparaît.  

1. Saisissez **Balise** dans la barre de recherche.

1. Sélectionnez **Exige une balise sur les groupes de ressources** dans les résultats de recherche (vous devrez peut-être faire défiler la liste), puis cliquez sur **Sélectionner**.  Remarque : cette stratégie a pour effet de refuser la création de nouveaux groupes de ressources qui ne répondent pas aux exigences.  

1. Prenez note du nom d’affectation par défaut.  Conservez le même nom et cliquez sur **Suivant** en bas de la page.

1. Dans le champ Nom de l’indicateur, saisissez **Environnement** avant d’utiliser le bouton **Suivant**.

1. Conservez les paramètres de correction par défaut, puis sélectionnez **Suivant**.

1. Un message de non-conformité s’affiche : saisissez **Une balise d’environnement est nécessaire**, puis cliquez sur **Suivant**. Remarque : ce message apparaîtra comme motif de non-conformité pour les groupes de ressources sans balise Environnement créés avant l’affectation de la stratégie.  Après la mise en place de cette stratégie, la création de groupes de ressources sans balise d’environnement sera refusée.

1. Examinez l’affectation de stratégie, puis cliquez sur Créer.  Si la stratégie n’apparaît pas immédiatement, sélectionnez **Actualiser**. Remarque : l’entrée en application de la stratégie peut prendre jusqu’à 30 minutes.

1. Quittez la page des affectations de stratégies en cliquant sur le **X** en haut à droite de l’écran.

1. Vous vous trouvez désormais sur la page d’accueil des services Azure.  Ne fermez pas cette page, car vous en aurez besoin lors de la prochaine activité.

### <a name="task-3"></a>Tâche 3

Dans cette tâche, vous allez constater les effets de l’affectation de la stratégie Azure en créant un groupe de ressources dans Azure, sans indicateur. Vous allez ensuite pouvoir mettre à jour ce groupe afin d’y inclure un indicateur.  Remarque : il faut parfois attendre jusqu’à 30 minutes avant que la stratégie créée lors de la tâche précédente prenne effet, bien que cela reste rare.

1. Ouvrez l’onglet Accueil - Microsoft Azure.

1. En haut de la page, sous Services Azure, sélectionnez **Groupes de ressources**.

1. Sélectionnez **+ Créer** en haut à gauche de la page.

1. Dans l’onglet De base de l’option Créer un groupe de ressources, l’onglet Abonnement indique Pass Azure - Parrainage : ne le modifiez pas.

1. Saisissez **SC900-Labos** dans le champ Groupe de ressources.

1. Laissez le paramètre Région défini par défaut, puis sélectionnez **Suivant : Étiquettes**.

1. Ne remplissez pas les champs Nom ni Valeur de la balise.  LAISSEZ-LES VIDES, puis cliquez sur **Vérifier + créer**.

1. Un message indiquant que la requête est validée s’affiche (le nom et la valeur de la balise ne sont pas exigés dans l’assistant) : cliquez ensuite sur **Créer**.

1. Un message d’échec s’affichera en haut de l’écran : « Échec de la création du groupe de ressources. Afficher les détails de l’erreur ».  Cliquez sur **Afficher les détails de l’erreur**. La condition faisant partie de la stratégie Azure n’a pas été remplie ; par conséquent, la création du groupe de ressources a été bloquée pour cause de non-conformité.

    Remarque : Si le message d’échec n’apparaît pas et que le groupe de ressources a été créé, la stratégie n’est pas encore entrée en application.  Accédez à la page Stratégie de la stratégie que vous avez créée au cours de l’activité précédente : une fois la stratégie entrée en application, vous verrez que la ressource n’est pas conforme.  La page des détails inclura le message de non-conformité. Si vous obtenez l’erreur, les étapes suivantes montrent comment corriger le déploiement.

1. Le récapitulatif de l’erreur affiche le type d’erreur « La ressource « SC900-Labos » a été interdite par la stratégie. »  Fermez cette fenêtre en cliquant sur le **X** en haut à gauche de l’écran.

1. Dans la fenêtre Créer un groupe de ressources, sélectionnez **Précédent**.

1. Vous êtes revenu à la page des Balises pour la création d’un groupe de ressources.  Dans le champ Nom, saisissez Environnement. Dans le champ Valeur, saisissez **SC900-Labos**, puis cliquez sur **Suivant : Vérifier + créer >** .

1. Vérifiez la balise et sélectionnez **Créer**.

1. Le groupe de ressources apparaît dans la liste.  La balise a été indiquée dans le groupe de ressources : par conséquent, la condition incluse dans la stratégie Azure a été remplie.  Le groupe de ressources est conforme à la stratégie.

1. Avant de le quitter, supprimez la stratégie Azure.
    1. Dans le coin supérieur gauche, sélectionnez Accueil pour revenir à la page d’accueil d’Azure.

    1. En dessous des Services Azure, sélectionnez Stratégie Azure.
    1. Au milieu de la page se trouve une liste des affectations de stratégie ou d’initiative Azure.  À côté de celle consistant à demander un indicateur sur les groupes de ressources, les points de suspension vous permettent de sélectionner Supprimer l’affectation.
    1. Un message s’affiche pour vous demander de confirmer la suppression de l’affectation.  Sélectionnez Oui.

### <a name="review"></a>Révision

Dans ce labo, vous avez parcouru la page d’arrivée d’Azure Policy. Ensuite, vous avez suivi le processus de création d’une stratégie et en avez étudié les effets.
