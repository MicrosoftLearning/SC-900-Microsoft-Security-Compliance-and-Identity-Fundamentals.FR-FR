---
demo:
  title: 'Configuration de la démonstration'
  module: 'Configuration de la démonstration'
---


## <a name="pre-demo-setup"></a>Configuration avant la démonstration

Cette configuration consiste à activer le journal d’audit Microsoft.

### <a name="setup---enable-microsoft-365-audit-log"></a>Configuration - Activer le journal d’audit de Microsoft 365

Lors de cette tâche de configuration, vous allez activer la fonction de journal d’audit dans Microsoft 365.  Bien que la documentation indique que le journal d’audit est activé par défaut, la plupart des locataires de labo n’ont pas cette fonctionnalité activée. Il peut se passer plusieurs heures avant que l’activation ne prenne effet.  Il est conseillé d’activer cette fonctionnalité, car Microsoft 365 utilise les journaux d’audit pour les insights utilisateur, les activités identifiées dans les stratégies et les insights d’analyse.

1. Ouvrez Microsoft Edge. Dans la barre d’adresse, entrez **admin.microsoft.com**.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique fourni par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**. Vous accédez ainsi à la page du Centre d’administration Microsoft 365.

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous les Centres d’administration, sélectionnez **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.  

1. Dans le volet de navigation situé à gauche du portail de conformité Microsoft Purview, sélectionnez **Tout afficher**.

1. Dans le volet de navigation à gauche, sélectionnez **Audit**.  Remarque : la fonctionnalité d’audit est également accessible depuis la page d’accueil de Microsoft 365 Defender.

1. Vérifiez que l’onglet **Recherche** est sélectionné (souligné).

1. Quand vous arrivez sur la page Audit, attendez 2 à 3 minutes.  Si l’audit n’est PAS activé, vous verrez une barre bleue en haut de la page qui indique de commencer à enregistrer les activités des utilisateurs et des administrateurs.  Sélectionnez **Commencer à enregistrer les activités des utilisateurs et des administrateurs**.  Une fois que l’audit est activé, la barre bleue disparaît.  S’il n’y a pas de barre bleue, alors l’audit est déjà activé et aucune autre action n’est requise.

1. Retournez à la page d’accueil du portail de conformité Microsoft Purview en sélectionnant **Accueil** dans le volet de navigation de gauche.

### <a name="review"></a>Révision

Dans cette configuration, vous avez activé la fonction de journal d’audit dans Microsoft 365.
