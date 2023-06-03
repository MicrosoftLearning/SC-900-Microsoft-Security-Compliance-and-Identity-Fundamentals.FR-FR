<a name="---"></a><!---
---
Démonstration : Titre : « Azure Policy » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft ; Module 6 : Décrire les fonctionnalités de gouvernance des ressources dans Azure ; Unité 2 : Décrire Azure Policy »
---
--->

# <a name="demo-azure-policy"></a>Démonstration : Azure Policy

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft
- Module : Décrire les fonctionnalités de gouvernance des ressources dans Azure
- Unité : Décrire Azure Policy

## <a name="demo-scenario"></a>Scénario de la démonstration

Dans cette démo, vous présentez le processus de configuration d’une stratégie Azure et l’impact de cette stratégie.

### <a name="demo-part-1"></a>Partie 1 de la démonstration

Créez une stratégie afin d’exiger une balise sur un groupe de ressources (indique les étapes de création d’une stratégie à partir d’un modèle).

1. Ouvrez Microsoft Edge. Dans la barre d’adresses, entrez **portal.azure.com**.  Vous devez déjà être connecté. Si ce n’est pas le cas, connectez-vous avec vos informations d’identification d’administrateur.

1. Dans la zone de recherche (la barre bleue en haut de la page près de l’intitulé « Microsoft Azure »), saisissez **stratégie**, puis sélectionnez **Stratégie** dans les résultats de recherche.

1. Vous êtes maintenant dans la vue d’ensemble de la page Stratégie. Prenez note des informations disponibles sur le tableau de bord.

1. Dans le volet de navigation gauche, sous Création, sélectionnez **Attributions**.  Notez qu’il y a déjà une attribution de stratégie. Sélectionnez **Valeur par défaut ASC**.  Vérifiez le champ Description. REMARQUE : Le champ de description référence Azure Security Center, qui a été rebaptisé Microsoft Defender pour le cloud.  Revenez à la page des affectations de stratégies en cliquant sur le **X** en haut à droite de la page.

1. Sélectionnez **Affecter une stratégie** en haut de la page. L’assistant d’affectation de stratégie s’ouvre pour guider l’administrateur dans le processus d’affectation d’une stratégie.

1. Vous commencez dans l’onglet Informations de base.
    1. Pour l’étendue, gardez le paramètre par défaut. Dans cet exemple, l’étendue de la stratégie est l’abonnement Azure fourni par l’hébergeur de labo autorisé (ALH).
    1. Pour la définition de stratégie, sélectionnez les **points de suspension**.  Une liste des définitions de stratégie disponibles apparaît.  Dans la barre de recherche, entrez **Demander une étiquette**. Sélectionnez **Exige une balise sur les groupes de ressources** dans les résultats de recherche (vous devrez peut-être faire défiler la liste), puis cliquez sur **Sélectionner**.  Remarque : cette stratégie a pour effet de refuser la création de nouveaux groupes de ressources qui ne répondent pas aux exigences.  
    1. Prenez note du nom d’affectation par défaut.  Gardez le nom tel quel.
    1. Vérifiez que l’option Application de la stratégie est définie sur **Activé** et sélectionnez **Suivant**.

1. Vous êtes maintenant sous l’onglet Paramètres. Dans le champ Nom de l’étiquette, entrez **Environnement**, puis sélectionnez **Suivant**.

1. Sous l’onglet Correction, gardez les paramètres par défaut, puis sélectionnez **Suivant**.

1. Vous êtes maintenant sous l’onglet Messages de non-conformité. Dans le champ du message de non-conformité, entrez **Une étiquette Environnement est nécessaire**, puis sélectionnez **Suivant**. Remarque : ce message apparaîtra comme motif de non-conformité pour les groupes de ressources sans balise Environnement créés avant l’affectation de la stratégie.  

1. Passez en revue l’attribution de stratégie, puis sélectionnez **Créer**.  Si la stratégie n’apparaît pas immédiatement, sélectionnez **Actualiser**. Remarque : Vous devez parfois attendre jusqu’à 30 minutes avant que la stratégie soit appliquée, mais elle l’est généralement beaucoup plus rapidement.

1. Quittez la page des affectations de stratégies en cliquant sur le **X** en haut à droite de l’écran.

1. Vous êtes maintenant dans la page d’accueil des services Azure.  Ne fermez pas cette page, car vous en avez besoin dans la prochaine tâche.

### <a name="demo-part-2"></a>Partie 2 de la démonstration

Dans cette tâche, vous voyez l’impact de l’attribution de stratégie Azure quand vous tentez de créer un groupe de ressources dans Azure qui n’a pas d’étiquette.

1. Ouvrez l’onglet Accueil - Microsoft Azure.

1. En haut de la page, sous Services Azure, sélectionnez **Groupes de ressources**.

1. Sélectionnez **+ Créer** en haut à gauche de la page.

1. Sous l’onglet Informations de base de l’option Créer un groupe de ressources, laissez le champ Abonnement tel quel.

1. Saisissez **SC900-Labos** dans le champ Groupe de ressources.

1. Laissez le paramètre Région défini par défaut, puis sélectionnez **Suivant : Étiquettes**.

1. Ne remplissez pas les champs Nom ni Valeur de la balise.  LAISSEZ-LES VIDES, puis cliquez sur **Vérifier + créer**.

1. Vous voyez un message indiquant la réussite de la validation (le nom et la valeur de l’étiquette ne sont pas demandés dans l’Assistant), puis sélectionnez **Créer**.

1. Vous voyez un message d’échec en haut de l’écran : « La création du groupe de ressources a échoué ». Sélectionnez **Voir les détails de l’erreur**. La condition de la stratégie Azure n’a pas été remplie et la création du groupe de ressources a été bloquée parce qu’elle n’est pas conforme. Remarque : Si le message d’échec n’apparaît pas et que le groupe de ressources a été créé, la stratégie n’est pas encore entrée en application.  Accédez à la page Stratégie de la stratégie que vous avez créée dans la tâche précédente. Une fois la stratégie appliquée, vous voyez que la ressource n’est pas conforme.  La page des détails inclura le message de non-conformité.

1. Le récapitulatif de l’erreur affiche le type d’erreur « La ressource « SC900-Labos » a été interdite par la stratégie. »  Fermez cette fenêtre en cliquant sur le **X** en haut à gauche de l’écran.

1. Dans la fenêtre Créer un groupe de ressources, sélectionnez **Précédent**.

1. Vous êtes revenu à la page Étiquettes de Créer un groupe de ressources.  Dans le champ Nom, saisissez Environnement. Dans le champ Valeur, saisissez **SC900-Labos**, puis cliquez sur **Suivant : Vérifier + créer >** .

1. Vérifiez la balise et sélectionnez **Créer**.

1. Dans le champ Nom, entrez **Environnement** et dans le champ Valeur, entrez **Labos** (cette valeur n’a pas d’importance, la stratégie nécessite simplement une valeur d’étiquette), puis sélectionnez **Suivant : Vérifier + créer >** et **Créer**.

1. Vous voyez le groupe de ressources dans la liste.  

1. Indiquez aux élèves que s’il y avait eu un groupe de ressources créé avant la stratégie, ce groupe de ressources s’afficherait comme non conforme par rapport à cette attribution de stratégie et qu’il devrait être corrigé, en appliquant l’étiquette Environnement.  Il y a un groupe de ressources préexistant étiqueté ResourceGroup1 qui n’est pas conforme et peut être corrigé, mais la durée de mise à jour de l’état après la correction est plus longue que d’habitude pour l’environnement lab.

### <a name="review"></a>Révision

Dans cette démonstration, vous avez montré le processus de définition d’une stratégie Azure ainsi que l’impact de cette stratégie.
