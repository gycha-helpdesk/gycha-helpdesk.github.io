<!--
Author:		    Mussa AL Hussein
Date:		    10.04.2024
Description:    marche a suivre pour reinstaller les profiles de JAMF
-->

# Réinitialisation de l'Authentification Multi-Facteurs (MFA)

Procédure de Réinitialisation de l'Authentification Multi-Facteurs (MFA)  
et utilisation de la Méthode TAP dans Microsoft Entra ID (Azure AD)

**Objectif** **:**

Cette procédure décrit les étapes que doit suivre un administrateur pour  
réinitialiser l'authentification multi-facteurs (MFA) et configurer la  
méthode TAP (Temporary Access Pass) lorsqu'un utilisateur a oublié son  
moyen d'authentification (par exemple, son téléphone).

**Important** **:** La méthode TAP ne doit être utilisée qu'en cas  
d'oubli temporaire ou de perte du téléphone et ne constitue pas une  
méthode d'authentification standard ou régulière.

---

**1.** **Prérequis** **:**

> • Accès au **portail** **Entra** **ID** avec un compte disposant du  
> rôle **Authentication** **Administrator** .  
>  
> • Vérification préalable que l'oubli du téléphone est bien la cause de  
> la demande.

---

**2.** **Accéder** **au** **Portail** **Azure** **AD** **:**

> 1. Connectez-vous au portail Azure via l'URL :  [<u>https://entra.microsoft.com/</u>](https://entra.microsoft.com/)  
>
> 2. Utilisez vos identifiants « a-xxxxxxx » pour vous authentifier.  
>
> 3. Dans le menu de navigation de gauche, sélectionnez **Identité**.

---

**3.** **Identification** **de** **l'Utilisateur** **:**

> 1. Allez dans **Utilisateurs** > **Tous les utilisateurs**.  
>
> 2. Recherchez l'utilisateur en question en utilisant son nom ou son identifiant.  

```{image} images/UtileMFA01.png
:width: 1000px  
:name: MFA
:align: center  
```

> 3. Cliquez sur le profil de l'utilisateur pour accéder aux détails.

---

**4.** **Réinitialisation** **de** **l'Authentification** **MFA** **:**

> 1. Dans la fiche utilisateur, allez dans la section **Méthodes**  
> **d’authentification**.  
>
> 2. Cliquez sur l'option **Exiger** **une réinscription** **de**  
> **l’authentification multifacteur**  
```{image} images/uw4l00h5.png
:name: MFA
:align: center  
```
> 3. Confirmez l'action en cliquant sur **OK**.

Cette étape force l'utilisateur à réenregistrer ses informations MFA  
lors de sa prochaine connexion.

---

**5.** **Utilisation** **de** **la** **Méthode** **TAP** **(uniquement** **en** **cas** **d'oubli** **du** **téléphone)** **:**

> 1. Retournez à l'interface **Méthodes d’authentification**.  
>
> 2. Cliquez sur « **Ajouter une méthode d’authentification** » et sélectionnez **Droits d’accès temporaire (TAP)** dans la liste des méthodes.  
>
>   - **Durée** : Définir une période limitée conformément aux politiques  
>     de sécurité. Max 1 jour (1440 minutes)  
>
>   - **Utilisation ponctuelle** : au choix selon le contexte.  
```{image} images/ep4nke2n.png
:name: MFA
:align: center  
```
> 3. Cliquez sur **Ajouter** pour enregistrer la nouvelle configuration.  
>
> 4. Transmettez le **nouveau TAP** de manière sécurisée à l'utilisateur  
> en précisant qu'il doit être utilisé uniquement pour la réinitialisation  
> temporaire en cas d'oubli de l'appareil MFA.

---

**6.** **Vérification** **de** **l'Accès** **:**

> 1. Demandez à l'utilisateur de se connecter pour vérifier le bon  
> fonctionnement du processus MFA réinitialisé.  
>
> 2. Vérifiez dans le portail Entra que l'utilisateur a correctement  
> réenregistré son authentification MFA.  
>
> 3. Une fois l'accès restauré, supprimez le TAP si celui-ci n'est plus  
> nécessaire.
```{image} images/glc42ffw.png
:name: MFA
:align: center  
```
