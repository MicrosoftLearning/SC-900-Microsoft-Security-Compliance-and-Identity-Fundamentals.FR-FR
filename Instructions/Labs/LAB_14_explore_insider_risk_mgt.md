---
ms.openlocfilehash: 553860b67fc7cc2b181e874e4c57fb4bc972822b
ms.sourcegitcommit: 15658ca1c7bae8a4dbaa33ab6f897070bde521b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/12/2022
ms.locfileid: "147892699"
---
<a name="---"></a><!--->
---
Labo : Titre : « Explorer la gestion des risques internes dans Microsoft Purview » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft ; Module 4 : Décrire les fonctionnalités propres aux risques internes de Microsoft Purview ; Unité 2 : Décrire la gestion des risques internes »
---
--->

# <a name="lab-explore-insider-risk-management-in-microsoft-purview"></a>Labo : Explorer la gestion des risques internes dans Microsoft Purview

Ce labo correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités des solutions de conformité Microsoft
- Module : Décrire les fonctionnalités propres aux risques internes de Microsoft Purview
- Unité : Décrire la gestion des risques internes

## <a name="lab-scenario"></a>Scénario du labo

Ce labo va vous apprendre à paramétrer une stratégie de risque lié aux menaces internes, ainsi que les prérequis de base pour configurer et utiliser des stratégies de gestion des risques internes.  Remarque : ce labo aborde seulement les questions de configuration de la gestion des risques internes et les options associées à la création d’une stratégie.  Il ne propose pas de tâche destinée au déclenchement de la stratégie, car le nombre d’événements que cela nécessite serait inadapté à cet exercice.

**Durée estimée** : 25-30 minutes

### <a name="task-1"></a>Tâche 1

Dans cette tâche, vous allez jouer le rôle d’administrateur général et accorder les autorisations pour la gestion des risques internes.  Plus particulièrement, vous allez ajouter des utilisateurs au groupe qui en a la charge, afin de vous assurer que les personnes désignées peuvent accéder et gérer les fonctionnalités de gestion des risques internes.  Les autorisations accordées au groupe de rôles commencent à s’appliquer aux utilisateurs de toute l’organisation sous 30 minutes.

1. Ouvrez Microsoft Edge. Saisissez **admin.microsoft.com** dans la barre d’adresse.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.

    1. Saisissez le mot de passe d’administrateur communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**. Vous accédez ainsi à la page du Centre d’administration Microsoft 365.

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous les Centres d’administration, sélectionnez **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.  

1. Dans le volet de navigation situé à gauche du portail de conformité Microsoft Purview, sélectionnez **Autorisations**.

1. Dans la page Autorisations et rôles, sous « Afficher et gérer les rôles utilisés pour effectuer des tâches spécifiques à la solution dans le centre de conformité ». Sélectionnez **Rôles**.

1. Dans le champ, saisissez **Risque interne** avant de sélectionner l’icône de recherche (en forme de loupe).  Notez les nombreux rôles qui s’affichent.  aux niveaux d’accès différents.  Sélectionnez **Gestion des risques internes**.

1. Dans la fenêtre qui s’affiche, à côté des Membres, sélectionnez **Modifier**.

1. Pour ajouter des membres à ce groupe, sélectionnez **Choisir des membres**,

1. Sélectionnez **+ Ajouter** en haut de la page.

1. Dans la liste des noms, sélectionnez **Administrateur MOD**, **Megan Bowen**, puis **Ajouter** et **Terminé** en bas de la page.

1. Après avoir vérifié que les membres ajoutés ne comportent aucune erreur, sélectionnez **Enregistrer**.

1. En bas de la fenêtre de gestion des risques internes, sélectionnez **Fermer**.

1. Dans le volet de navigation de gauche, sélectionnez **Accueil** pour revenir à la page du portail de conformité Microsoft Purview.

1. Conservez cet onglet ouvert pour pouvoir y revenir lors d’une prochaine tâche.

### <a name="task-2-skip-if-you-did-the-setup-lab-task-to-enable-the-audit-log"></a>Tâche 2 (IGNOREZ cette étape si vous avez suivi le labo sur la configuration du journal d’audit)

La gestion des risques internes utilise les journaux d’audit de Microsoft 365 pour recueillir les commentaires et les activités en provenance des utilisateurs et identifiés dans les stratégies et les résultats d’analyse. Dans cette tâche, vous allez activer la fonctionnalité de recherche du Journal d’audit. Remarque :  vous devrez peut-être attendre plusieurs heures après l’activation avant de pouvoir renvoyer les résultats lorsque vous effectuez une recherche dans le journal d’audit.  Même s’il vous faut attendre pour pouvoir consulter ce dernier, vous aurez toujours la possibilité de terminer d’autres tâches de ce labo.

1. Sélectionnez l’onglet de navigateur intitulé, **Accueil - Page de conformité Microsoft 365**.  Si vous l’avez déjà fermé, ouvrez Microsoft Edge et saisissez **compliance.microsoft.com**, puis connectez-vous avec vos informations d’identification d’administrateur.

1. Dans le volet de navigation à gauche, sélectionnez **Audit**.

1. Vérifiez que l’onglet **Recherche** est sélectionné (souligné).

1. Quand vous arrivez sur la page Audit, attendez 2 à 3 minutes.  Si Audit n’est PAS activé, vous verrez une barre bleue en haut de la page qui indique Commencer à enregistrer les activités des utilisateurs et des administrateurs.  Sélectionnez **Commencer à enregistrer les activités des utilisateurs et des administrateurs**.  Une fois que l’audit est activé, la barre bleue disparaît.  S’il n’y a pas de barre bleue, alors l’audit est déjà activé et aucune autre action n’est nécessaire.

1. Retournez à la page d’accueil du portail de conformité Microsoft Purview en sélectionnant **Accueil** dans le volet de navigation de gauche.

1. Conservez cet onglet ouvert pour l’utiliser lors de la prochaine tâche.

### <a name="task-3"></a>Tâche 3

Dans cette tâche, vous allez parcourir les paramètres associés à la solution de gestion des risques internes.  Ces paramètres s’appliquent à toutes les stratégies de gestion des risques internes, quel que soit le modèle à partir duquel elles ont été créées.

1. Vous devez vous trouver dans la page d’accueil du portail de conformité Microsoft Purview. Si ce n’est pas le cas, ouvrez l’onglet **Accueil - Conformité Microsoft 365**.

1. Dans le volet de navigation situé à gauche, sous Solutions, sélectionnez **Gestion des risques internes**.

1. Avant de commencer à élaborer une stratégie, vous devez configurer certains paramètres.  Sur la page de gestion des risques internes, accédez aux paramètres en sélectionnant l’**icône représentant un engrenage**, dans le coin supérieur droit.  
    1. Vérifiez que vous êtes dans l’onglet **Confidentialité** : pour les utilisateurs dont les activités correspondent à vos stratégies de risque lié aux menaces internes, ce paramètre détermine l’affichage ou non de leur véritable identité.  Sélectionnez **Ne pas montrer une version anonyme du nom d’utilisateur**, puis **Enregistrer**.

    1. Allez sur l’onglet **Indicateurs de la stratégie**. lorsque survient un événement qui déclenche la stratégie, un score de risque est calculé pour l’utilisateur en fonction des activités reliées aux indicateurs sélectionnés. Ces derniers sont inclus dans les modèles de stratégies de risque lié aux menaces internes.  Faites défiler la page pour afficher tous les indicateurs disponibles et les informations qui y sont associées. Sous **Indicateurs de bureau**, choisissez **Sélectionner tout**, puis **Enregistrer**.
    1. Allez sur l’onglet **Périodes de stratégie**. les périodes choisies prennent effet lorsque l’utilisateur déclenche une correspondance avec une stratégie de risque lié aux menaces internes.   La fenêtre d’activation détermine le délai pendant lequel les stratégies s’emploient à détecter l’activité des utilisateurs. Elle apparaît lorsqu’une action et une stratégie correspondent pour la première fois. La détection des activités passées indique à la stratégie jusqu’où remonter pour détecter l’activité de l’utilisateur. Elle apparaît lorsqu’une action et une stratégie correspondent pour la première fois.  Laissez les valeurs par défaut.  Sélectionnez l’onglet **Détections intelligentes**.
    1. Sélectionnez l’onglet **Détections intelligentes**. examinez les options présentes,  particulièrement les paramètres de domaines et leur relation aux indicateurs.
    1. Explorez les autres éléments répertoriés dans les paramètres et notez que nombre d’entre eux sont en préversion.

1. Pour revenir à la vue générale de la gestion des risques internes, sélectionnez **Gestion des risques internes** dans le coin supérieur gauche de la page, au-dessus de Paramètres.

1. Conservez cet onglet ouvert pour l’utiliser lors de la prochaine tâche.

### <a name="task-4"></a>Tâche 4

Cette tâche va vous guider dans le processus de création d’une stratégie.

1. Assurez-vous de vous trouver sur la page de gestion des risques internes.  Si ce n’est pas le cas, ouvrez l’onglet nommé **Gestion des risques internes - Conformité Microsoft 365**.

1. Sur la page générale de gestion des risques internes, sélectionnez l’onglet **Stratégies**, puis **+ Créer une stratégie**.  Configurez chaque onglet suivant.

    1. Modèle de stratégie :  dans la liste des catégories, sélectionnez **Fuites de données**, puis **Fuites de données générales**.  N’oubliez pas que les modèles des catégories peuvent comporter des prérequis supplémentaires.  Lisez les détails du modèle, puis sélectionnez **Suivant**.

    1. Nom et description : saisissez un nom, **SC900-InsiderRiskPolicy**, puis sélectionnez **Suivant**.
    1. Utilisateurs et groupes :  passez en revue les informations.  Conservez le paramètre par défaut, **Inclure tous les utilisateurs et groupes**.  Sélectionnez **Suivant**.
    1. Contenu à classer par ordre de priorité : lisez la description. Sélectionnez **Je veux indiquer des sites SharePoint, des étiquettes de confidentialité et/ou des types d’informations sensibles comme contenu prioritaire**, puis **Suivant**.
        1. Site SharePoint : pour cet exemple de stratégie, ne remplissez rien et sélectionnez **Suivant**.
        1. Types d’informations sensibles : pour cet exemple de stratégie, ne remplissez rien et sélectionnez **Suivant**.
        1. Étiquettes de confidentialité : sélectionnez **+ Ajouter ou modifier les étiquettes de confidentialité**.  Choisissez les étiquettes suivantes :  **Budget confidentiel** et **Hautement confidentiel\Projet - Falcon**, puis sélectionnez **Ajouter** et **Suivant**.
    1. Déclencheurs : vérifiez les informations détaillées.  La stratégie se déclenche quand l’utilisateur procède à une exfiltration définie (utilisez les icônes d’information pour en savoir plus sur chaque point mentionné) OU quand son activité correspond à une stratégie de protection contre la perte de données (DLP).  Cet exercice ne prévoyant pas de stratégie DLP, sélectionnez **L’utilisateur procède à une exfiltration**.  Vous constaterez que les indicateurs de stratégie activés lors de la tâche précédente sont cochés.   Souvenez-vous que ces indicateurs ne deviennent actifs que lorsque la stratégie se déclenche. Toutes les activités liées sont alors utilisées pour calculer un score de risque pour l’utilisateur. Sélectionnez **Suivant**.
    1. Seuils des indicateurs : c’est là que vous pouvez associer un seuil par défaut ou personnalisé aux indicateurs.  Souvenez-vous que ces derniers ne deviennent actifs qu’après l’événement déclencheur de stratégie. Les seuils n’ont donc aucune influence en la matière. Sélectionnez **Spécifier des seuils personnalisés**. Cette option vous permet de voir les valeurs par défaut actuelles. Conservez les valeurs par défaut, puis sélectionnez **Suivant**.  
    1. Indicateurs : Notez que tous les indicateurs de bureau que vous avez sélectionnés dans la tâche précédente sont sélectionnés.  Faites défiler la page pour voir les autres indicateurs de stratégie disponibles et d’autres éléments qui sont sélectionnés automatiquement.   La détection de séquence s’active.  Si une séquence d’activités est reconnue, il existe peut-être un risque supérieur.  Pointez votre souris sur l’icône d’informations pour obtenir des informations détaillées.  Ces éléments nécessitent certains indicateurs spécifiques, ainsi que des appareils intégrés.  Ce n’est le cas d’aucun appareil de ce locataire, alors pour des raisons de facilité, décochez **Sélectionner tout**.
    1. Terminer : vérifiez les paramètres avant de sélectionner **Envoyer** et **Terminé**.

1. Vous revenez alors à l’onglet Confidentialité de la page de gestion des risques internes.  La stratégie que vous venez de créer s’affiche,  

1. avec un champ « Utilisateurs concernés » qui représente les utilisateurs actuellement concernés par un score de risque.  Cela n’arrive que lorsque la stratégie est déclenchée, raison pour laquelle vous voyez une valeur de 0.  Un administrateur peut régler les paramètres de façon à ce que des scores de risque soient attribués à certaines personnes, selon l’activité détectée par la stratégie sélectionnée ET en priorité sur un événement déclencheur.  Pour ce faire, sélectionnez le cercle vide près du nom de la stratégie pour la choisir, puis sélectionnez **Commencer à noter l’activité des utilisateurs** au-dessus du tableau.  Une fois tous les champs remplis, sélectionnez **Commencer à noter l’activité**.  L’affichage des utilisateurs dans l’onglet correspondant peut prendre jusqu’à 24 heures. Passé ce délai, vous pouvez consulter les activités détectées de chacun dans cet onglet.  En bas de la fenêtre, sélectionnez **Fermer**.

1. Fermez tous les onglets ouverts du navigateur.

### <a name="review"></a>Révision

Ce labo vous a appris à paramétrer une stratégie de risque lié aux menaces internes, ainsi que les prérequis de base pour configurer et utiliser des stratégies de gestion des risques internes.
