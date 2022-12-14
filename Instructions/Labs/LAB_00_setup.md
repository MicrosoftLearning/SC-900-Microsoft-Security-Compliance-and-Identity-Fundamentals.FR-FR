<a name="---"></a><!---
---
Labo : Titre : « Installation »
---
--->

# <a name="lab-setup"></a>Labo : Installation

## <a name="lab-scenario"></a>Scénario du labo

Ce labo de configuration consiste à activer le journal d’audit Microsoft.

**Durée estimée** : 5-10 minutes

### <a name="setup---enable-microsoft-365-audit-log"></a>Configuration - Activer le journal d’audit de Microsoft 365

Lors de cette tâche de configuration, vous activerez la fonction de journal d’audit dans Microsoft 365.  Bien que la documentation indique que le journal d’audit est activé par défaut, la plupart des locataires de labo n’ont pas cette fonctionnalité activée. Il peut se passer plusieurs heures avant que l’activation ne prenne effet.  Il est utile d’activer cette fonctionnalité, car Microsoft 365 utilise les journaux d’audit pour les informations concernant les utilisateurs, les activités identifiées dans les stratégies et les informations concernant les analyses.

1. Ouvrez Microsoft Edge. Dans la barre d’adresse, entrez **admin.microsoft.com**.

1. Connectez-vous avec vos informations d’identification d’administrateur.
    1. Dans la fenêtre de connexion, entrez **admin@WWLxZZZZZZ.onmicrosoft.com** (où ZZZZZZ représente votre ID de locataire unique communiqué par votre fournisseur d’hébergement de labo), puis sélectionnez **Suivant**.
    1. Entrez le mot de passe d’administrateur qui vous a été communiqué par votre fournisseur d’hébergement de labo. Sélectionnez **Connexion**.
    1. Lorsque vous êtes invité à rester connecté, sélectionnez **Oui**. Vous accédez ainsi à la page du Centre d’administration Microsoft 365.

1. Sélectionnez **Tout afficher** dans le volet de navigation gauche du centre d’administration Microsoft 365.

1. Sous les Centres d’administration, sélectionnez **Conformité**.  Le navigateur ouvre une nouvelle page. Il s’agit de la page d’accueil du portail de conformité Microsoft Purview.  

1. Dans le volet de navigation à gauche, sélectionnez **Audit**.  Remarque : la fonctionnalité d’audit est également accessible depuis la page d’accueil de Microsoft 365 Defender (précédemment dénommé Centre de sécurité Microsoft 365).

1. Vérifiez que l’onglet **Nouvelle recherche** est sélectionné (souligné).

1. Quand vous arrivez sur la page Audit, attendez 2 à 3 minutes.  Si Audit n’est PAS activé, vous verrez une barre bleue en haut de la page qui indique Commencer à enregistrer les activités des utilisateurs et des administrateurs.  Sélectionnez **Commencer à enregistrer les activités des utilisateurs et des administrateurs**.  Si vous êtes invité à confirmer la mise à jour des paramètres de l’organisation, sélectionnez **Oui**. Une fois que l’audit est activé, la barre bleue disparaît.  S’il n’y a pas de barre bleue, alors l’audit est déjà activé et aucune autre action n’est requise.  Vous pouvez également vérifier si l’audit est activé en passant par PowerShell, mais cela n’entre pas dans le cadre de ce cours.

1. Retournez à la page d’accueil du portail de conformité Microsoft Purview en sélectionnant **Accueil** dans le volet de navigation de gauche. Déconnectez-vous de Microsoft 365 en sélectionnant l’icône en haut à droite de la fenêtre Microsoft 365 qui représente un cercle avec les lettres MA à l’intérieur (à côté de l’icône de point d’interrogation), puis en sélectionnant **Se déconnecter**. Fermez le navigateur.

### <a name="review"></a>Révision

Dans cette configuration, vous avez activé la fonction de journal d’audit dans Microsoft 365.
