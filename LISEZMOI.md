# Cépi et le Royaume d'En-Dessous

Un petit champignon, Cépi, tombe tout au fond de la terre pendant une nuit d'orage.
Pour rejoindre sa famille à la surface, il traverse le Royaume d'En-Dessous :
grottes luisantes, cavernes de cristal, forêt souterraine, cœur de lave et terriers…
et découvre pourquoi les taches de son chapeau brillent dans le noir.

Jeu de plateforme 3D réalisé avec **Godot 4.7** (rendu Forward+, Vulkan), jouable
**seul ou à deux** en coopération locale. Tout le contenu (personnages, niveaux,
végétation, textures, sons et musiques) est généré par le projet lui-même : il n'y
a aucun asset externe à part la police Fredoka.

**Version 2.3** : l'aventure complète (tutoriel, 5 chapitres et un épilogue), la
coopération à deux en écran scindé, le Carnet (histoire, personnages, pages à
retrouver), un nouveau menu principal, beaucoup plus de réglages d'affichage, et une
version macOS.

## Lancer le jeu

- **Version exportée** : décompresse l'archive et lance `Cepi.exe` (Windows),
  `Cepi.x86_64` (Linux) ou `Cepi.app` (macOS). Aucune installation nécessaire.
- **macOS** : l'application n'est pas signée par Apple. Au premier lancement, fais
  un clic droit (ou Ctrl + clic) sur l'application > **Ouvrir**, puis confirme. Si macOS
  indique qu'elle est « endommagée », ouvre le Terminal et tape
  `xattr -cr ` suivi du chemin de l'application (glisse-la dans la fenêtre), puis Entrée.
  Compatible Mac Apple Silicon (M1 et suivants) et Intel, macOS 11 ou plus récent conseillé.
- **Depuis les sources** : ouvre `project.godot` avec Godot 4.7 (ou plus récent),
  laisse l'import se terminer (quelques minutes la première fois), puis F5.

Il faut une carte graphique compatible Vulkan (ou Direct3D 12 sous Windows). Si l'image
saccade, choisis le préréglage **Bas** ou **Moyen** dans Réglages > Graphismes.

## L'aventure

| | Chapitre | Ce qui t'attend |
|---|---|---|
| 0 | L'École de Pépé Colimaçon | Le tutoriel : chaque mouvement expliqué par un vieil escargot |
| 1 | Les Grottes Luisantes | Le réveil de Cépi, le lac, la clairière, le champignon géant |
| 2 | Les Cavernes de Cristal | Lila, les cristaux chantants, les ponts de lumière, la Géode, le Cœur de Cristal |
| 3 | La Forêt des Racines | Arbres-lanternes, courants d'air, le village de Racine-Creuse |
| 4 | Le Cœur Ardent | Orgues de basalte, fleuve de lave, geysers, la Reine Lampyre |
| 5 | La Grande Remontée | La fuite devant la Moisissure d'Ombre qui monte |
| 6 | L'Aube | La surface, le Vieux Chêne et les retrouvailles |

Chaque chapitre cache **3 lucioles** et une **page du carnet de Grand-Mère Morille**.
Le **Carnet** (menu principal ou pause) rassemble l'histoire, les personnages et les pages.
À la fin du chapitre 2, Cépi obtient l'**Élan**, un bond en avant utilisable en l'air.

## Commandes

| Action | Clavier / souris | Manette |
|---|---|---|
| Se déplacer | ZQSD (ou WASD) / flèches | Stick gauche |
| Caméra | Souris | Stick droit |
| Sauter (maintenir = plus haut) | Espace | A |
| Planer (en l'air : rappuyer et maintenir) | Espace | A |
| Courir vite | Maj | B ou gâchette droite |
| Tourbillon (assomme, fait chanter les cristaux) | E ou clic gauche | X |
| Élan (après le chapitre 2) | F ou clic droit | Y ou RB |
| Recentrer la caméra | C ou clic molette | Clic stick droit |
| Pause | Échap ou P | Start |
| Menus : valider / retour | Entrée / Échap | A / B |

Les touches sont lues par position physique : ZQSD fonctionne en AZERTY, WASD en QWERTY.

### Jouer à deux

Dans le menu principal, règle **Joueurs : Coopération à deux** puis lance une partie.
Le 2e joueur incarne **Lila**. L'écran est **scindé** : Cépi à gauche, Lila à droite,
chacun avec sa caméra (stick droit de sa manette). Les deux joueurs sont indépendants :
chacun avance à son rythme et, s'il tombe, réapparaît à son propre dernier point de
passage. Les cœurs sont partagés.

- **Deux manettes** : une par joueur (la manette 1 joue Cépi, la manette 2 joue Lila ;
  le clavier et la souris restent utilisables pour Cépi).
- **Une manette** : Cépi au clavier + souris, Lila à la manette.
- **Aucune manette** (clavier partagé) : Cépi = ZQSD/WASD, Espace, Maj gauche, E, F ;
  Lila = flèches, Entrée (ou Ctrl droit), Maj droit, Suppr, Fin.

## Mises à jour automatiques

À chaque lancement, le jeu vérifie sur GitHub (github.com/Titan-CyberTech/Cepi) s'il existe une
version plus récente. Si oui, il affiche les nouveautés, télécharge la mise à jour, la vérifie
puis redémarre tout seul. Ta progression et tes réglages sont conservés ; sans connexion, le jeu
démarre normalement.

## Réglages

- **Graphismes** : préréglages Bas/Moyen/Haut/Ultra, anticrénelage (FXAA, SMAA, MSAA,
  TAA), qualité des ombres, brouillard volumétrique, SSAO, SSIL, SSR, halo lumineux,
  densité de végétation, distance d'affichage, échelle de rendu (50 à 200 %), AMD FSR 1/2.
- **Affichage** : fenêtré, plein écran, plein écran exclusif, fenêtré sans bordure ;
  la résolution native de l'écran + 27 résolutions de 800 × 600 à 5120 × 2880
  (4:3, 5:4, 16:9, 16:10, 21:9, 32:9) ; V-Sync ;
  limite d'images par seconde (30 à 240, dont 144 i/s) ; champ de vision ; luminosité ; compteur d'images.
- **Son** : volume général, musique, effets, ambiance.
- **Commandes** : sensibilités, inversion des axes, caméra automatique, vibrations.
- **Jeu** : conseils, cœurs infinis (mode détente), chronomètre, secousses de caméra,
  effacement de la progression.

La progression est sauvegardée automatiquement (chapitres, records, lucioles, pages).

## Organisation du projet

```
scenes/            main.tscn (déroulement), levels/*.tscn (niveaux générés)
scripts/
  autoload/        game.gd (état, commandes, progression, réglages), audio.gd
  data/            level_db.gd (chapitres, histoire), biomes.gd (ambiances), lore.gd (personnages, carnet, dialogues)
  player/          player.gd (contrôleur, Élan, bulle), cepi_model.gd (Cépi, Lila, la famille), camera_rig.gd
  entities/        spores, lucioles, pages, cristaux chantants, ponts de lumière, courants d'air,
                   geysers, Moisissure, personnages, arbres, maisons-champignons, ponts…
  level/           level.gd (atmosphère, terrain, végétation), eau, lave, particules
  ui/              interface en jeu, menus, réglages, kit de composants
shaders/           personnages, terrain, eau, lave, Moisissure, cristaux, végétation, écorce…
assets/            levels/<id>/ (terrain GLB, décor, parcours), textures, sons, musiques, portraits
tools/             générateurs Python (ignorés par Godot)
```

### Régénérer le contenu (optionnel)

Python 3 + numpy, scipy, scikit-image, trimesh, fast-simplification, pillow (et ffmpeg
pour l'audio) :

```
cd tools/levelgen
python build_terrain.py z2_cristal     # grotte + îlots (GLB) et dispersion du décor
python write_scene.py z2_cristal       # scène du niveau + parcours du pilote automatique
cd ..
python gen_textures.py                 # textures de roche et de mousse
python gen_audio.py ; python gen_audio2.py   # bruitages, ambiances, musiques
```

Les chapitres 2 à 6 et le tutoriel sont décrits dans `tools/levelgen/levels/*.py` avec
un « constructeur de parcours » (`builder.py`) qui vérifie que chaque saut est faisable
avec la physique de Cépi, creuse la grotte autour du chemin et écrit un parcours de test.

### Tests automatiques

Chaque niveau est vérifié par un pilote automatique qui le termine de bout en bout :

```
godot --headless --path . --fixed-fps 60 res://scenes/main.tscn -- --level=z3_racines --autopilot=route --quit-at=300
```

Secrets : `--autopilot=secret1` (avec `--checkpoint=N`), `page`, `secret2`, `secret3`.
Coopération : ajoute `--coop` (un robot suit le joueur 1).

## Crédits

- Police **Fredoka** — SIL Open Font License 1.1 (voir `assets/fonts/OFL.txt`).
- Moteur **Godot Engine** — licence MIT.
