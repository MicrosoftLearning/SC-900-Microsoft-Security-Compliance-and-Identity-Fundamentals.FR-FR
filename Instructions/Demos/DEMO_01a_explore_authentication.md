<!---
---
Démonstration : Titre : « Explorer les paramètres des utilisateurs Microsoft Entra ID » Parcours d’apprentissage/Module/Unité : « Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra ; Module 2 : Décrire les capacités d’authentification de Microsoft Entra ID ; Unité 3 : Décrire les méthode d'authentification et Unité 4 : Décrire l’authentification multifacteur »
---
--->

# Démonstration : méthodes d’authentification et MFA

Cette démonstration correspond au contenu Learn suivant :

- Parcours d’apprentissage : Décrire les fonctionnalités de Microsoft Entra.
- Module : décrire les fonctionnalités d’authentification de Microsoft Entra ID.
- Unités : décrire les méthodes d'authentification et décrire l'authentification multifacteur.

## Scénario de démonstration

Dans cette démonstration, vous explorerez les différents paramètres disponibles pour l'authentification dans Microsoft Entra.

1. Revenez à l’onglet ouvert du navigateur intitulé « Centre d’administration accueil Microsoft Entra ».  Si vous avez précédemment fermé cet onglet de navigateur, ouvrez Microsoft Edge et connectez-vous à **[entra.microsoft.com](https://entra.microsoft.com)** avec vos informations d’identification d’administrateur Microsoft 365.

1. Dans le volet de navigation gauche, développez **Protection**, puis sélectionnez **Méthodes d'authentification**.

1. La sélection des méthodes d'authentification permet d'afficher la page des stratégies.  Vous verrez ici les méthodes d'authentification disponibles et si elles sont activées.  Nous allons passer en revue quelques-unes de ces méthodes :.  
    1. Sélectionnez **SMS**.  Lisez la description en haut de la page : « Cette méthode d’authentification remet un code unique via SMS au téléphone d’un utilisateur, puis celui-ci entre ce code pour se connecter. Le SMS est utilisable pour l’authentification multifacteur et la réinitialisation de mot de passe en libre-service. Il peut également être configuré pour être utilisé comme premier facteur ».
        1. Il convient de souligner que certaines méthodes d'authentification peuvent être utilisées pour la MFA et/ou la réinitialisation de mot de passe en libre-service.  Certaines ne peuvent être utilisées que comme forme primaire d'authentification, tandis que d'autres ne peuvent être utilisés que comme forme secondaire d'authentification.
        1. Pour configurer une méthode d'authentification particulière, vous devez l'activer, puis cibler les utilisateurs et/ou les groupes à inclure.  Vous pouvez également sélectionner les groupes à exclure.
        1. Ne modifiez pas les paramètres.  Fermez la page des paramètres SMS en sélectionnant le **X** en haut à droite de la page.  
    1. Jetons un coup d’œil aux paramètres des appels vocaux.  Sélectionnez **Appel vocal**, la description, vous fait apparaître une différence importante.  Les appels vocaux ne sont pas utilisables en tant que méthode d’authentification de premier facteur.
    1. Sélectionnez maintenant **Microsoft Authenticator**.  Il s’agit des méthodes d’authentification phares.  
        1. C’est ici que vous activez les fonctionnalités et que vous ciblez les personnes à inclure.  Vous pouvez le faire pour tous les utilisateurs ou groupes. Une fois que vous avez identifié les utilisateurs ou groupes à inclure, vous pouvez identifier des groupes spécifiques à exclure.  
        1. Sous l’onglet **Configurer**, vous pouvez sélectionner si une fonctionnalité spécifique est gérée par Microsoft. Ce paramètre est un moyen pratique pour une organisation d’autoriser Microsoft à activer ou à désactiver une fonctionnalité par défaut. Cela peut aider une organisation à améliorer sa position en matière de sécurité.
        1. Ne modifiez pas les paramètres. Fermez la page en cliquant sur le **X** en haut à droite de la page.
 
1. Examinons maintenant la protection par mot de passe. Sélectionnez **Protection par mot de passe**.  Notez les différents paramètres de configuration disponibles.  
    1. Sélectionnez l’icône d’informations à côté du **seuil de verrouillage** pour voir la signification de ce paramètre.  Actuellement, cette valeur est fixée à 10, ce qui signifie qu'il peut y avoir jusqu'à 10 échecs de connexion avant que le compte ne soit bloqué. Cette valeur semble un peu élevée, vous pouvez donc la modifier.
    1. Sélectionnez l'icône d'information pour chacun des différents paramètres et parlez-y brièvement.  Vous voudrez surtout appeler la liste des mots de passe interdits personnalisés.

1. Les forces d’authentification sont des contrôles d’accès conditionnels qui permettent aux administrateurs de spécifier quelle combinaison de méthodes d’authentification peut être utilisée pour accéder à une ressource. Vous verrez cela dans Accès conditionnel.

1. Dans le volet de navigation de gauche des méthodes d’authentification, sélectionnez **Activité**.
    1. L’**inscription** est soulignée en bleu.  Vous pouvez ici afficher l'activité d'inscription pour différentes méthodes d'authentification.
    1. Sélectionnez **Utilisation** pour afficher les détails de l’utilisation et notez que vous pouvez ajouter différents filtres.

1. Dans ce module, vous avez également parlé de l'authentification multifacteur. Vous en saurez plus sur la MFA dans la démonstration sur l'accès conditionnel, mais vous pouvez prendre une minute pour montrer quelques paramètres de base.  Dans le volet de navigation du centre d’administration Microsoft Entra, sélectionnez **Authentification multifacteur**.  Vous devrez peut-être sélectionner **Afficher plus** sous la section Protection, dans le volet de navigation gauche.
    1. Sur la page **Démarrage**, il est indiqué que la meilleure façon de l'appliquer aux utilisateurs est l'accès conditionnel, mais il y a des paramètres spécifiques à configurer ici.
    1. Sélectionnez **Verrouillage de compte** et appelez les paramètres de verrouillage configurables.
    1. Sélectionnez **Bloquer/débloquer des utilisateurs**, en précisant que c'est ici qu'un administrateur peut bloquer ou débloquer manuellement des utilisateurs.  Notez qu'un utilisateur bloqué restera bloqué pendant 90 jours à moins d'être débloqué manuellement.
    1. Sélectionnez **Alerte de fraude**.  Cela permet aux administrateurs d’autoriser les utilisateurs à signaler une fraude s'ils reçoivent une demande de vérification en deux étapes qui ne vient pas d'eux.
    1. Sélectionnez **Notifications**.  Vous pouvez configurer Microsoft Entra pour envoyer des notifications par e-mail quand les utilisateurs signalent des alertes de fraude. Ces notifications sont généralement envoyées aux administrateurs d’identité, car les informations d’identification du compte de l’utilisateur sont susceptibles d’être compromises.
    1. Fermez la page en cliquant sur le **X** en haut à droite de la fenêtre.  Répétez ensuite cette étape pour revenir au centre d'administration Microsoft Entra.

1. Gardez l'onglet du navigateur ouvert car vous retournerez au centre d'administration Microsoft Entra pour la prochaine démonstration.

### Révision

Dans cette démonstration, vous avez montré les méthodes d'authentification disponibles dans Microsoft Entra.  Vous montrez également quelques-uns des paramètres configurables associés à l'authentification multifacteur.
