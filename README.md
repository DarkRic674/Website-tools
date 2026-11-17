# Website-tools
List of tools for a website.

# Image Tools

🇫🇷 [Français](#-français) · 🇬🇧 [English](#-english) · 🇯🇵 [日本語](#-日本語) · 🇪🇸 [Español](#-español)

---

## 🇫🇷 Français

Trois outils pour récupérer et gérer de grandes collections d'images. Ils fonctionnent sous Windows.

**Langue :** chaque outil propose un menu déroulant (Français, English, 日本語, Español). Le choix est mémorisé et partagé entre les trois outils.

### 1. Image Extractor (`image_extractor.exe`)
Télécharge les images d'un ou plusieurs sites web.

- **Modes :**
  - *Cette page uniquement* : analyse l'URL indiquée.
  - *Plusieurs pages (liste)* : colle une URL par ligne, ou charge un fichier `.txt`.
  - *Site entier* : suit les liens du même domaine (nombre de pages max réglable, 100 par défaut).
- **Formats :** .jpg, .png, .gif, .webp, .svg, .bmp, .avif, .ico (cases à cocher).
- **Options :** taille minimale en Ko (pour ignorer les miniatures), sous-dossier par domaine, bouton Arrêter, bouton Ouvrir le dossier.
- **Lancer :** double-clique sur `image_extractor.exe`.
- **Limites :** les images chargées uniquement par JavaScript (scroll infini, galeries dynamiques) ne sont pas toutes détectées. Respecte les conditions d'utilisation des sites et les droits d'auteur.

### 2. Supprimer les doublons (`supprimer_doublons.py`)
Supprime les fichiers `nom_1.ext`, `nom_2.ext`… lorsque `nom.ext` existe dans le même dossier. L'original est toujours conservé.

- **Modes :**
  - *Selon le nom* (par défaut) : supprime tous les `_1`, `_2`… dont l'original existe.
  - *Contenu identique uniquement* : plus prudent, ne supprime que les fichiers strictement identiques (il en supprime donc moins).
- **Options :** inclure les sous-dossiers, barre de progression, bouton Arrêter.
- **Sécurité :** la liste des fichiers à supprimer s'affiche et une confirmation est demandée. **La suppression est définitive (pas de corbeille).**
- **Ligne de commande :** `python supprimer_doublons.py "C:\dossier" --sub --identical --yes` (sans `--yes`, affiche seulement la liste).

### 3. Organiser un dossier (`organiser_dossier.py`)
Répartit les fichiers d'un dossier dans des sous-dossiers `Lot_001`, `Lot_002`… (1000 fichiers chacun par défaut).

- **Options :** nombre de fichiers par sous-dossier, images uniquement (décoché = tous les fichiers), barre de progression, bouton Arrêter.
- Les fichiers sont **déplacés** (pas copiés), donc l'opération est rapide. Seuls les fichiers à la racine du dossier choisi sont traités.
- Si tu relances le script plus tard, la numérotation continue (`Lot_041`…) sans écraser les lots existants.
- **Ligne de commande :** `python organiser_dossier.py "C:\dossier" --size 1000 --yes` (ajoute `--all` pour tous les types de fichiers).

---

## 🇬🇧 English

Three tools to collect and manage large image collections. They run on Windows.

**Language:** every tool has a drop-down menu (Français, English, 日本語, Español). Your choice is remembered and shared across the three tools.

### 1. Image Extractor (`image_extractor.exe`)
Downloads images from one or several websites.

- **Modes:**
  - *This page only*: scans the URL you enter.
  - *Multiple pages (list)*: paste one URL per line, or load a `.txt` file.
  - *Entire site*: follows links within the same domain (adjustable max pages, 100 by default).
- **Formats:** .jpg, .png, .gif, .webp, .svg, .bmp, .avif, .ico (checkboxes).
- **Options:** minimum size in KB (to skip thumbnails), subfolder per domain, Stop button, Open folder button.
- **Run:** double-click `image_extractor.exe`.
- **Limitations:** images loaded only through JavaScript (infinite scroll, dynamic galleries) may not all be detected. Respect website terms of use and copyright.

### 2. Delete duplicates (`supprimer_doublons.py`)
Deletes `name_1.ext`, `name_2.ext`… files when `name.ext` exists in the same folder. The original is always kept.

- **Modes:**
  - *By name* (default): deletes every `_1`, `_2`… whose original exists.
  - *Identical content only*: safer, only deletes byte-for-byte identical files (so it deletes fewer).
- **Options:** include subfolders, progress bar, Stop button.
- **Safety:** the list of files to delete is shown and you must confirm. **Deletion is permanent (no recycle bin).**
- **Command line:** `python supprimer_doublons.py "C:\folder" --sub --identical --yes` (without `--yes`, it only lists the files).

### 3. Organize a folder (`organiser_dossier.py`)
Splits the files of a folder into subfolders `Lot_001`, `Lot_002`… (1000 files each by default).

- **Options:** files per subfolder, images only (unchecked = all files), progress bar, Stop button.
- Files are **moved** (not copied), so it is fast. Only files at the root of the chosen folder are processed.
- If you run it again later, numbering continues (`Lot_041`…) without overwriting existing batches.
- **Command line:** `python organiser_dossier.py "C:\folder" --size 1000 --yes` (add `--all` for every file type).

---

## 🇯🇵 日本語

大きな画像コレクションを回収して管理するための3つのツール。Windowsで動作します。

**言語：** すべてのツールにドロップダウンメニュー（Français、English、日本語、Español）があります。選択した言語は記憶され、3つのツールで共有されます。

### 1. Image Extractor（`image_extractor.exe`）
1つまたは複数のウェブサイトから画像をダウンロードします。

- **モード：**
  - *このページのみ*：入力したURLを解析します。
  - *複数ページ（リスト）*：1行に1つのURLを貼り付けるか、`.txt`ファイルを読み込みます。
  - *サイト全体*：同じドメイン内のリンクをたどります（最大ページ数は変更可能、初期値は100）。
- **形式：** .jpg、.png、.gif、.webp、.svg、.bmp、.avif、.ico（チェックボックスで選択）。
- **オプション：** 最小サイズ（KB、サムネイルの除外用）、ドメインごとのサブフォルダ、停止ボタン、フォルダを開くボタン。
- **起動：** `image_extractor.exe`をダブルクリックします。
- **制限事項：** JavaScriptだけで読み込まれる画像（無限スクロールや動的ギャラリー）はすべて検出できない場合があります。ウェブサイトの利用規約と著作権を尊重してください。

### 2. 重複ファイルの削除（`supprimer_doublons.py`）
同じフォルダに`名前.拡張子`がある場合、`名前_1.拡張子`、`名前_2.拡張子`…を削除します。元のファイルは必ず残ります。

- **モード：**
  - *名前で判定*（初期設定）：元ファイルが存在するすべての`_1`、`_2`…を削除します。
  - *内容が同一のものだけ*：より安全で、バイト単位で完全に同一のファイルのみ削除します（そのため削除数は少なくなります）。
- **オプション：** サブフォルダを含める、進捗バー、停止ボタン。
- **安全性：** 削除対象のリストが表示され、確認が求められます。**削除は完全に行われます（ごみ箱には入りません）。**
- **コマンドライン：** `python supprimer_doublons.py "C:\フォルダ" --sub --identical --yes`（`--yes`がない場合はリスト表示のみ）。

### 3. フォルダ整理（`organiser_dossier.py`）
フォルダ内のファイルをサブフォルダ`Lot_001`、`Lot_002`…に振り分けます（初期値は1フォルダあたり1000件）。

- **オプション：** 1フォルダあたりのファイル数、画像のみ（オフの場合はすべてのファイル）、進捗バー、停止ボタン。
- ファイルは**移動**されます（コピーではありません）ので高速です。選択したフォルダ直下のファイルのみが対象です。
- 後で再実行した場合、既存のフォルダを上書きせず、番号は続きから振られます（`Lot_041`…）。
- **コマンドライン：** `python organiser_dossier.py "C:\フォルダ" --size 1000 --yes`（すべての種類のファイルを対象にするには`--all`を追加）。

---

## 🇪🇸 Español

Tres herramientas para recopilar y gestionar grandes colecciones de imágenes. Funcionan en Windows.

**Idioma:** cada herramienta tiene un menú desplegable (Français, English, 日本語, Español). La elección se guarda y se comparte entre las tres herramientas.

### 1. Image Extractor (`image_extractor.exe`)
Descarga imágenes de uno o varios sitios web.

- **Modos:**
  - *Solo esta página*: analiza la URL indicada.
  - *Varias páginas (lista)*: pega una URL por línea o carga un archivo `.txt`.
  - *Sitio completo*: sigue los enlaces del mismo dominio (máximo de páginas ajustable, 100 por defecto).
- **Formatos:** .jpg, .png, .gif, .webp, .svg, .bmp, .avif, .ico (casillas de verificación).
- **Opciones:** tamaño mínimo en KB (para omitir miniaturas), subcarpeta por dominio, botón Detener, botón Abrir carpeta.
- **Ejecutar:** haz doble clic en `image_extractor.exe`.
- **Limitaciones:** las imágenes que se cargan solo mediante JavaScript (scroll infinito, galerías dinámicas) pueden no detectarse todas. Respeta las condiciones de uso de los sitios y los derechos de autor.

### 2. Eliminar duplicados (`supprimer_doublons.py`)
Elimina los archivos `nombre_1.ext`, `nombre_2.ext`… cuando `nombre.ext` existe en la misma carpeta. El original siempre se conserva.

- **Modos:**
  - *Por nombre* (por defecto): elimina todos los `_1`, `_2`… cuyo original existe.
  - *Solo contenido idéntico*: más prudente, solo elimina archivos idénticos byte a byte (por lo tanto, elimina menos).
- **Opciones:** incluir subcarpetas, barra de progreso, botón Detener.
- **Seguridad:** se muestra la lista de archivos a eliminar y se pide confirmación. **La eliminación es definitiva (no pasa por la papelera).**
- **Línea de comandos:** `python supprimer_doublons.py "C:\carpeta" --sub --identical --yes` (sin `--yes`, solo muestra la lista).

### 3. Organizar una carpeta (`organiser_dossier.py`)
Reparte los archivos de una carpeta en subcarpetas `Lot_001`, `Lot_002`… (1000 archivos cada una por defecto).

- **Opciones:** archivos por subcarpeta, solo imágenes (desmarcado = todos los archivos), barra de progreso, botón Detener.
- Los archivos se **mueven** (no se copian), por lo que es rápido. Solo se procesan los archivos en la raíz de la carpeta elegida.
- Si lo ejecutas de nuevo más tarde, la numeración continúa (`Lot_041`…) sin sobrescribir los lotes existentes.
- **Línea de comandos:** `python organiser_dossier.py "C:\carpeta" --size 1000 --yes` (añade `--all` para todos los tipos de archivo).
