# Introduction

## MAXIME ROLLAND

### LINUX

---

## Système d'exploitation

Un système d'exploitation est un logiciel qui agit comme une interface entre l'utilisateur final et le matériel informatique. Il gère les ressources matérielles et logicielles et fournit des services pour les programmes informatiques.

### Exemples concrets de systèmes d'exploitation

- **Windows** : Utilisé principalement dans les environnements domestiques et professionnels.
- **macOS** : Système d'exploitation pour les ordinateurs Apple.
- **Linux** : Répandu dans les serveurs, supercalculateurs et appareils embarqués.
- **Android** : Basé sur Linux, utilisé sur la majorité des smartphones.
- **iOS** : Système d'exploitation d'Apple pour les appareils mobiles.

### Composants clés

- **Applications** : Programmes utilisés par l'utilisateur pour effectuer des tâches spécifiques.
- **Pilotes** : Logiciels qui permettent au système d'exploitation de communiquer avec le matériel.
- **Matériel** : Les composants physiques d'un ordinateur.

---

## Structure d'un système d'exploitation

Un système d'exploitation typique comprend plusieurs couches hiérarchiques :

- **Matériel** : La couche physique contenant le processeur, la mémoire, les périphériques d'entrée/sortie, etc.
- **BIOS / UEFI** : Le firmware qui initialise le matériel et charge le système d'exploitation.
- **Secteur d’amorçage / Chargeur de démarrage** : Programme qui charge le noyau du système d'exploitation en mémoire.
- **Noyau** : Gère les ressources système et permet aux logiciels de communiquer avec le matériel.
- **Espace utilisateur** : Où les applications et les processus de l'utilisateur s'exécutent.

---

## Distinction : Linux vs Distribution Linux

| **Aspect**              | **Linux**                                         | **Distribution Linux**                                 |
| ----------------------- | ------------------------------------------------- | ------------------------------------------------------ |
| **Définition**          | Noyau développé par Linus Torvalds en 1991.       | Système complet incluant le noyau Linux et des outils. |
| **Fonction principale** | Gère le matériel et les ressources.               | Fournit un environnement utilisable aux utilisateurs.  |
| **Exemples**            | Linux pur (noyau uniquement).                     | Ubuntu, Fedora, Debian, Arch Linux.                    |
| **Utilisateurs ciblés** | Développeurs système et intégrateurs spécialisés. | Utilisateurs finaux ou administrateurs système.        |

---

## Historique de Unix et Linux

### Frise chronologique simplifiée

```plaintext
1969 : Création d'Unix par Ken Thompson et Dennis Ritchie.
1971 : Réécriture en langage C, rendant Unix portable.
1975 : Distribution massive d'Unix.
1983 : Lancement du projet GNU par Richard Stallman.
1985 : Fondation de la Free Software Foundation (FSF).
1991 : Linus Torvalds crée le noyau Linux.
1992 : Linux devient libre sous la licence GNU GPL.
```

### La naissance d’Unix

- **1969** : Création par Ken Thompson, inspiré de Multics, initialement écrit en assembleur.
- **1971** : Réécriture en C grâce à Dennis Ritchie, rendant Unix plus portable.
- **1975** : Début de la distribution à grande échelle.

### Gnu is Not Unix (GNU)

- **1983** : Lancement du projet GNU par Richard Stallman pour développer un système libre.
- **1985** : Fondation de la Free Software Foundation (FSF).
- **1990** : Développement avancé des outils GNU mais sans noyau pleinement fonctionnel (projet HURD inachevé).

### L’arrivée de Linux

- **1991** : Linus Torvalds crée un noyau pour apprendre et expérimenter.
- **1992** : Linux adopte la licence libre GNU GPL, facilitant sa diffusion.

---

## Avantages de Linux

- **Modifiable** : Adaptable selon les besoins spécifiques. Par exemple, les entreprises comme Google utilisent des versions modifiées de Linux (Android) pour leurs produits.
- **Partageable** : Code source librement disponible. Cela favorise des projets collaboratifs tels que Fedora ou Debian, où des milliers de contributeurs participent au développement.
- **Adaptable** : Fonctionne sur une large gamme de matériels, des serveurs web comme ceux d'Amazon AWS aux supercalculateurs comme Summit, le plus rapide au monde.
- **Simple et ludique** : Utile pour l'apprentissage et l'expérimentation, comme pour les étudiants en informatique ou les hobbyistes utilisant Raspberry Pi.
- **Répandu** : Utilisé dans divers secteurs. Par exemple :
  - **Serveurs web** : Plus de 90 % des serveurs web fonctionnent sous Linux.
  - **Supercalculateurs** : Tous les 500 supercalculateurs les plus rapides au monde utilisent Linux.
  - **IoT et embarqué** : Présent dans les appareils connectés, comme les voitures Tesla.

---

# Pratique : Installation et utilisation

## Activités

1. **Installer VirtualBox** : Créer des machines virtuelles pour expérimenter.
2. **Télécharger et installer des distributions** : Ubuntu 19.10, Debian 10 et une distribution au choix.
3. **Créer un utilisateur standard** :
   - Nom d'utilisateur : `user`
   - Mot de passe : `Azerty01`
4. **Exercices de base** : Configuration initiale, navigation dans le système.

---

# Commandes GNU & Unix

## Pourquoi la ligne de commande ?

- **Efficacité** : Plus rapide pour exécuter des tâches répétitives ou complexes.
- **Économie de ressources** : Utile sur des serveurs ou systèmes limités.
- **Contrôle avancé** : Offre des fonctionnalités non disponibles via une interface graphique.

## Commandes essentielles

### Se déplacer dans l’arborescence

```bash
cd [repertoire]  # Changer de répertoire
pwd [-LP]        # Afficher le répertoire courant
```

### Gérer les fichiers

```bash
ls [option] [repertoire]  # Lister le contenu
cp [option] source cible  # Copier des fichiers
mv [option] source cible  # Déplacer ou renommer des fichiers
rm [option] fichier       # Supprimer des fichiers
mkdir [option] repertoire # Créer des répertoires
```

### Exemples pratiques

- **Lister uniquement les fichiers cachés** : `ls -a`
- **Copier un fichier avec confirmation** : `cp -i source.txt destination/`

---

## Gestion des logiciels

### APT : Gestionnaire de paquets

APT est un outil puissant pour la gestion des logiciels sous les distributions basées sur Debian.

Un **paquet logiciel** est une archive contenant :

- Les fichiers nécessaires pour installer un logiciel (exécutables, bibliothèques, etc.).
- Des scripts de configuration ou post-installation.
- Des informations sur les dépendances requises pour son bon fonctionnement.

APT facilite l'installation, la mise à jour et la suppression de ces paquets, tout en gérant automatiquement les dépendances.

- **apt-cache** : Explorez les informations sur les paquets disponibles.
- **apt-get** : Effectuez des actions comme installer ou supprimer des logiciels.

Exemples :

```bash
apt-get update         # Mettre à jour les dépôts
apt-get install <pkg>  # Installer un paquet
apt-get remove <pkg>   # Supprimer un paquet
```

### Autres outils similaires

- **dnf** : Gestionnaire de paquets pour les distributions basées sur Red Hat.
- **pacman** : Utilisé par Arch Linux.

---

# Gestion des utilisateurs et droits

### Gestion des utilisateurs

- **adduser** : Créer un nouvel utilisateur avec des paramètres par défaut.
- **deluser** : Supprimer un utilisateur existant.
- **passwd** : Modifier le mot de passe d’un utilisateur.

### Gestion des groupes d'utilisateurs

Les groupes d'utilisateurs permettent de simplifier la gestion des droits en regroupant plusieurs utilisateurs sous une même entité logique.

- **groupadd** : Créer un groupe.
- **groupdel** : Supprimer un groupe.
- **usermod -aG [groupe] [utilisateur]** : Ajouter un utilisateur à un groupe.

### Importance des groupes dans la gestion des droits

- Facilite l'attribution des permissions (lecture, écriture, exécution) à plusieurs utilisateurs en une seule action.
- Utilisé pour sécuriser l'accès à des fichiers, répertoires ou applications sensibles.
- Simplifie l'administration, notamment dans les environnements multi-utilisateurs.

### Droits et permissions

- **chmod** : Modifiez les permissions (lecture, écriture, exécution).
- **chown** : Changez le propriétaire d’un fichier ou répertoire.
- **chgrp** : Modifiez le groupe propriétaire d’un fichier.

### Exemples

```bash
chmod 755 fichier.txt  # Lecture/écriture/exécution pour propriétaire, lecture/exécution pour les autres
chown user fichier.txt # Attribuer la propriété à 'user'
chgrp group fichier.txt # Attribuer un groupe propriétaire
```

---

# Shell : Outils et astuces

### Redirections et flux

Dans un système Unix/Linux, les flux permettent d'interagir avec les données via trois canaux principaux :

- **STDIN (Standard Input)** : Représente l'entrée standard, généralement utilisée pour recevoir des données à partir du clavier ou d'un fichier.
- **STDOUT (Standard Output)** : Représente la sortie standard, utilisée pour afficher les résultats dans le terminal.
- **STDERR (Standard Error)** : Représente la sortie d'erreur, utilisée pour afficher les messages d'erreur.

#### Commandes et exemples pratiques

- `>` : Rediriger STDOUT vers un fichier (création ou écrasement).
  - **Exemple** : `echo "Bonjour" > fichier.txt` crée un fichier contenant "Bonjour".
- `>>` : Ajouter STDOUT à un fichier existant.
  - **Exemple** : `echo "Suite" >> fichier.txt` ajoute "Suite" à la fin du fichier existant.
- `<` : Lire STDIN depuis un fichier.
  - **Exemple** : `cat < fichier.txt` affiche le contenu du fichier.
- `2>` : Rediriger STDERR vers un fichier.
  - **Exemple** : `ls dossier_inexistant 2> erreur.log` enregistre l'erreur dans le fichier `erreur.log`.
- `|` : Passer STDOUT d’une commande à STDIN d'une autre.
  - **Exemple** : `ls | grep fichier` affiche uniquement les éléments contenant "fichier" dans leur nom.

---

### Recherche et traitement

- **find** : Rechercher des fichiers selon des critères spécifiques (nom, type, taille).
- **grep** : Rechercher du texte dans des fichiers.
- **sort** : Trier des lignes dans un fichier texte.
- **uniq** : Supprimer les doublons dans un fichier trié.

---

# Conclusion

Linux offre un environnement puissant, adaptable et libre. Avec ses commandes simples et ses outils avancés, il constitue un choix idéal pour les professionnels et les amateurs. Son adoption continue de croître dans divers secteurs, rendant la maîtrise de Linux essentielle pour les informaticiens modernes.
