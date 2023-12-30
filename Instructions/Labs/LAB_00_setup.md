<!---
---
Labo : Titre : « Installation »
---
--->

# Mise en place du labo

## Locataires WWL - Conditions d’utilisation
Si un locataire vous est fourni dans le cadre d’une formation dispensée par un instructeur, notez qu’il est mis à votre disposition dans le seul but de prendre en charge les labos pratiques de la formation.

Vous ne devez ni partager ni utiliser les locataires en dehors des labos pratiques. Le locataire utilisé dans ce cours est un locataire d’essai. Au terme de la classe, le locataire ne pourra pas faire l’objet d’une prolongation et vous ne pourrez plus l’utiliser ni y accéder.

Vous n’êtes pas autorisé à convertir un locataire en abonnement payant. Les locataires obtenus dans le cadre de ce cours sont la propriété de Microsoft Corporation. Nous nous réservons le droit d’y accéder et d’en reprendre possession à tout moment.

## Scénario du labo

Ce labo de configuration consiste à activer le journal d’audit Microsoft.

**Durée estimée** : 5 à 10 minutes

### Configuration - Activer le journal d’audit de Microsoft 365

Lors de cette tâche de configuration, vous allez activer la fonction de journal d’audit dans Microsoft 365.  Bien que la documentation indique que le journal d’audit est activé par défaut, la plupart des locataires de labo n’ont pas cette fonctionnalité activée. Il peut se passer plusieurs heures avant que l’activation ne prenne effet.  Il est conseillé d’activer cette fonctionnalité, car Microsoft 365 utilise les journaux d’audit pour les insights utilisateur, les activités identifiées dans les stratégies et les insights d’analyse.

1. Ouvrez Microsoft Edge. Dans la barre d’adresse, entrez **admin.microsoft.com**.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique communiqué par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Cliquez sur **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**. Vous accédez alors à la page du centre d’administration Microsoft 365.

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous Centres d’administration, sélectionnez **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.  

1. Dans le volet de navigation de gauche, sous Solutions, sélectionnez **Audit**.  Remarque : la fonctionnalité d’audit est également accessible via la page d’accueil de Microsoft 365 Defender (anciennement Centre de sécurité Microsoft 365).

1. Vérifiez que l’onglet **Nouvelle recherche** est sélectionné (souligné).

1. Lorsque vous arrivez sur la page Audit, attendez 2 à 3 minutes.  Si l’audit n’est PAS activé, vous voyez une barre bleue en haut de la page indiquant de commencer à enregistrer les activités des utilisateurs et des administrateurs.  Sélectionnez **Commencer à enregistrer les activités de l’utilisateur et de l’administrateur**.  Si vous êtes invité à confirmer la mise à jour des paramètres de l’organisation, sélectionnez **Oui**. Une fois l’audit activé, la barre bleue disparaît.  S’il n’y a pas de barre bleue, alors l’audit est déjà activé et aucune autre action n’est requise.  Un autre moyen de vérifier si l’audit est activé est via PowerShell, mais cette méthode n’est pas abordée dans ce cours.

1. Retournez à la page d’accueil du portail de conformité Microsoft Purview en sélectionnant **Accueil** dans le volet de navigation de gauche. Déconnectez-vous de Microsoft 365 en sélectionnant l’icône en haut à droite de la fenêtre Microsoft 365 qui représente un cercle avec les lettres MA à l’intérieur (à côté de l’icône de point d’interrogation), puis en sélectionnant **Se déconnecter**. Fermez le navigateur.

### Révision

Dans cette configuration, vous avez activé la fonction de journal d’audit dans Microsoft 365.
