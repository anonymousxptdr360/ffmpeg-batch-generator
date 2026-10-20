# ⚡ FFmpeg Ultimate CLI Generator

Un outil web ultra-léger, zéro dépendance et 100 % local pour générer des scripts d'encodage et de compression en masse (vidéos et images) sous Windows, macOS et Linux.

---

## 📖 À propos

**FFmpeg Ultimate CLI Generator** permet d'automatiser la compression et la conversion de dossiers entiers de photos et vidéos sans aucune ligne de commande à taper manuellement. 

Ouvrez le fichier HTML dans votre navigateur, configurez vos préférences (codecs, sous-dossiers, qualité, préservation EXIF) et copiez-collez le script généré directement dans votre terminal (PowerShell, .bat ou Bash).

---

## ✨ Fonctionnalités (3.5)

- 💻 **Cross-Platform :** Génère des scripts natifs pour **Windows (PowerShell 5.1/7+ & .BAT)** et **macOS/Linux (Bash/Zsh)**.
- 🎬 **Codecs Vidéo Modernes :** Support complet de **AV1 (SVT-AV1)**, **H.265 / HEVC** et **H.264**, avec gestion fine du CRF, des presets de vitesse, du 8/10-bit (HDR) et du re-muxing intelligent (`.mkv`, `.mp4`).
- 📸 **Conversion Images & Photos :** Conversion intelligente vers **AVIF**, **HEIC** (iPhone), **WebP**, **JPG** et **PNG**.
- 📂 **Gestion des Sous-Dossiers :** 3 modes au choix (ignorer, reproduire la même arborescence, ou tout regrouper à plat avec gestion automatique des doublons de noms).
- ⏱️ **Estimation Intelligente par Benchmark :** Exécute un mini-benchmark réel de 3 secondes sur votre machine au démarrage pour calculer un temps restant précis, ajusté après chaque fichier.
- 🍎 **Compatibilité Apple Photos & EXIF :**
  - Copie intégrale des métadonnées EXIF (GPS, date de prise de vue) via **ExifTool**.
  - **Correction des captures d'écran :** Extraction de la date depuis le nom de fichier (`Screenshot_YYYYMMDD...`) pour réinjection dans le tag `DateTimeOriginal`.
  - **Rotation automatique :** Application des filtres de rotation EXIF pour éviter les photos inversées.
- 🐍 **Fallback Python + pillow-heif :** Intégration automatique de Python pour lire et encoder le format **HEIC** même si votre version de FFmpeg ne le supporte pas nativement.
- 🛡️ **Sécurité & Résilience :**
  - **Reprise après interruption :** Détecte et saute les fichiers déjà traités.
  - **Anti-boucle infinie :** Exclut automatiquement le dossier de destination s'il est situé dans la source.
  - **Option de secours :** Copie l'original tel quel si un fichier est corrompu ou illisible afin d'éviter toute perte dans votre galerie.
- 🔒 **100 % Local & Privé :** Fonctionne à 100 % dans votre navigateur. Aucune donnée, aucun chemin et aucun fichier ne quittent votre ordinateur.

---

## ⚙️ Prérequis

Pour exécuter les scripts générés, les outils suivants doivent être installés sur votre système (détectés automatiquement par le script s'ils sont dans le PATH).

### 1. FFmpeg (Indispensable)

#### Windows
Ouvrez PowerShell et installez la version complète via Winget :
```cmd
winget install Gyan.FFmpeg

```

*(Pensez à redémarrer PowerShell après l'installation).*

#### macOS

Via Homebrew :

```bash
brew install ffmpeg

```

#### Linux

```bash
# Ubuntu / Debian
sudo apt update && sudo apt install ffmpeg

# Fedora
sudo dnf install ffmpeg

# Arch Linux
sudo pacman -S ffmpeg

```

---

### 2. ExifTool (Recommandé pour conserver les dates & GPS des photos)

#### Windows

```cmd
winget install OliverBetz.ExifTool

```

#### macOS

```bash
brew install exiftool

```

#### Linux (Ubuntu/Debian)

```bash
sudo apt install libimage-exiftool-perl

```

---

### 3. Python + pillow-heif (Uniquement pour le format HEIC / Photos iPhone)

Si vous traitez des photos HEIC et que votre version de FFmpeg est inférieure à 7.1, installez la bibliothèque Python suivante :

```bash
pip install pillow-heif

```

*(Le script PowerShell/Bash tentera une installation automatique via `pip` s'il détecte Python sur votre machine).*

---

## 🚀 Utilisation

1. **Récupérez le projet :**
```bash
git clone https://github.com/anonymousxptdr360/ffmpeg-batch-generator.git
```


*(ou téléchargez simplement le fichier `index.html` depuis la page des Releases).*
2. **Ouvrez `index.html**` dans n'importe quel navigateur web.
3. **Indiquez les chemins :**
* Dossier source *(ex: `C:\Users\Nom\Pictures\Photos`)*
* Dossier de destination *(ex: `D:\Compresses`)*


4. **Ajustez vos réglages :** Choisissez le format cible (AV1, HEIC, AVIF...), la qualité (CRF) et le mode de sous-dossiers.
5. **Lancez le script :**
* **Bouton Copier :** Collez le code directement dans votre terminal.
* **Bouton Télécharger :** Téléchargez le fichier (`.ps1`, `.bat` ou `.sh`) et exécutez-le.



---

## 🔒 Confidentialité & Sécurité

Ce générateur est une application statique exécutée côté client :

* ❌ Aucun serveur backend
* ❌ Aucun cookie ni traqueur
* ❌ Aucune télémétrie
* ✅ Fonctionne entièrement hors-ligne

---

## 📄 Licence

Ce projet est sous licence **MIT**.

Vous êtes totalement libre de l'utiliser, le modifier, le distribuer, l'intégrer dans des projets privés ou commerciaux, **à la seule condition d'inclure la notice de copyright d'origine et de créditer l'auteur (`anonymousxptdr360`)**.

Voir le fichier `LICENSE` pour plus de détails.

---

## 📦 Dépôt GitHub

Projet hébergé sur :

👉 https://anonymousxptdr360.github.io/ffmpeg-batch-generator/FFmpeg.html
