# 🎖️ Tutoriel ARMA MOD FRANCE — Personnaliser le patch patronymique avec votre nom (WORK IN PROGRESS)

Bienvenue !  
Dans ce tutoriel, vous apprendrez à modifier le **patch patronymique** (disponible depuis la version 1.17 du mod AMF) pour y inscrire votre propre nom. Ce guide est accessible aux **débutants** comme aux **utilisateurs avancés**.

## ***"La majorité des utilisateurs n’utilisent que 20 à 30 % des fonctionnalités d’un logiciel."*** - Donald Norman

## ***Ne te laisse pas impressionner par la complexité d’un outil : dans 90 % des cas, tu n’utiliseras que 20 % de ses fonctions.***

Ne soyez pas effrayé des interfaces et des logiciels que l'on va utiliser dans ce tutoriel (comme les outils d'arma reforger), cette citation de Donald Norman est très très juste, même dans les tâches d'intégration de contenu jouable les plus complexes (comme les véhicules par exemple), pour le cas d'AMF, on n'utilise qu'une petite partie de Enfusion (du style 25%) pour faire 95% de ce qu'est AMF (qui représente les tenues, véhicules, armes, objets, scripts...).

---

## 🧰 Prérequis

- **GIMP** (gratuit) ou **Photoshop**  
  👉 [Télécharger GIMP 3.0.4](https://download.gimp.org/gimp/v3.0/windows/gimp-3.0.4-setup.exe)
  
- **Arma Reforger** sur **PC** (⚠️ obligatoire)

---

## 1️⃣ Télécharger le projet graphique

Rendez-vous sur cette page et téléchargez le fichier :  
**`AMF_ProjetPhotoshopPatchPatronymique.psd`**

➡️ Cliquez dessus puis sélectionnez **"Download Raw"** pour le récupérer.  
![Téléchargement du PSD](https://github.com/user-attachments/assets/045cbce8-c3f8-4556-a76f-721d6602d1aa)

---

## 2️⃣ Modifier le patch dans GIMP ou Photoshop

### ✏️ Ouvrir le projet

Faites un clic droit sur le fichier `.psd` téléchargé → **"Ouvrir avec"** → choisissez **GIMP** ou **Photoshop**.

---

### 🖼️ 2.1 Modifier le patch avec **Photoshop**

Ouvrez le fichier avec **Adobe Photoshop**.  
Une fois ouvert, vous verrez ce projet :  
![Interface Photoshop](https://github.com/user-attachments/assets/b24b7bfa-c477-4619-a718-799397dfb4f2)

#### 🧭 Repères en fonction des couleurs :

- 🔵 **Outil texte** : permet d’éditer le nom
- 🌸 **Zone de texte (rose)** : à modifier avec votre nom
- 🟨 **Fenêtre des calques** : contient texte, fond, effets réalistes (poussière, boue, etc.)
- 🟧 **Calque texte** : à personnaliser
- 🔴 **Icône "œil"** : active/désactive un calque

#### ✍️ Modifier le nom

- Sélectionnez l’**outil texte** puis cliquez sur le texte encadré en rose.
- Remplacez par votre nom, par exemple : `Lucas MOONLGHT → L. MOONLGHT`.

#### 🎨 Choisir un fond

Activez les camouflages en cliquant sur l’**icône œil** dans la fenêtre des calques.  
Vous pouvez créer plusieurs versions (un patch par camouflage).

#### 💾 Exporter

Allez dans **Fichier > Exportation > Exportation rapide en PNG**.  
Exportez l'image dans un **nouveau dossier** (ce sera la base de votre futur mod).

---

### 🎨 2.2 Modifier le patch avec **GIMP**

Ouvrez le projet avec **GIMP**.  
Si une boîte de dialogue s'affiche, choisissez **Colorimétrie relative**, puis **Convertir**.

![Erreur GIMP](https://github.com/user-attachments/assets/b9c0ce98-d7c4-4e0a-8edc-c4876afa32ca)

#### 🧭 Repères en fonction des couleurs :

- 🔵 **Outil texte** (entouré bleu ciel)
- 🌸 (zone rose) **Texte à modifier** 
- 🟨 **Calques** : texte, fond, VFX
- 🟧 **Calque texte**
- 🔴 **Icône œil** : activer/désactiver un calque

#### ✍️ Modifier le nom

- Cliquez sur le texte avec l'outil texte.
- Éditez avec votre nom (ex : `L. MOONLGHT`).
- Centrez le texte manuellement avec des **espaces** si besoin.
- Paramètres :
  - 🟩 **Police** : Arial Bold
  - 🟩 **Taille** : entre **85 et 90 px**

#### 🎨 Choisir un fond

Comme dans Photoshop, utilisez les **calques camouflage**. Activez/désactivez selon votre besoin.

#### 💾 Exporter

Allez dans **Fichier > Exporter sous** → choisissez le format **PNG**.

💡 **Nom de fichier recommandé** :  
`Patch_L.MOONLGHT_CE.png`  
(Pour un camouflage CE, par exemple)

---

## 3️⃣ Intégrer le patch dans un mod Arma Reforger

Une fois vos textures prêtes, il est temps de les intégrer dans un **mod ARMA Reforger** ! 

Petites explications avant de commencer: 
- Dans tout moteur de jeu récent, les objets, patchs, vêtements, armes, cailloux... sont représenté sous la forme de préfabriqué. Ce sont simplement des entité génériques qui peuvent être utilisé simplement, sans prise de tête par les moddeurs et les développeurs. Voyez ceci comme **la configuration** de votre patch patronymique (dans ce cas) mais voyez les préfabs comme l'entièreté de ce que vous voyez en jeu (du simple cailloux, au Mi-8 qui vous bombarde de roquettes qui sont également des préfabs !). Dans ces préfabs, il y a des **components**, traduis comportement en français. Ce sont simplement des scripts qui vont intervenir dans le préfab pour lui permettre d'avoir des fonctionnalités (comme la colision avec le component RigidBody, affichier le modèle 3D et la texture avec le MeshObject, le comportement d'un véhicule avec le SCR_WheeledSimulationComponent, ext...). Si vous avez compris ceci, vous êtes prêt pour faire votre patch.
- Il existe aussi des fichiers de configurations "simple", c'est tout simplement une liste d'options pour certains component (comme la liste des patchs à afficher dans la caisse des patchs par exemple). Elle permet de renseigner des options de base qui ne sont pas modifiables par l'utilisateur final, mais par les moddeurs et les développeurs.
- Dans les moteurs de jeu, il y a deux type de fichier pour gérer les textures, les matériaux (.emat) et les textures (.png, .edds, .edd...). La différence est que le matériau sert a répertorier les textures (.edds, .dds) par type pour pouvoir les appliquer sur un modèle 3D (ex: un patch patronymique en 3D).
- Quand l'on va mettre nos textures dans Enfusion, le moteur va les importer (comme tous fichiers). Il va les convertir dans quelque chose qui est optimisé pour les jeux vidéos ainsi qu'un format qui comprend réellement (Exemple: .png -> .edds, .fbx -> .xob). Cela ce fait automatiquement, et il ne faut pas supprimer les fichiers que vous avez mit dans le moteur ! Ces fichiers qui ont été importé seront supprimé dans la version qui sera envoyé sur le Workshop par le moteur lui même. Vous ne devez pas supprimer de vous même les fichiers que vous avez mis dans votre mod ⚠️

### 🧩 Objectif :

Créer une **variante personnalisée** du patch patronymique officiel avec un mod personnalisé ! 

#### ✍️ Créer le mod pour réaliser le(s) patch(s)
Ouvrez les outils de Arma Reforger, puis faite **add project > Add existing project**

![image](https://github.com/user-attachments/assets/ed5e5bf2-9032-4128-9929-ee5301b906c9)

Ensuite, allez dans le dossier où sont placés vos mods Arma Reforger (Souvent C:\Users\{VotreNomD'utilisateur}\Documents\My Games\ArmaReforger\addons), puis ouvrez le dossier nommé AMF_FANTASSIN_64CF25A41DCBDBE0 puis sélectionnez le seul fichier à l'intérieur

![image](https://github.com/user-attachments/assets/3a69d02b-0d6d-404a-bb44-78474f33853e)

Une fois cela fait, on va créer votre 1er mod (ou pas), faite **add project > Create a new project**

![image](https://github.com/user-attachments/assets/6c63a084-5cab-47e7-8ebd-f9469f83d687)

- Nommez votre mod sans espaces ni caractères spéciaux 
- choisiez potentiellement l'emplacement de votre mod sur votre PC
- Sélectionnez en dépendance AMF_FANTASSIN

Puis faite Create !

![image](https://github.com/user-attachments/assets/057f8220-29cd-4109-b5a0-bed3c36137b5)

#### 🧩 Créer la hiérarchie de dossier pour pouvoir faire les patchs proprement

Dans les mods Arma Reforger, vous n'êtes pas obligé de faire une hiérarchie de dossier, vous pouvez très bien tout mélanger ! Cependant, je vous souhaite bon courage pour vous y retrouver ! 
# N’importe qui peut écrire du code que la machine comprend. Un bon développeur écrit du code que les humains comprennent. - Martin Fowler

Pour ce faire, vous pouvez créer la hiérarchie suivante:

-Assets > Items > Patchs > Patronymiques

-Configs > EntityCatalog > FR

-Prefabs > Items > Patchs > Patronymiques

En finalité, ça devrait ressembler à ça ✅

![image](https://github.com/user-attachments/assets/dcc43505-e4a3-4804-b6d3-5fda0bdbd180)

Une fois tout cela fait, vous n'avez plus qu'a vous rendre dans le mod AMF_FANTASSIN et à aller chercher le préfabriqué du patch Patronymique de base, proposé par AMF.

Pour ce faire, rendez vous dans AMF_FANTASSIN > Prefabs > Items > Patchs > Patronymiques puis faite clique droit sur le fichier "Patch_Patronymique_Base" qui faites "Inherit to {LeNomDeVotreMod}" 

## ATTENTION ⚠️: Ne pas faire "Override to {LeNomDeVotreMod}" sinon la configuration du patch de base sera remplacé par la votre et risque de causer des problèmes par la suite 

**🚧 Work In Progress 🚧**

---

## 📌 Conseils supplémentaires **🚧 Work In Progress 🚧**

- Créez une **version par camouflage** pour plus de réalisme.
- Respectez le **format militaire** des noms (`L. NOMDEFAMILLE`).
- Conservez une **structure de dossier claire** pour vos textures.

---

## ✅ Résultat **🚧 Work In Progress 🚧**

Une fois votre mod finalisé, vous pourrez voir votre **patch personnalisé** directement sur vos unités en jeu avec le mod **AMF** !

---

Si vous avez des questions, n’hésitez pas à ouvrir une issue ou à passer sur le [Discord d’AMF](https://discord.gg/eycKqCKtWX) dans [le fil](https://discord.com/channels/507939466959257610/1390817279842979860).

---

© 2025 — *Arma Mod France*
