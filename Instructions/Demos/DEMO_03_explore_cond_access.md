<!---
---
Démonstration : Titre : « Accès conditionnel Azure AD » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra ; Module 3 : Décrire les fonctionnalités de gestion des accès de Microsoft Entra ID ; Unité 2 : Décrire l’accès conditionnel »
---
--->

# Démonstration : accès conditionnel Microsoft Entra

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra
- Module : décrire les fonctionnalités de gestion des accès de Microsoft Entra ID
- Leçon : décrire l’accès conditionnel

## Scénario de démonstration

Cette démonstration vous permettra de parcourir les diverses options disponibles pour créer une stratégie d’accès conditionnel.

1. Revenez à l’onglet ouvert du navigateur intitulé « Centre d’administration accueil Microsoft Entra ».  Si vous avez précédemment fermé cet onglet de navigateur, ouvrez Microsoft Edge et connectez-vous à **[entra.microsoft.com](https://entra.microsoft.com)** avec vos informations d’identification d’administrateur Microsoft 365.

1. Dans le volet de navigation gauche, développez **Protection**, puis sélectionnez **Accès conditionnel**.

1. La page de présentation de l’accès conditionnel s’affiche.  Ici, vous pouvez voir les informations sur le résumé de la stratégie, les nouveautés et les alertes générales.  Dans le volet de navigation de gauche de la fenêtre Accès conditionnel, sélectionnez **Stratégies**.

1. L’écran Stratégies d’accès conditionnel s’affiche. Toute stratégie d’accès conditionnel existante est répertoriée ici. Pour afficher les paramètres associés à l’accès conditionnel, sélectionnez **+ Nouvelle stratégie**.

1. Dans le champ **Nom**, entrez un nom pour la stratégie.

1. Remarquez que vous disposez de plusieurs options sous **Affectations**.  Étant donné que les stratégies d’accès conditionnel sont comparables aux instructions si/alors, les paramètres d’affectation sont comparables aux instructions « si ».
    1. **Utilisateurs** : survolez l’icône d’information près de l’intitulé « Utilisateurs » avec votre curseur et expliquez que c’est ici que vous sélectionnez les identités dans le répertoire auquel la stratégie s’applique, y compris les utilisateurs, les groupes et les principaux de service. Sélectionnez **0 utilisateur et groupe sélectionné**.  L’option pour inclure ou exclure des utilisateurs ou des groupes apparaît. Sélectionnez et énoncez les paramètres disponibles pour l’onglet **Inclure**, puis sélectionnez et énoncez les paramètres disponibles pour l’onglet **Exclure**.
    1. **Ressources cibles** : sélectionnez **Ressources cibles**.  Ici, vous contrôlez l’accès en fonction du trafic d’accès réseau, des applications cloud ou des actions spécifiques.  Développez le champ en dessous de l'emplacement où il est indiqué de sélectionner ce à quoi cette stratégie s'applique.  Vous pouvez ici choisir si la stratégie s'applique aux applications cloud, aux actions de l'utilisateur ou au contexte d'authentification.  
        1. Sélectionnez **Applications cloud**, puis sous l’onglet Inclure, sélectionnez l’option **Sélectionner des applications**, puis sous l’emplacement où il est indiqué **Sélectionner**, sélectionnez **Aucun**, une fenêtre s’ouvrira pour sélectionner une ou plusieurs des applications pour lesquelles la stratégie s’appliquera.
        1. Fermez la fenêtre Sélectionner des applications cloud en cliquant sur le **X** en haut à droite de la fenêtre.
        1. Si le temps le permet, vous pouvez choisir de passer en revue les autres options (actions de l'utilisateur et contexte d'authentification) pour voir les options de configuration pour chacune d'entre elles.
    1. **Réseau** - Pointez votre souris sur l’icône d’informations à côté de l’indication « Réseau ».  Soulignez que les emplacements réseau sont déterminés par la plage d’adresses IP ou par les coordonnées GPS à partir desquelles l’utilisateur se connecte.  Sélectionnez **Non configuré** pour afficher les options disponibles.
    1. **Conditions** : survolez l’icône d’information près de l’intitulé « Conditions » avec votre curseur et expliquez qu’il s’agit de conditions qui définissent les modalités d’application de la stratégie. Par exemple, ’emplacement. Sélectionnez **0 condition sélectionnée**. Parlez des différents « signaux » répertoriés.   Sélectionnez quelques-unes des options en sélectionnant d’abord l’icône d’information pour définir de quoi il s’agit, puis en sélectionnant **Non configuré** pour l’élément spécifique afin d’afficher les différentes options.
        1. **Risque de l’utilisateur** - Un risque de l’utilisateur reflète la probabilité qu’une identité ou un compte donné soit compromis. Ces risques sont calculés hors connexion à l’aide de sources d’informations sur les menaces internes et externes de Microsoft.
        1. **Risque de connexion** - Un risque de connexion reflète la probabilité qu’une requête d’authentification donnée soit rejetée par le propriétaire de l’identité. Il peut s’agir, par exemple, d’une connexion à partir d’une adresse IP anonyme, d’un voyage atypique, etc.
        1. **Risque interne** - Le risque interne, configuré dans la protection adaptative, évalue les risques en fonction des activités à risque d’un utilisateur qui concernent des données.
        1. **Plateforme d’appareil** - La plateforme à partir de laquelle l’utilisateur se connecte. Par exemple « iOS ».
        1. **Emplacement** - L’emplacement (déterminé selon la plage d’adresses IP) à partir duquel l’utilisateur se connecte
        1. **Applications client** - Le logiciel dont se sert l’utilisateur pour accéder à l’application cloud. Par exemple « Navigateur ».
        1. **Filtre pour les appareils** - Quand ils créent des stratégies d’accès conditionnel, les administrateurs peuvent cibler ou exclure des appareils spécifiques dans leur environnement. Les administrateurs peuvent maintenant cibler des appareils spécifiques à l’aide des opérateurs et propriétés pris en charge pour les filtres d’appareil et les autres conditions d’attribution disponibles dans vos stratégies d’accès conditionnel.

1. **Contrôles d’accès** : pour revenir à l’analogie entre les stratégies d’accès conditionnel et les instructions « si » et « alors », les contrôles d’accès sont comparables à l’instruction « alors ».
    1. **Octroi** - Survolez l’icône d’information près de l’intitulé « Octroi » avec votre curseur pour en lire la description.  Sélectionnez **0 contrôle sélectionné** pour afficher les différentes options.  Parlez de certaines d’entre elles.  Présentez en particulier l’option **Demander l’authentification multifacteur** sous Accorder l’accès et expliquez de quelle manière cette option s’utilise pour contrôler précisément les conditions où est exigée la MFA.   Précisez également que vous pouvez définir plusieurs contrôles et exiger tous les contrôles sélectionnés ou un seul d’entre eux.
    1. **Session** - Survolez l’icône d’information près de l’intitulé « Session » avec votre curseur pour en lire la description.  Précisez que les contrôles de session permettent de limiter l’expérience dans un logiciel cloud  Par exemple, l’utilisateur pourra accéder à l’application cloud, mais il ne pourra télécharger aucun contenu ni imprimer quoi que ce soit.  Il s’agit d’un sujet plus complexe, il faut donc faire simple.

1. Une fois qu’une stratégie est configurée, vous pouvez l’activer en sélectionnant **Activer**, puis en appuyant sur le bouton **Créer** pour créer une stratégie.

1. Sélectionnez le **X** dans le coin supérieur droit de la page pour fermer la stratégie.

1. Fermez les onglets de votre navigateur.

### Révision

Cette démonstration vous a permis de parcourir les diverses options disponibles pour créer une stratégie d’accès conditionnel.
