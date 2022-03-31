---
Demo:
  title: Azure Policy
  module: 'Module 4 Lesson 5: Describe the capabilities of Microsoft compliance solutions: Describe Azure Policy'
ms.openlocfilehash: 898e2d2ae228baf6acbffd7301fcbdf4a6a2dba5
ms.sourcegitcommit: a341c2fc38e9b37dafb792d82e3c948f7ba4a099
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/14/2022
ms.locfileid: "137894069"
---
# <a name="demo-azure-policy"></a>Démonstration : Azure Policy

### <a name="demo-scenario"></a>Scénario de la démonstration
Cette démonstration vous accompagnera tout au long du processus de définition d’une stratégie Azure et vous permettra de réaliser l’impact de cette stratégie.

#### <a name="demo-part-1-create-a-policy-to-require-a-tag-on-a-resource-group-shows-steps-to-create-a-policy-from-a-template"></a>Partie 1 de la démonstration : Créez une stratégie afin d’exiger une balise sur un groupe de ressources (indique les étapes de création d’une stratégie à partir d’un modèle).

1. Ouvrez Microsoft Edge. Saisissez **portal.microsoft.com** dans la barre d’adresse.  Vous devriez déjà être connecté ; si ce n’est pas le cas, connectez-vous à l’aide de vos informations d’identification d’administrateur.

1. Dans la zone de recherche (la barre bleue en haut de la page près de l’intitulé « Microsoft Azure »), saisissez **stratégie**, puis sélectionnez **Stratégie** dans les résultats de recherche.

1. Vous avez désormais sous les yeux la présentation de la page Stratégie. Prenez note des informations disponibles sur le tableau de bord.

1. Dans le volet de navigation gauche, sous Création, sélectionnez **Affectations**.  Vous remarquerez qu’il existe déjà une affectation de stratégie. Cliquez sur **ASC par défaut**.  Vérifiez le champ Description. REMARQUE : Le champ de description fait référence à Azure Security Center, qui a été rebaptisé Microsoft Defender pour le cloud.  Revenez à la page des affectations de stratégies en cliquant sur le **X** en haut à droite de la page.

1. Sélectionnez **Affecter une stratégie** en haut de la page.

1. L’assistant d’affectation de stratégie s’ouvre pour guider l’administrateur dans le processus d’affectation d’une stratégie.  Sélectionnez les **points de suspension** près du champ Définition de la stratégie.  Une liste des définitions de stratégie disponibles apparaît.  

1. Saisissez **Balise** dans la barre de recherche.

1. Sélectionnez **Exige une balise sur les groupes de ressources** dans les résultats de recherche (vous devrez peut-être faire défiler la liste), puis cliquez sur **Sélectionner**.  Remarque : cette stratégie a pour effet de refuser la création de nouveaux groupes de ressources qui ne répondent pas aux exigences.  

1. Prenez note du nom d’affectation par défaut.  Conservez le même nom et cliquez sur **Suivant** en bas de la page.

1. Dans le champ Nom de la balise, saisissez **Environnement** (les groupes de ressources exigeront une balise Environnement), puis cliquez sur **Suivant**.  

1. Dans l’onglet Correction, lisez la description, mais ne modifiez pas les paramètres. Sélectionnez **Suivant**.

1. Un message de non-conformité s’affiche : saisissez **Une balise d’environnement est nécessaire**, puis cliquez sur **Suivant**. Remarque : ce message apparaîtra comme motif de non-conformité pour les groupes de ressources sans balise Environnement créés avant l’affectation de la stratégie.  Après la mise en place de cette stratégie, la création de groupes de ressources sans balise d’environnement sera refusée.

1. Examinez l’affectation de stratégie, puis cliquez sur Créer.  Si la stratégie n’apparaît pas immédiatement, sélectionnez **Actualiser**. Remarque : l’entrée en application de la stratégie peut prendre jusqu’à 30 minutes.

1. Quittez la page des affectations de stratégies en cliquant sur le **X** en haut à droite de l’écran.

1. Vous vous trouvez désormais sur la page d’accueil des services Azure.  Ne fermez pas cette page, car vous en aurez besoin lors de la prochaine activité.

#### <a name="demo-part-2--show-the-impact-of-the-policy-by-creating-a-resource-group-without-a-tag-then-fix-it-to-have-a-tag"></a>Partie 2 de la démonstration :  Montrez l’impact de la stratégie en créant un groupe de ressources sans balise, puis ajoutez-lui-en une.

1. Sélectionnez **Groupes de ressources** en haut de la page, sous l’intitulé « Services Azure ». Si l’option n’apparaît pas dans la liste, saisissez Groupe de ressources dans la barre de recherche et sélectionnez-la depuis cette zone.

1. Sélectionnez **+ Créer** en haut à gauche de la page.

1. Dans l’onglet De base de l’option Créer un groupe de ressources, l’onglet Abonnement indique Pass Azure - Parrainage : ne le modifiez pas.

1. Saisissez **SC900-Labos** dans le champ Groupe de ressources.

1. Laissez le paramètre Région défini par défaut, puis sélectionnez **Suivant : Étiquettes**.

1. Ne remplissez pas les champs Nom ni Valeur de la balise.  LAISSEZ-LES VIDES, puis cliquez sur **Vérifier + créer**.

1. Un message indiquant que la requête est validée s’affiche (le nom et la valeur de la balise ne sont pas exigés dans l’assistant) : cliquez ensuite sur **Créer**.

1. Un message d’échec s’affichera en haut de l’écran : « Échec de la création du groupe de ressources. Afficher les détails de l’erreur ».  Cliquez sur **Afficher les détails de l’erreur**. La condition faisant partie de la stratégie Azure n’a pas été remplie ; par conséquent, la création du groupe de ressources a été bloquée pour cause de non-conformité. Remarque : Si le message d’échec n’apparaît pas et que le groupe de ressources a été créé, la stratégie n’est pas encore entrée en application.  Accédez à la page Stratégie de la stratégie que vous avez créée au cours de l’activité précédente : une fois la stratégie entrée en application, vous verrez que la ressource n’est pas conforme.  La page des détails inclura le message de non-conformité.

1. Le récapitulatif de l’erreur affiche le type d’erreur « La ressource « SC900-Labos » a été interdite par la stratégie. »  Fermez cette fenêtre en cliquant sur le **X** en haut à gauche de l’écran.

1. Dans la fenêtre Créer un groupe de ressources, cliquez sur **<Précédent**.

1. Vous êtes revenu à la page des Balises pour la création d’un groupe de ressources.  Dans le champ Nom, saisissez Environnement. Dans le champ Valeur, saisissez **SC900-Labos**, puis cliquez sur **Suivant : Vérifier + créer >** .

1. Vérifiez la balise et sélectionnez **Créer**.

1. Le groupe de ressources apparaît dans la liste.  La balise a été indiquée dans le groupe de ressources : par conséquent, la condition incluse dans la stratégie Azure a été remplie.  Le groupe de ressources est conforme à la stratégie.

#### <a name="review"></a>Révision

Dans cette démonstration, vous avez montré le processus de définition d’une stratégie Azure ainsi que l’impact de cette stratégie.
