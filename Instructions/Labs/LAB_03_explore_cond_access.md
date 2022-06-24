---
lab:
  title: Explorer la gestion des accès dans Azure AD avec l’accès conditionnel
  module: 'Module 2 Lesson 3: Describe the capabilities of Microsoft Identity and access management solutions: Explore the access management capabilities of Azure AD'
ms.openlocfilehash: c8e9f8eb6e0d3609adc7ed5ea7f4d18ebfa33c4b
ms.sourcegitcommit: 57e11f5a455d10c8ae3c95bb8a9487b10af3d315
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2022
ms.locfileid: "146542601"
---
# <a name="lab-explore-access-management-in-azure-ad-with-conditional"></a>Labo : Découvrir la gestion de l’accès conditionnel dans Azure AD

## <a name="lab-scenario"></a>Scénario du labo

Dans ce labo, vous découvrirez l’authentification multifacteur (MFA) à accès conditionnel du point de vue d’un administrateur et d’un utilisateur.  En tant qu’administrateur, vous allez créer une stratégie exigeant que les utilisateurs passent par une authentification multifacteur lorsqu’ils accèdent à une application de gestion Microsoft Azure basée sur le cloud.  Du point de vue de l’utilisateur, vous verrez l’impact de la stratégie d’accès conditionnel, y compris le processus d’inscription MFA.

**Durée estimée** : 10-15 minutes

### <a name="task-1"></a>Tâche 1

Dans cette tâche, en tant qu’administrateur, vous réinitialiserez le mot de passe de l’utilisateur Charline Berger.  Cette étape est nécessaire pour pouvoir se connecter initialement en tant qu’utilisateur dans les tâches ultérieures.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse, saisissez **portal.azure.com**.

2. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Saisissez le mot de passe d’administrateur communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

3. Dans le coin supérieur gauche de l’écran, à côté de là où Microsoft Azure est indiqué, sélectionnez l’icône de menu Afficher le portail (les trois lignes horizontales également appelées « icône hamburger ») puis, dans le volet de navigation gauche, sous Favoris, sélectionnez Azure Active Directory. S’il n’est pas répertorié sous Favoris, dans la zone de recherche, entrez Azure Active Directory, puis dans la liste des résultats, sélectionnez **Azure Active Directory**.

4. Dans le volet de navigation de gauche, sélectionnez **Utilisateurs**.

5. Sélectionnez **Charline Berger** dans la liste des utilisateurs.

6. Sélectionnez **Réinitialiser le mot de passe**  en haut de la page. Comme vous ne vous êtes jamais connecté en tant que Charline Berger, vous ne connaissez pas son mot de passe et devrez le réinitialiser.

7. À l’ouverture de la fenêtre de réinitialisation du mot de passe, sélectionnez **Réinitialiser le mot de passe**.  IMPORTANT : notez le nouveau mot de passe. Vous en aurez besoin pour vous connecter en tant qu’utilisateur lors d’une tâche ultérieure.

8. Fermez la fenêtre de réinitialisation du mot de passe en sélectionnant le **X** dans le coin supérieur droit de la page.

9. Fermez la fenêtre Utilisateurs en sélectionnant le **X** dans le coin supérieur droit de la page.

10. Gardez cette fenêtre ouverte.

### <a name="task-2"></a>Tâche 2

Dans cette tâche, vous allez suivre le processus de création d’une stratégie d’accès conditionnel dans Azure AD.

1. Ouvrez l’onglet du navigateur intitulé Contoso - Microsoft Azure.   Si vous avez fermé l’onglet du navigateur, ouvrez Microsoft Edge. Dans la barre d’adresse, saisissez portal.azure.com, connectez-vous avec vos informations d’identification d’administrateur, puis sélectionnez Azure Active Directory.  

2. Dans le volet de navigation gauche, sélectionnez **Sécurité**.

3. Dans le volet de navigation gauche, sélectionnez **Accès conditionnel**.

4. L’écran des stratégies d’accès conditionnel s’affiche. Toutes les stratégies d’accès conditionnel sont répertoriées ici. Sélectionnez **Nnouvelle stratégie**.

5. Dans le champ Nom, saisissez **Stratégie de test MFA**.

6. Sous Utilisateurs et groupes, sélectionnez **0 utilisateurs et groupes sélectionnés**.

7. L’option d’inclure ou d’exclure des utilisateurs ou des groupes apparaît.  Assurez-vous que l’option **Inclure** est sélectionnée (soulignée).

8. Sélectionnez l’option pour **Sélectionner des utilisateurs et des groupes** et sélectionnez **Utilisateurs et groupes**.  La fenêtre Sélectionner des utilisateurs et des groupes s’ouvre.  

9. Dans la barre de recherche, saisissez **Charline**.  Sélectionnez **Charline Berger** sous la barre de recherche, puis appuyez sur le bouton **Sélectionner** au bas de la page.  Remarque : attribuer la stratégie aux utilisateurs d’un groupe est une pratique courante.  Dans ce labo, nous allons attribuer la stratégie à un utilisateur spécifique afin de gagner du temps.

10. Sous Applications ou actions cloud, sélectionnez **Aucune application ou action cloud sélectionnée**.

11. Vous pourrez alors choisir d’inclure ou d’exclure des applications cloud ou des actions utilisateur.  Assurez-vous que les **Applications cloud** sont mises en surbrillance et que l’option **Inclure** est sélectionnée (soulignée), puis sélectionnez **Sélectionner des applications**.  La fenêtre Sélectionner des applications cloud s’ouvre.

12. Dans la barre de recherche, saisissez **Azure**.  Dans les résultats de la recherche qui apparaissent sous la zone de recherche, sélectionnez **Gestion Microsoft Azure**, puis appuyez sur **Sélectionner** au bas de la page.  Notez l’avertissement.  

13. Sous Conditions, sélectionnez **0 conditions sélectionnées**.  Notez les différentes options que vous pouvez configurer.  La stratégie vous permet de contrôler l’accès utilisateur en fonction de signaux provenant de conditions telles que le risque, la plateforme de l’appareil, l’emplacement, les applications clientes ou l’état de l’appareil.  Par exemple, vous pouvez inclure une condition pour que la stratégie soit appliquée à n’importe quel emplacement, à l’exception des emplacements sélectionnés ou approuvés, comme le réseau de votre siège social.  Ne définissez aucune condition pour cette stratégie.

14. Vous allez maintenant définir les contrôles d’accès.  Sous Accorder, sélectionnez **0 contrôles sélectionnés**.

15. La fenêtre Accorder s’ouvre.  Assurez-vous que l’option **Accorder l’accès** est sélectionnée, puis sélectionnez **Exiger une authentification multifacteur**.  Sous la section Pour plusieurs contrôles, conservez le paramètre par défaut **Demander tous les contrôles sélectionnés**.  Appuyez sur **Sélectionner** en bas de la page.

16. Au bas de la page, sous Activer la stratégie, sélectionnez **Activé**, puis appuyez sur le **bouton Créer**.

17. Au bout de quelques secondes, la stratégie MFA pilote devrait apparaître dans la liste des stratégies d’accès conditionnel (si nécessaire, sélectionnez **Actualiser** en haut de la page).

18. Déconnectez-vous d’Azure et fermez la fenêtre du navigateur.

### <a name="task-3"></a>Tâche 3

Dans cette tâche, vous verrez l’impact de la stratégie d’accès conditionnel du point de vue de l’utilisateur, Charline Berger. Vous commencerez par vous connecter à une application qui n’est pas incluse dans la stratégie d’accès conditionnel.  Ensuite, vous répéterez le processus pour une application qui est incluse dans la stratégie d’accès conditionnel.  Rappelez-vous que la stratégie exige que l’utilisateur passe par une MFA lorsqu’il accède à une application de gestion Microsoft Azure.  Pour utiliser une MFA, l’utilisateur doit d’abord enregistrer la méthode d’authentification qui sera utilisée comme MFA, par exemple un code envoyé à un appareil mobile ou une application d’authentification.

1. Ouvrez Microsoft Edge.  Dans la barre d’adresse du navigateur, entrez **login.microsoftonline.com/** .

1. Connectez-vous en tant que Charline Berger.
    1. Dans la fenêtre de connexion, entrez **DebraB@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Saisissez le mot de passe que vous avez noté lors de la tâche précédente. Sélectionnez **Connexion**.
    1. Le mot de passe fourni lorsque vous avez réinitialisé le mot de passe, en tant qu’administrateur, étant temporaire, vous devez mettre à jour votre mot de passe (cela ne fait pas partie de la MFA).  Saisissez le mot de passe actuel. Ensuite, pour les champs du nouveau mot de passe et de confirmation du mot de passe, saisissez **SC900-Lab**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**.

1. Vous devriez être connecté à votre compte Microsoft 365.  Aucune MFA n’était nécessaire pour cette application, car elle ne fait pas partie de la stratégie.

1. Vous allez maintenant tenter de vous connecter à une application qui répond aux critères d’une MFA.  Ouvrez Microsoft Edge et dans la barre d’adresse, entrez **portal.azure.com**.

1. Une fenêtre indiquant que des informations supplémentaires sont nécessaires s’affiche.  Sélectionnez **Suivant**.  Notez que cela va lancer le processus d’inscription MFA, car vous accédez pour la première fois à l’application cloud qui a été identifiée dans la stratégie d’accès conditionnel.  Ce processus d’inscription ne doit être effectué qu’une seule fois.   L’administrateur peut configurer la méthode d’authentification à utiliser pour éviter que l’utilisateur ne doive suivre le processus d’inscription.

1. Dans la fenêtre Sécuriser votre compte, vous pouvez sélectionner la méthode à utiliser comme MFA.  Vous pouvez utiliser Microsoft Authenticator. Dans cet exercice de labo, vous choisirez une autre méthode afin de gagner du temps.  Sélectionnez **Je veux configurer une autre méthode**.  Dans la fenêtre contextuelle Choisir une autre méthode, sélectionnez la **flèche déroulante vers le bas**, **Téléphone**, puis **Confirmer**.

1. Assurez-vous que votre pays est sélectionné dans la fenêtre qui s’ouvre, puis saisissez le numéro de téléphone mobile que vous souhaitez utiliser et sélectionnez-le. Assurez-vous que l’option **Envoyez-moi un code par SMS** est sélectionnée, puis appuyez sur **Suivant**.  L’écran affiche « SMS vérifié. Votre téléphone a été enregistré avec succès. »  Sélectionnez **Suivant**. Ensuite, sélectionnez **Done** (Terminé).  Le processus d’inscription unique est terminé.

1. Il se peut que vous recevez un message indiquant que votre connexion a expiré.  Il suffit alors de saisir le mot de passe **SC900-Lab** et de sélectionner **Se connecter**.

1. Une fenêtre s’affiche et vous invite à saisir le code qui a été envoyé à votre téléphone.  Saisissez le code et sélectionnez **Suivant**.  Il s’agit du processus auquel vous, comme Gilbert, serez confronté chaque fois que vous accéderez à une application cloud de gestion Microsoft Azure, telle que le portail Azure, conformément à la stratégie MFA.

1. Une fenêtre s’affiche et vous invite à saisir le code qui a été envoyé à votre téléphone.  Saisissez le code et appuyez sur le bouton **Vérifier**.  Lorsque vous êtes invité à rester connecté, sélectionnez **Non**.

1. Vous devez maintenant être en mesure d’accéder au portail Azure.  Le portail Azure est une application de gestion Microsoft Azure et nécessite donc une authentification multifacteur, conformément à la stratégie d’accès conditionnel qui a été créée.  

1. Déconnectez-vous en cliquant sur l’icône d’utilisateur à côté de l’adresse e-mail, dans le coin supérieur droit de l’écran, et en sélectionnant Se déconnecter. Ensuite, fermez toutes les fenêtres de navigation.

### <a name="review"></a>Révision

Dans ce labo, vous avez suivi le processus de configuration d’une stratégie d’accès conditionnel, qui exige que les utilisateurs passent par une MFA lorsqu’ils accèdent à l’application cloud de gestion Microsoft Azure.  Ensuite, en tant qu’utilisateur, vous avez suivi le processus d’inscription MFA et vu l’impact de la stratégie d’accès conditionnel exigeant l’utilisation d’une MFA pour accéder au portail Azure.
