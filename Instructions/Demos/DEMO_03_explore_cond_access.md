---
demo:
  title: 'Accès conditionnel Azure AD'
  module: 'Module 3 : Décrire les fonctionnalités de gestion des accès d’Azure AD'
---


# <a name="demo-azure-ad-conditional-access"></a>Démonstration : Accès conditionnel Azure AD

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités d’Azure Active Directory (Azure AD) - Solution Microsoft Entra
- Module : Décrire les fonctionnalités de gestion des accès d’Azure AD
- Unité : Décrire l’accès conditionnel dans Azure AD

## <a name="demo-scenario"></a>Scénario de la démonstration

Cette démonstration vous permettra de parcourir les diverses options disponibles pour créer une stratégie d’accès conditionnel.

1. Accédez à l’onglet **Contoso - Microsoft Azure** ouvert dans votre navigateur. Si vous avez fermé l’onglet, ouvrez une page du navigateur et saisissez portal.azure.com dans la barre d’adresse. Ensuite, sélectionnez Azure Active Directory. Vous devriez être connecté en tant qu’administrateur dans le portail Azure : si ce n’est pas le cas, reconnectez-vous.

1. Dans le volet de navigation gauche, sélectionnez **Sécurité**.

1. Dans le volet de navigation gauche, sélectionnez **Accès conditionnel**.

1. L’écran des stratégies d’accès conditionnel s’affiche. Toutes les stratégies d’accès conditionnel sont répertoriées ici. Sélectionnez **+ Nouvelle stratégie** pour afficher les paramètres associés à l’accès conditionnel.

1. Dans le champ **Nom**, entrez un nom pour la stratégie.

1. Vous remarquerez que plusieurs options sont disponibles sous **Affectations**.  Les stratégies d’accès conditionnel sont analogues aux instructions conditionnelles (si-alors) : les paramètres d’affectations correspondent donc aux instructions « if ».
    1. **Utilisateurs et groupes** - Survolez l’icône d’information près de l’intitulé « Utilisateurs et groupes » avec votre curseur et expliquez que c’est ici que vous déterminez les utilisateurs et les groupes dans le répertoire auquel la stratégie s’applique. Sélectionnez **0 utilisateurs et groupes sélectionnés**.  L’option pour inclure ou exclure des utilisateurs ou des groupes apparaît. Sélectionnez et expliquez les paramètres disponibles pour l’onglet **Inclure**, puis faites de même pour l’onglet **Exclure**.
    1. **Applications ou actions cloud** - Survolez l’icône d’information près de l’intitulé « Applications ou actions cloud » avec votre curseur et expliquez que c’est ici que vous définissez les applications utilisées ou les actions effectuées par l’utilisateur pour la stratégie d’accès conditionnel.  Sélectionnez **Pas d’applications cloud, d’actions ni de contextes authentifiés sélectionnés**.
        1. Cliquez sur la flèche de déroulement dans la zone sous l’intitulé **Sélectionner les éléments auxquels s’applique cette stratégie** et prenez note des options proposées.  Ne modifiez pas le paramètre par défaut, Applications cloud.
        1. Sélectionnez les paramètres disponibles pour l’onglet Inclure et expliquez-les. Sous l’onglet **Inclure**, sélectionnez **Sélectionner des applications**.  Une fenêtre s’ouvre, dans laquelle vous pouvez faire votre choix dans une liste d’applications.  Ne sélectionnez rien ; fermez cette fenêtre en cliquant sur le **X** en haut à droite de la fenêtre. Revenez à votre choix et sélectionnez **Aucun** pour supprimer l’erreur.
        1. Ensuite, sélectionnez les paramètres disponibles pour l’onglet **Exclure** et expliquez-les.  Ici aussi, vous pouvez sélectionner des applications spécifiques à exclure.
    1. **Conditions** - Survolez l’icône d’information près de l’intitulé « Conditions » avec votre curseur et expliquez que cette option définit le moment où s’appliquera la stratégie. Sélectionnez **0 conditions sélectionnées**. Expliquez les différents « signaux » répertoriés.   Sélectionnez quelques-unes des options en cliquant d’abord sur l’icône d’information afin de la définir, puis en cliquant sur **Non configuré** pour l’élément en particulier afin de montrer les diverses options.
        1. **Risque de l’utilisateur** - Un risque de l’utilisateur reflète la probabilité qu’une identité ou un compte donné soit compromis. Ces risques sont calculés hors connexion à l’aide de sources d’informations sur les menaces internes et externes de Microsoft.
        1. **Risque de connexion** - Un risque de connexion reflète la probabilité qu’une requête d’authentification donnée soit rejetée par le propriétaire de l’identité. Par exemple, lorsque la connexion est établie depuis une adresse IP anonyme ou au cours d’un voyage atypique.
        1. **Plateforme d’appareil** - La plateforme à partir de laquelle l’utilisateur se connecte. Par exemple, « iOS ».
        1. **Emplacement** - L’emplacement (déterminé selon la plage d’adresses IP) à partir duquel l’utilisateur se connecte
        1. **Applications client** - Le logiciel dont se sert l’utilisateur pour accéder à l’application cloud. Par exemple, « Navigateur ».
        1. **Filtre pour les appareils** - Quand ils créent des stratégies d’accès conditionnel, les administrateurs peuvent cibler ou exclure des appareils spécifiques dans leur environnement. Les administrateurs peuvent maintenant cibler des appareils spécifiques à l’aide des opérateurs et propriétés pris en charge pour les filtres d’appareil et les autres conditions d’attribution disponibles dans vos stratégies d’accès conditionnel.

1. **Contrôles d’accès** - Pour en revenir à l’analogie des stratégies d’accès conditionnel aux instructions conditionnelles, les contrôles d’accès sont analogues à l’instruction « then ».
    1. **Octroi** - Survolez l’icône d’information près de l’intitulé « Octroi » avec votre curseur pour en lire la description.  Sélectionnez **0 contrôles sélectionnés** pour afficher les différentes options.  Expliquez certaines d’entre elles.  Présentez en particulier l’option **Demander l’authentification multifacteur** sous Accorder l’accès et expliquez de quelle manière cette option s’utilise pour contrôler précisément les conditions où est exigée la MFA.   Expliquez aussi que vous pouvez définir plusieurs contrôles et tous les exiger, ou seulement imposer l’un des contrôles sélectionnés.
    1. **Session** - Survolez l’icône d’information près de l’intitulé « Session » avec votre curseur pour en lire la description.  Expliquez que les Contrôles de session permettent de limiter l’expérience dans une application cloud.  Par exemple, l’utilisateur pourra accéder à l’application cloud, mais il ne pourra télécharger aucun contenu ni imprimer quoi que ce soit.  Il s’agit là d’un sujet plus complexe : n’entrez pas dans les détails.

1. Une fois la stratégie configurée, vous pouvez l’activer en sélectionnant **Activée**, puis en cliquant sur le bouton **Créer** pour créer une stratégie.

1. Sélectionnez le **X** en haut à droite de la page pour quitter la stratégie, puis sélectionnez Microsoft Azure sur la barre bleue en haut de la page pour revenir à la page d’accueil du portail Azure.

1. Gardez cette page du navigateur ouverte pour la démonstration suivante.

### <a name="review"></a>Révision

Cette démonstration vous a permis de parcourir les diverses options disponibles pour créer une stratégie d’accès conditionnel.
