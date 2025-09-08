---
lab:
  title: "Explorer la gestion des risques internes dans Microsoft\_Purview"
  module: Describe the data security solutions of Microsoft Purview
---

# Labo : Explorer la gestion des risques internes dans Microsoft Purview

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : décrire les fonctionnalités de Microsoft Priva et Microsoft Purview
- Module : décrire les solutions de sécurité des données de Microsoft Purview
- Unité : décrire la gestion des risques internes dans Microsoft Purview

## Scénario du labo

Dans ce labo, vous suivez le processus de configuration d’une stratégie des risques internes, ainsi que les prérequis de base pour configurer et utiliser des stratégies de gestion des risques internes.  Remarque : ce labo aborde seulement les questions de configuration de la gestion des risques internes et les options associées à la création d’une stratégie.  Ce labo ne comprend pas de tâche pour déclencher la stratégie, car le nombre d’événements et le temps nécessaires ne sont pas couverts par cet exercice.

**Durée estimée :** 60 minutes

### Tâche 1

Dans cette tâche, vous explorez les différentes autorisations de rôle pour Gestion des risques internes et vérifiez que des utilisateurs spécifiques ont déjà été inclus dans le groupe de rôles Gestion des risques internes. S’assurer que les utilisateurs disposent des autorisations de rôle appropriées garantit que les utilisateurs désignés peuvent accéder aux fonctionnalités de gestion des risques internes et les gérer. Lors de l’ajout de membres à un groupe de rôles, l’application des autorisations de groupe de rôles à des utilisateurs au sein de l’organisation peut prendre jusqu’à 30 minutes.

1. Ouvrez l’onglet du navigateur menant sur la page d’accueil de Microsoft Purview.  Si vous l’avez précédemment fermé, ouvrez un onglet du navigateur et entrez **https://admin.microsoft.com** . Connectez-vous avec les identifiants d’administration du tenant (ou « locataire/abonné ») Microsoft 365 fournis par l’hôte de labo autorisé (ALH). 

1. Dans le volet de navigation de gauche du centre d’administration Microsoft 365, sélectionnez **Tout afficher**, puis **Microsoft Purview**.  Une nouvelle page de navigateur s’ouvre sur la page d’accueil du portail Microsoft Purview.  

1. Dans le volet de navigation de gauche, sélectionnez **Paramètres**, développez **Rôles et étendues**, puis sélectionnez **Groupes de rôles**.

1. Dans le champ de recherche, en haut à droite de la page, saisissez **Risque interne**, puis appuyez sur Entrée.  Notez les nombreux rôles qui s’affichent.  Chacun d’eux a des niveaux d’accès différents.  Sélectionnez **Gestion des risques internes** et passez en revue la description.  Faites défiler jusqu’aux membres et notez qu’Administrateur MOD et Megan Bowen sont listés. Fermez la fenêtre en sélectionnant le symbole **X** en haut à droite de la fenêtre.

1. Dans le volet de navigation de gauche, sélectionnez **Accueil** pour revenir à la page du portail Microsoft Purview.

1. Gardez cet onglet ouvert, car vous y revenez dans une tâche ultérieure.

### Tâche 2

Dans cette tâche, vous parcourez les paramètres associés à la solution Gestion des risques internes.  Les paramètres de gestion des risques internes s’appliquent à toutes les stratégies de gestion des risques internes, quel que soit le modèle choisi lors de la création de la stratégie.

1. Vous devez vous trouver dans la page d’accueil du portail Microsoft Purview.

1. Avant de commencer à configurer une stratégie, un administrateur doit connaître certains paramètres et les configurer en fonction des besoins de son organisation. Dans le volet de navigation de gauche, sélectionnez **Paramètres**, puis **Gestion des risques internes**.  Ici, vous allez explorer certains des paramètres disponibles.
    1. Sélectionnez **Confidentialité** : pour les utilisateurs dont les activités correspondent à vos stratégies de risque interne, ce paramètre détermine l’affichage de leur véritable identité ou l’utilisation de version anonymisées pour masquer leurs identités.  Pour les besoins de cette démonstration, vous pouvez garder le paramètre par défaut.
    1. Sélectionnez **Indicateurs de stratégie**. Lorsqu’un événement déclencheur de stratégie survient, les activités qui correspondent aux indicateurs sélectionnés sont utilisées pour déterminer le score de risque pour l’utilisateur. Les indicateurs de stratégie sélectionnés ici sont inclus dans les modèles de stratégie de risque de risque lié aux menaces internes.  Faites défiler l’écran pour afficher tous les indicateurs disponibles et toutes les informations associées.  Sous **Indicateurs d’Office**, sélectionnez **Sélectionner tout**. Les options que vous sélectionnez sur cet écran sont incluses dans vos modèles de stratégie.
    1. Sélectionnez **Périodes de la stratégie**. Les périodes que vous choisissez ici entrent en vigueur pour un utilisateur lorsqu’il déclenche une correspondance pour une stratégie de risque interne.   La fenêtre Activation détermine la durée pendant laquelle les stratégies détecteront activement l’activité des utilisateurs. Elle se déclenche lorsqu’un utilisateur effectue la première activité correspondant à une stratégie. La détection des activités passées détermine jusqu’où une stratégie doit remonter pour détecter l’activité d’un utilisateur. Cette détection se déclenche lorsqu’un utilisateur effectue la première activité correspondant à une stratégie.  Laissez les valeurs par défaut.
    1. Sélectionnez **Détections intelligentes**. Passez en revue les options présentées ici.  Notez les paramètres des domaines et leur relation avec les indicateurs.
    1. Explorez les autres éléments répertoriés dans les paramètres et notez que nombre d’entre eux sont en préversion.

1. Dans le volet de navigation de gauche, sélectionnez **Solutions**, puis **Gestion des risques internes**.

1. Gardez cet onglet ouvert, car vous l’utilisez dans la prochaine tâche.

### Tâche 3

Lors de la création d’une stratégie de gestion des risques internes, vous devez choisir des options : une stratégie rapide ou une stratégie personnalisée. Les paramètres de stratégie rapide remplissent automatiquement les meilleures pratiques recommandées ou les résultats de la dernière analyse analytique de votre organisation.  Dans cette tâche, vous parcourez les paramètres de création d’une stratégie personnalisée. L’objectif est d’avoir simplement une idée des diverses options et de la flexibilité du processus de création d’une stratégie.

1. Vous devriez être sur la page de présentation de gestion des risques internes.  Si ce n’est pas déjà fait, sélectionnez **Solutions** dans le volet de navigation de gauche, puis **Gestion des risques internes**.

1. Sur la page générale de gestion des risques internes, sélectionnez l’onglet **Stratégies**, puis sélectionnez **+ Créer une stratégie** et sélectionnez **Stratégie personnalisée**. Configurez chacun des onglets de stratégie suivants.

    1. Modèle de stratégie : sous la catégorie Fuites de données, sélectionnez **Fuites de données**.  Lisez les détails du modèle. Sous les prérequis, la stratégie DLP s’affiche avec une coche dans un cercle vert pour indiquer que le prérequis est rempli.  Il y a une stratégie DLP préconfigurée pour ce locataire lab. Cliquez sur **Suivant**.
    1. Nom et description : saisissez un nom, **`SC900-InsiderRiskPolicy`**, puis sélectionnez **Suivant**.
    1. Utilisateurs et groupes : passez en revue la zone d’informations.  Conservez le paramètre par défaut, **Inclure tous les utilisateurs et groupes**.  Cliquez sur **Suivant**.
    1. Exclure les utilisateurs et les groupes (facultatif) : Ici, vous pouvez répertorier les utilisateurs et les groupes à exclure. Ne changez rien. Cliquez sur **Suivant**.
    1. Contenu prioritaire : selon la description, les scores de risque sont augmentés pour toute activité qui contient du contenu prioritaire, ce qui augmente les chances de générer une alerte de gravité élevée. Par souci de simplicité, sélectionnez **Je ne veux pas indiquer de contenu prioritaire pour l’instant**, puis sélectionnez **Suivant**.
    1. Déclencheurs : l’événement déclencheur détermine quand une stratégie doit commencer à attribuer des scores de risque à l’activité d’un utilisateur.  Vous pouvez choisir une stratégie DLP existante ou indiquer que l’utilisateur doit effectuer une activité d’exfiltration. Sélectionnez **L’utilisateur correspond à une stratégie de protection contre la perte de données (DLP)**, puis, dans la liste déroulante, sélectionnez **U.S. Financial Data**. Cliquez sur **Suivant**.
    1. Indicateurs : Développez **Indicateurs d’Office**. Notez la façon dont la zone pour Indicateurs d’Office est déjà sélectionnée, en fonction des paramètres de la tâche précédente.  Vous pouvez désélectionner certains indicateurs sélectionnés ou en ajouter de nouveaux en sélectionnant Choisir des indicateurs. Pour cet exercice, laissez les paramètres actuels comme tels et sélectionnez **Suivant**.
    1. Dans la page Options de détection, gardez tous les paramètres par défaut, mais lisez la description associée aux différentes options et pointez sur l’icône d’informations pour obtenir des informations plus détaillées sur un paramètre spécifique.  Cliquez sur **Suivant**.
    1. Dans la page Décider s’il faut utiliser les seuils d’indicateur par défaut ou ceux du client, gardez le paramètre par défaut **Appliquer les seuils fournis par Microsoft**, puis sélectionnez **Suivant**.
    1. Terminer : passez en revue les paramètres, puis sélectionnez **Envoyer**.
    1. Passez en revue la description de ce qui se passe ensuite, puis sélectionnez **Terminé**.

1. Vous revenez alors à l’onglet Stratégies de la page Gestion des risques internes.  La stratégie que avez créée est listée.  Si vous ne la voyez pas, sélectionnez l’icône **Actualiser**.

1. En tant qu’administrateur, vous pouvez commencer immédiatement à attribuer des scores de risque aux utilisateurs en fonction de l’activité détectée par les stratégies que vous avez sélectionnées. Cela évite qu’un événement déclencheur (comme une correspondance de stratégie DLP) soit détecté en premier.  L’administrateur sélectionne le carré vide à côté du nom de la stratégie pour la choisir, puis sélectionne **Commencer à noter l’activité des utilisateurs** au-dessus du tableau des stratégies.  Une nouvelle fenêtre s’ouvre et l’administrateur doit remplir les champs disponibles. Laissez les champs vides, car vous ne configurez pas cette option, mais pour avoir plus d’informations sur les raisons de la configurer, sélectionnez **Pourquoi le faire ?**.  Fermez la fenêtre en sélectionnant le **X** en haut à droite de la fenêtre.

1. Dans le volet de navigation de gauche, sélectionnez **Accueil** pour revenir à la page de destination du portail Microsoft Purview.

1. Laissez l’onglet du navigateur ouvert.

### Révision

Dans ce labo, vous avez suivi le processus de configuration d’une stratégie des risques internes, ainsi que les prérequis de base pour configurer et utiliser des stratégies de gestion des risques internes.
