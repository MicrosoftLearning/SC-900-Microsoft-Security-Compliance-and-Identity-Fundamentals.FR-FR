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

## Scénario de la démonstration

Cette démonstration vous permettra de parcourir les diverses options disponibles pour créer une stratégie d’accès conditionnel.

1. Revenez à l’onglet ouvert du navigateur intitulé « Centre d’administration accueil Microsoft Entra ».  Si vous avez précédemment fermé cet onglet de navigateur, ouvrez Microsoft Edge et connectez-vous à **[entra.microsoft.com](https://entra.microsoft.com)** avec vos informations d’identification d’administrateur Microsoft 365.

1. Dans le volet de navigation gauche, développez **Protection**, puis sélectionnez **Accès conditionnel**.

1. La page de présentation de l’accès conditionnel s’affiche.  Ici, vous verrez des vignettes montrant le résumé de la stratégie et les alertes générales.  Dans le volet de navigation de gauche, sélectionnez **Stratégies**.

1. L’écran des stratégies d’accès conditionnel s’affiche. Toutes les stratégies d’accès conditionnel sont répertoriées ici. Sélectionnez **+ Nouvelle stratégie** pour afficher les paramètres associés à l’accès conditionnel.

1. Dans le champ **Nom**, entrez un nom pour la stratégie.

1. Vous remarquerez que plusieurs options sont disponibles sous **Affectations**.  Les stratégies d’accès conditionnel sont analogues aux instructions conditionnelles (si-alors) : les paramètres d’affectations correspondent donc aux instructions « if ».
    1. **Utilisateurs** : survolez l’icône d’information près de l’intitulé « Utilisateurs » avec votre curseur et expliquez que c’est ici que vous sélectionnez les identités dans le répertoire auquel la stratégie s’applique, y compris les utilisateurs, les groupes et les principaux de service. Sélectionnez **0 utilisateurs et groupes sélectionnés**.  L’option pour inclure ou exclure des utilisateurs ou des groupes apparaît. Sélectionnez et expliquez les paramètres disponibles pour l’onglet **Inclure**, puis faites de même pour l’onglet **Exclure**.
    1. **Ressources cibles** : sélectionnez **Ressources cibles**.  Ici, vous contrôlez l’accès en fonction du trafic d’accès réseau, des applications cloud ou des actions spécifiques.  Développez le champ en dessous de l'emplacement où il est indiqué de sélectionner ce à quoi cette stratégie s'applique.  Vous pouvez ici choisir si la stratégie s'applique aux applications cloud, aux actions de l'utilisateur ou au contexte d'authentification.  
        1. Sélectionnez **Applications cloud**, puis sous l’onglet Inclure, sélectionnez l’option **Sélectionner des applications**, puis sous l’emplacement où il est indiqué **Sélectionner**, sélectionnez **Aucun**, une fenêtre s’ouvrira pour sélectionner une ou plusieurs des applications pour lesquelles la stratégie s’appliquera.
        1. Fermez la fenêtre Sélectionner des applications cloud en cliquant sur le **X** en haut à droite de la fenêtre.
        1. Si le temps le permet, vous pouvez choisir de passer en revue les autres options (actions de l'utilisateur et contexte d'authentification) pour voir les options de configuration pour chacune d'entre elles.
    1. **Conditions** : survolez l’icône d’information près de l’intitulé « Conditions » avec votre curseur et expliquez qu’il s’agit de conditions qui définissent les modalités d’application de la stratégie. Par exemple, ’emplacement. Sélectionnez **0 conditions sélectionnées**. Expliquez les différents « signaux » répertoriés.   Sélectionnez quelques-unes des options en cliquant d’abord sur l’icône d’information afin de la définir, puis en cliquant sur **Non configuré** pour l’élément en particulier afin de montrer les diverses options.
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

1. Sélectionnez le **X** dans le coin supérieur droit de la page pour fermer la stratégie.

1. Fermez les onglets de votre navigateur.

### Révision

Cette démonstration vous a permis de parcourir les diverses options disponibles pour créer une stratégie d’accès conditionnel.
