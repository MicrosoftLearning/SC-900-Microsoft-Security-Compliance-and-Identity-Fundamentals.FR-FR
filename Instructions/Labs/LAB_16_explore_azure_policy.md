<!---
---
Labo : Titre : « Découvrir Azure Policy » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft ; Module 6 : Décrire les fonctionnalités de gouvernance des ressources dans Azure ; Unité 2 : Décrire Azure Policy »
---
--->

# Labo : Explorer Azure Policy

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft
- Module : Décrire les fonctionnalités de gouvernance des ressources dans Azure
- Unité : Décrire Azure Policy

## Scénario du labo

Azure Policy aide à appliquer les normes organisationnelles et à évaluer la conformité à l’échelle. Azure Policy évalue les ressources dans Azure en comparant les propriétés de ces ressources aux règles d’entreprise. Dans ce labo, vous créez une stratégie et voyez l’impact de cette stratégie.  Vous explorez également les informations de conformité et de correction disponibles dans la page de stratégie.

**Durée estimée** : 15 à 20 minutes

### Tâche 1

Dans cette tâche, vous créez une attribution de stratégie de base pour demander une étiquette sur un groupe de ressources.
1.  Ouvrez Microsoft Edge. Dans la barre d’adresse, entrez **portal.azure.com**.

1. Connectez-vous avec les informations d’identification d’administrateur de votre abonnement Azure (ces informations d’identification d’administrateur sont différentes des informations d’identification d’administrateur Microsoft 365).
    1. Dans la fenêtre de connexion, entrez **User1-XXXXXXXX@LODSPRODMSLEARNMCA.onmicrosoft.com** (où XXXXXXXX représente votre ID de locataire unique fourni par le fournisseur d’hébergement de votre labo), puis sélectionnez **Suivant**.

    1. Entrez le mot de passe d’administrateur communiqué par votre fournisseur d’hébergement de labo. Cliquez sur **Connexion**.
    1. Si vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Vous êtes maintenant dans le portail Azure.  Dans la barre de recherche, dans la barre bleue en haut de la page à côté de là où il est indiqué Microsoft Azure, saisissez **Stratégie** puis sélectionnez **Stratégie** dans les résultats de recherche. La page d’accueil Stratégie s’ouvre sur une vue de tableau de bord.  L’étendue de la vue Tableau de bord est l’abonnement Azure fourni par l’hébergeur de labo autorisé (ALH). Une stratégie est listée, il s’agit d’une stratégie créée par l’ALH pour utiliser l’abonnement Azure.

1. Dans le volet de navigation gauche, sous Création, sélectionnez **Affectations**.

1. En haut de la page, sélectionnez **Affecter une stratégie**. L’Assistant Attribuer une stratégie s’ouvre pour guider l’administrateur dans le processus d’attribution de stratégie.

1. Vous commencez dans l’onglet Informations de base.
    1. Pour l’étendue, gardez le paramètre par défaut. Dans cet exemple, l’étendue de la stratégie est l’abonnement Azure fourni par l’hébergeur de labo autorisé (ALH).
    1. Pour la définition de stratégie, sélectionnez les **points de suspension**.  Une liste des définitions de stratégies disponibles est fournie.  Dans la barre de recherche, entrez **Demander une étiquette**. Sélectionnez **Exiger une balise sur le groupe de ressources** dans les résultats de recherche (vous devrez peut-être faire défiler la liste), puis cliquez sur **Ajouter**.  Remarque : cette stratégie a pour effet de refuser la création de tout nouveau groupe de ressources qui ne répond pas à l’exigence.  
    1. Notez le nom d’affectation par défaut.  Gardez le nom tel quel.
    1. Assurez-vous que l’option Application de la stratégie est définie sur **Activée**

1. Sélectionnez **Suivant**, puis sélectionnez à nouveau **Suivant** pour passer à l’onglet Paramètres (vous pouvez également sélectionner l’onglet Paramètres directement).

1. Vous êtes maintenant sous l’onglet Paramètres. Dans le champ Nom de l’étiquette, entrez **Environnement**, puis sélectionnez **Suivant**.

1. Sous l’onglet Correction, gardez les paramètres par défaut, puis sélectionnez **Suivant**.

1. Vous êtes maintenant sous l’onglet Messages de non-conformité. Dans le champ du message de non-conformité, entrez **Une étiquette Environnement est nécessaire**, puis sélectionnez **Suivant**. Remarque : ce message apparaîtra comme motif de non-conformité pour les groupes de ressources qui ont été créés avant l’affectation de la stratégie et qui n’ont pas d’étiquette Environnement.

1. Passez en revue l’attribution de stratégie, puis sélectionnez **Créer**.  Si la stratégie ne s’affiche pas immédiatement, sélectionnez **Actualiser**. Remarque : Vous devez parfois attendre jusqu’à 30 minutes avant que la stratégie soit appliquée, mais elle l’est généralement beaucoup plus rapidement.

1. Quittez la page d’affectation des stratégies en sélectionnant le **X** dans le coin supérieur droit de l’écran.

1. Vous êtes maintenant dans la page d’accueil des services Azure.  Ne fermez pas cette page, car vous en avez besoin dans la prochaine tâche.

### Tâche 2

Dans cette tâche, vous voyez l’impact de l’attribution de stratégie Azure quand vous tentez de créer un groupe de ressources dans Azure qui n’a pas d’étiquette.

1. Ouvrez l’onglet du navigateur, Accueil - Microsoft Azure.

1. En haut de la page, sous Services Azure, sélectionnez **Groupes de ressources**.

1. Dans le coin supérieur gauche de la page, sélectionnez **+ Créer**.

1. Sous l’onglet Informations de base de l’option Créer un groupe de ressources, laissez le champ Abonnement tel quel.

1. Dans le champ Groupe de ressources, saisissez **SC900-Labs**.

1. Laissez le paramètre Région défini par défaut, puis sélectionnez **Suivant : Étiquettes**.

1. Laissez le champ Nom et valeur d’étiquette vide.  NE PAS REMPLIR, puis sélectionnez **Vérifier + créer**.

1. Vous voyez un message indiquant que la validation a réussi (le nom et la valeur de l’étiquette ne sont pas demandés dans l’Assistant), puis sélectionnez **Créer**.

1. Vous voyez un message d’échec en haut de l’écran : « La création du groupe de ressources a échoué ». Sélectionnez **Voir les détails de l’erreur**. La condition de la stratégie Azure n’a pas été remplie et la création du groupe de ressources a été bloquée parce qu’elle n’est pas conforme. Remarque : si vous ne voyez pas le message d’échec et que le groupe de ressources a été créé, c’est parce que la stratégie n’a pas encore pris effet.  Accédez à la page Stratégie de la stratégie que vous avez créée dans la tâche précédente. Une fois la stratégie appliquée, vous voyez que la ressource n’est pas conforme.  La page de détails contient le message de non-conformité.

1. Le résumé de l’erreur indique le type d’erreur « La ressource « SC900-Labs » n’a pas été autorisée par la stratégie. »  Fermez cette fenêtre en sélectionnant le **X** en haut à gauche de l’écran.

1. Dans la fenêtre Créer un groupe de ressources, sélectionnez **Précédent**.

1. Vous êtes revenu à la page Étiquettes de Créer un groupe de ressources.  Dans le champ Nom, saisissez Environnement. Dans le champ Valeur, saisissez **SC900-Labs**, puis sélectionnez **Suivant : Vérifier + créer >**.

1. Vérifiez les étiquettes et sélectionnez **Créer**.

1. Dans le champ Nom, entrez **Environnement** et dans le champ Valeur, entrez **Labos** (cette valeur n’a pas d’importance, la stratégie nécessite simplement une valeur d’étiquette), puis sélectionnez **Suivant : Vérifier + créer >** et **Créer**.

1. Vous voyez le groupe de ressources dans la liste.  

1. Sélectionnez **Accueil** dans la barre de navigation en haut de la page pour revenir à la page d’accueil Azure.

1. Laissez ouvert l’onglet de navigateur, vous en avez besoin pour la tâche suivante.

### Tâche 3 (facultatif)

Dans cette tâche, vous suivez les étapes de correction d’un groupe de ressources non conforme. REMARQUE : l’abonnement Azure utilisé pour le labo prend plus longtemps que d’habitude pour mettre à jour l’état de conformité d’un groupe de ressources corrigé.

1. Dans la page d’accueil Azure, sélectionnez **Stratégie**. La page d’accueil Stratégie s’ouvre sur une vue de tableau de bord.  L’étendue de la vue Tableau de bord est l’abonnement Azure fourni par l’hébergeur de labo autorisé.  

1. Vous devez voir la stratégie que vous avez créée précédemment, sélectionnez-la.

1. En haut de la page, sous Essentials, vous pouvez voir le nom, la description et d’autres informations essentielles.  Notez que la stratégie s’affiche comme non conforme.  Sélectionnez la stratégie pour avoir plus d’informations sur la raison de sa non-conformité. Ici, vous pouvez voir que la ressource resourcegroup1 n’est pas conforme.  Il s’agit d’un exemple de groupe de ressources qui a été créé avant de créer la stratégie. Sélectionnez **Détails** pour plus d’informations.  Ici, vous pouvez voir le message de conformité indiquant qu’une étiquette d’environnement est nécessaire.  Sélectionnez le **X** en haut à droite pour fermer la fenêtre.

1. Sélectionnez **resourcegroup1** et, en haut de la page, sélectionnez **Voir la ressource**.
    1. À côté du champ Étiquettes, sélectionnez **Modifier**
    1. Placez le curseur de la souris dans le champ Étiquette et sélectionnez **Environnement**.
    1. Placez le curseur de la souris dans le champ Valeur et sélectionnez **Labos**, puis **Enregistrer**.

1. Revenez maintenant à la page Stratégie.  Placez le curseur de la souris dans la zone de recherche bleue en haut de la page, puis sélectionnez **Stratégie**.

1. Dans le volet de navigation de gauche, sélectionnez **Conformité**.  Comme sur la page vue d’ensemble, vous pouvez afficher l’état de conformité des stratégies et/ou des initiatives répertoriées.  REMARQUE : même si vous avez ajouté l’étiquette au groupe de ressources, la mise à jour de l’état prend du temps.  Les abonnements Azure utilisés dans les labos peuvent avoir des délais plus longs que la normale. Si vous voulez attendre que l’état de conformité de cette ressource soit mis à jour, n’arrêtez pas le labo. En fonction de l’environnement lab, la mise à jour peut prendre une heure ou plus.  

### Révision

Dans ce labo, vous avez suivi le processus de création d’une attribution de stratégie Azure et avez pu voir l’impact de cette stratégie.

