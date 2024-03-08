---
lab:
  title: "Explorer la gestion des risques internes dans Microsoft\_Purview"
  module: Describe the insider risk capabilities in Microsoft Purview
---

# Labo : Explorer la gestion des risques internes dans Microsoft Purview

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft
- Module : Décrire les fonctionnalités propres aux risques internes de Microsoft Purview
- Unité : Décrire la gestion des risques internes

## Scénario du labo

Dans ce labo, vous suivez le processus de configuration d’une stratégie des risques internes, ainsi que les prérequis de base pour configurer et utiliser des stratégies de gestion des risques internes.  Remarque : ce labo aborde seulement les questions de configuration de la gestion des risques internes et les options associées à la création d’une stratégie.  Ce labo ne comprend pas de tâche pour déclencher la stratégie, car le nombre d’événements et le temps nécessaires ne sont pas couverts par cet exercice.

**Durée estimée** : 45 à 60 minutes

### Tâche 1

Dans cette tâche, en tant qu’administrateur général, vous allez activer les autorisations pour la gestion des risques internes.  Plus particulièrement, vous ajoutez des utilisateurs au groupe du rôle Gestion des risques internes pour que les personnes désignées puissent accéder aux fonctionnalités de gestion des risques internes et les gérer.  L’application des autorisations du groupe de rôles aux utilisateurs de l’ensemble de l’organisation peut prendre jusqu’à 30 minutes.

1. Ouvrez l’onglet du navigateur menant sur la page d’accueil de Microsoft Purview.  Si vous l’avez précédemment fermé, ouvrez un onglet du navigateur et entrez **https://admin.microsoft.com** . Connectez-vous avec les identifiants d’administration du tenant (ou « locataire/abonné ») Microsoft 365 fournis par l’hôte de labo autorisé (ALH). Dans le volet de navigation gauche du Centre d’administration Microsoft 365, sélectionnez **Tout afficher**, puis **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.  

1. Dans le volet de navigation gauche, développez **Rôles et étendues**, puis sélectionnez **Autorisations**.

1. Sous Solutions Microsoft Purview, sélectionnez **Rôles**.

1. Dans le champ de recherche, tapez **Risque interne**, puis appuyez sur Entrée.  Notez les nombreux rôles qui s’affichent.  Chacun d’eux a des niveaux d’accès différents.  Sélectionnez **Gestion des risques internes** et passez en revue la description.  Faites défiler jusqu’aux membres et notez qu’Administrateur MOD et Megan Bowen sont listés. Fermez la fenêtre en sélectionnant le **X** en haut à droite de la fenêtre.

1. Dans le volet de navigation de gauche, sélectionnez **Accueil** pour revenir à la page du portail de conformité Microsoft Purview.

1. Gardez cet onglet ouvert, car vous y revenez dans une tâche ultérieure.

### Tâche 2 (REMARQUE : IGNOREZ Tâche 2 si vous avez effectué le labo de configuration pour activer le journal d’audit)

La gestion des risques internes utilise les journaux d’audit de Microsoft 365 pour les insights utilisateur, les activités identifiées dans les stratégies et les insights d’analyse. Dans cette tâche, vous activez la fonctionnalité de recherche du Journal d’audit. Remarque : plusieurs heures peuvent s’écouler après l’activation de la recherche dans le journal d’audit avant de pouvoir renvoyer des résultats lorsque vous recherchez dans le journal d’audit.  Bien que plusieurs heures puissent s’écouler avant que vous puissiez effectuer une recherche dans le journal d’audit, vous pourrez continuer à effectuer les autres tâches de ce labo.

1. Sélectionnez l’onglet de navigateur intitulé, **Accueil - Page de conformité Microsoft 365**.  Si vous avez déjà fermé cet onglet de navigateur, ouvrez Microsoft Edge et entrez **compliance.microsoft.com** dans la barre d’adresses, puis connectez-vous avec vos informations d’identification d’administrateur.

1. Dans le volet de navigation de gauche, sous Solutions, sélectionnez **Audit**.

1. Vérifiez que l’onglet **Nouvelle recherche** est sélectionné (souligné).

1. Lorsque vous arrivez sur la page Audit, attendez 2 à 3 minutes.  Si l’audit n’est PAS activé, vous voyez une barre bleue en haut de la page indiquant de commencer à enregistrer les activités des utilisateurs et des administrateurs.  Sélectionnez **Commencer à enregistrer les activités de l’utilisateur et de l’administrateur**.  Une fois l’audit activé, la barre bleue disparaît.  S’il n’y a pas de barre bleue, alors l’audit est déjà activé et aucune autre action n’est requise.

1. Retournez à la page d’accueil du portail de conformité Microsoft Purview en sélectionnant **Accueil** dans le volet de navigation de gauche.

1. Gardez cet onglet ouvert, car vous l’utilisez dans la prochaine tâche.

### Tâche 3

Dans cette tâche, vous parcourez les paramètres associés à la solution Gestion des risques internes.  Les paramètres de gestion des risques internes s’appliquent à toutes les stratégies de gestion des risques internes, quel que soit le modèle choisi lors de la création de la stratégie.

1. Vous devez vous trouver dans la page d’accueil du portail de conformité Microsoft Purview. Si ce n’est pas le cas, ouvrez l’onglet de navigateur **Accueil - Conformité Microsoft 365**.

1. Dans le volet de navigation de gauche, sous Solutions, sélectionnez **Gestion des risques internes**.

1. Avant de commencer à configurer une stratégie, un administrateur doit connaître certains paramètres et les configurer en fonction des besoins de son organisation. Dans la page Gestion des risques internes, sélectionnez l’**icône d’engrenage des paramètres** en haut à droite de la fenêtre pour accéder aux paramètres Risques internes.  
    1. Vérifiez que vous êtes dans l’onglet **Confidentialité** : pour les utilisateurs dont les activités correspondent à vos stratégies de risque lié aux menaces internes, ce paramètre détermine l’affichage ou non de leur véritable identité.  Pour les besoins de cette démonstration, vous pouvez garder le paramètre par défaut.
    1. Sélectionnez l’onglet **Indicateurs de stratégie**. Lorsqu’un événement déclencheur de stratégie survient, les activités qui correspondent aux indicateurs sélectionnés sont utilisées pour déterminer le niveau de risque pour l’utilisateur. Les indicateurs de stratégie sélectionnés ici sont inclus dans les modèles de stratégie de risque de risque lié aux menaces internes.  Faites défiler l’écran pour afficher tous les indicateurs disponibles et toutes les informations associées. Sous **Indicateurs Office**, sélectionnez **Tout sélectionner**, puis **Enregistrer** en bas de la page (vous devez faire défiler vers le bas).
    1. Sélectionnez l’onglet **Périodes de la stratégie**. Les périodes que vous choisissez ici entrent en vigueur pour un utilisateur lorsqu’il déclenche une correspondance pour une stratégie de risque lié aux menaces internes.   La fenêtre Activation détermine la durée pendant laquelle les stratégies détecteront activement l’activité des utilisateurs. Elle se déclenche lorsqu’un utilisateur effectue la première activité correspondant à une stratégie. La détection des activités passées détermine jusqu’où une stratégie doit remonter pour détecter l’activité d’un utilisateur. Cette détection se déclenche lorsqu’un utilisateur effectue la première activité correspondant à une stratégie.  Laissez les valeurs par défaut.
    1. Sélectionnez l’onglet **Détections intelligentes**. Passez en revue les options proposées.  Notez les paramètres des domaines et leur relation avec les indicateurs.
    1. Explorez les autres éléments répertoriés dans les paramètres et notez que nombre d’entre eux sont en préversion.

1. Pour revenir à la vue d’ensemble de la gestion des risques internes, sélectionnez **Gestion des risques internes** dans le coin supérieur gauche de la page, au-dessus de Paramètres.

1. Gardez cet onglet ouvert, car vous l’utilisez dans la prochaine tâche.

### Tâche 4

Dans cette tâche, vous parcourez les paramètres de création d’une stratégie.  L’objectif est d’avoir simplement une idée des diverses options et de la flexibilité du processus de création d’une stratégie.

1. Vous devriez être sur la page de gestion des risques internes.  Si ce n’est déjà fait, ouvrez l’onglet du navigateur étiqueté **Gestion des risques internes - Conformité Microsoft 365**.

1. Sur la page générale de gestion des risques internes, sélectionnez l’onglet **Stratégies**, puis **+ Créer une stratégie**.  Configurez chacun des onglets de stratégie suivants.

    1. Modèle de stratégie : sous la catégorie Fuites de données, sélectionnez **Fuites de données**.  Lisez les détails du modèle. Sous les prérequis, la stratégie DLP s’affiche avec une coche dans un cercle vert pour indiquer que le prérequis est rempli.  Il y a une stratégie DLP préconfigurée pour ce locataire lab. Cliquez sur **Suivant**. 
    1. Nom et description : saisissez un nom, **SC900-InsiderRiskPolicy**, puis sélectionnez **Suivant**.
    1. Utilisateurs et groupes : passez en revue la zone d’informations.  Conservez le paramètre par défaut, **Inclure tous les utilisateurs et groupes**.  Cliquez sur **Suivant**.
    1. Contenu prioritaire : selon la description, les scores de risque sont augmentés pour toute activité qui contient du contenu prioritaire, ce qui augmente les chances de générer une alerte de gravité élevée. Par souci de simplicité, sélectionnez **Je ne veux pas indiquer de contenu prioritaire pour l’instant**, puis sélectionnez **Suivant**.
    1. Déclencheurs : l’événement déclencheur détermine quand une stratégie doit commencer à attribuer des scores de risque à l’activité d’un utilisateur.  Vous pouvez choisir une stratégie DLP existante ou indiquer que l’utilisateur doit effectuer une activité d’exfiltration. Sélectionnez **L’utilisateur correspond à une stratégie de protection contre la perte de données (DLP)**, puis, dans la liste déroulante, sélectionnez **U.S. Financial Data**. Cliquez sur **Suivant**.
    1. Indicateurs : notez que tous les indicateurs Office que vous avez sélectionnés dans la tâche précédente sont sélectionnés (vous pouvez le voir en sélectionnant la flèche vers le bas à côté d’Indicateurs Office), puis sélectionnez **Suivant**.
    1. Dans la page Options de détection, gardez tous les paramètres par défaut, mais lisez la description associée aux différentes options et pointez sur l’icône d’informations pour obtenir des informations plus détaillées sur un paramètre spécifique.  Cliquez sur **Suivant**.
    1. Dans la page Décider s’il faut utiliser les seuils d’indicateur par défaut ou ceux du client, gardez le paramètre par défaut **Appliquer les seuils fournis par Microsoft**, puis sélectionnez **Suivant**.
    1. Terminer : passez en revue les paramètres, puis sélectionnez **Envoyer**.
    1. Passez en revue la description de ce qui se passe ensuite, puis sélectionnez **Terminé**.

1. Vous revenez alors à l’onglet Stratégies de la page Gestion des risques internes.  La stratégie que avez créée est listée.  Si vous ne la voyez pas, sélectionnez l’icône **Actualiser**.

1. En tant qu’administrateur, vous pouvez commencer immédiatement à attribuer des scores de risque aux utilisateurs en fonction de l’activité détectée par les stratégies que vous avez sélectionnées. Cela évite qu’un événement déclencheur (comme une correspondance de stratégie DLP) soit détecté en premier.  L’administrateur sélectionne le carré vide à côté du nom de la stratégie pour la choisir, puis sélectionne **Commencer à noter l’activité des utilisateurs** au-dessus du tableau des stratégies.  Une nouvelle fenêtre s’ouvre et l’administrateur doit remplir les champs disponibles. Laissez les champs vides, car vous ne configurez pas cette option, mais pour avoir plus d’informations sur les raisons de la configurer, sélectionnez **Pourquoi le faire ?**.  Fermez la fenêtre en sélectionnant le **X** en haut à droite de la fenêtre.

1. Dans le volet de navigation de gauche, sélectionnez **Accueil** pour revenir à la page d’accueil du portail de conformité Microsoft Purview.

1. Laissez l’onglet du navigateur ouvert.

### Révision

Dans ce labo, vous avez suivi le processus de configuration d’une stratégie des risques internes, ainsi que les prérequis de base pour configurer et utiliser des stratégies de gestion des risques internes.
