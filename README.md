# Cépi et le Royaume d'En-Dessous

Jeu de plateforme 3D mignon, en solo ou à deux en écran scindé, pour Windows, Mac et Linux (moteur Godot 4.7). Un petit champignon, Cépi, tombe tout au fond de la terre pendant une nuit d'orage et doit retrouver sa famille à la surface : grottes luisantes, cavernes de cristal, forêt souterraine, cœur de lave, terriers… et le secret des taches de son chapeau qui brillent dans le noir.

Dernière version : voir la page **[Releases](https://github.com/Titan-CyberTech/Cepi/releases/latest)**.

## Télécharger le jeu

Ouvre la page **[Releases](https://github.com/Titan-CyberTech/Cepi/releases/latest)**.

**Windows (10 / 11, 64 bits)**
1. Télécharge `Cepi_Windows_vX.Y.Z.zip` et dézippe le dossier `Cepi_Windows` dans un endroit où tu peux écrire (Bureau, Documents…), **pas dans « Program Files »**.
2. Lance `Cepi.exe`. Si Windows affiche « Windows a protégé votre ordinateur » (jeu non signé) : *Informations complémentaires* → *Exécuter quand même*.

**Mac (macOS 11 ou plus récent, puce Apple ou Intel)**
1. Télécharge `Cepi_macOS_vX.Y.Z.zip`, ouvre-le et glisse `Cepi.app` dans ton dossier Applications.
2. Premier lancement : le jeu n'est pas signé par Apple, macOS le bloque une fois. Ouvre *Réglages Système → Confidentialité et sécurité* et clique sur **Ouvrir quand même** à côté de « Cepi » (ou dans le Terminal : `xattr -dr com.apple.quarantine /Applications/Cepi.app`).

**Linux (64 bits)**
1. Télécharge `Cepi_Linux_vX.Y.Z.zip` et dézippe-le dans ton dossier personnel (ex. `~/Jeux/Cepi`).
2. Lance `Cepi.x86_64` (double-clic, ou `./Cepi.x86_64` dans un terminal ; si besoin `chmod +x Cepi.x86_64`).

Il faut une carte graphique compatible Vulkan (ou Metal sur Mac, Direct3D 12 sous Windows). Si l'image saccade, choisis le préréglage **Bas** ou **Moyen** dans *Réglages → Graphismes*.

Le fichier `LISEZMOI.md` du dossier explique tout : histoire, commandes clavier et manette, jeu à deux, réglages.

## Nouveautés

- **2.3.0** : Mises à jour automatiques : au lancement, le jeu vérifie la dernière version publiée sur GitHub, la télécharge, la vérifie et redémarre dessus. Ta progression est conservée. Réglages > Affichage : explication pour jouer en 144 images par seconde.
- **2.2.0** : Les chutes sont toujours mortelles (plateformes fragiles, fond de grotte, pieds dans l'eau ou la lave). Coopération : les deux joueurs sont indépendants, chacun réapparaît à son propre point de passage.
- **2.1.0** : Coopération en écran scindé, une caméra par joueur ; deux manettes. Les menus se valident à la manette (A) et B revient en arrière. « Continuer » plus rapide, moisissure du chapitre 5 plus lente. Version macOS (puces Apple et Intel).
- **2.0.0** : L'aventure complète : tutoriel, 5 chapitres et un épilogue, la coopération à deux, le Carnet, un nouveau menu et beaucoup plus de réglages d'affichage.

## Mises à jour automatiques

À chaque lancement, le jeu vérifie la dernière Release publiée ici et affiche en petit, en bas à gauche, ce qu'il lit :

```
› Lecture de api.github.com/repos/Titan-CyberTech/Cepi/releases/latest
› Réponse de GitHub : code 200 · 7 Ko lus en 240 ms
› Dernière version publiée : v2.3.0 « Cépi 2.3.0 » — publiée le …
› Fichiers : Cepi.pck (72,7 Mo) · Cepi_Linux.pck (72,7 Mo) · Cepi_macOS.pck (…)
› Ta version : 2.3.0 -> le jeu est à jour
```

- En vert, tout va bien ; en jaune, une nouvelle version a été trouvée ; en rouge, un problème (hors ligne, GitHub indisponible…).
- Si une version plus récente existe, le jeu affiche ses nouveautés, télécharge le `.pck` de ton système, vérifie sa taille et son empreinte SHA-256, l'installe puis redémarre tout seul. Un bouton permet de jouer sans mettre à jour.
- La mise à jour est rangée dans le dossier de données du jeu : le jeu installé n'est jamais modifié (Windows, Linux et Mac). Si un démarrage sur la mise à jour échoue, le jeu revient tout seul à la version installée.
- Ta progression et tes réglages sont toujours conservés. Sans connexion, le jeu démarre normalement.
- GitHub limite les vérifications à 60 par heure et par connexion Internet : au-delà, le jeu l'indique et démarre quand même.

## Publier une nouvelle version

1. Préparer les 7 fichiers de la version (jeu complet, mises à jour légères, empreintes).
2. Créer une Release avec le tag **`v` + la version du jeu** (ex. `v2.4.0`), écrire les nouveautés (elles s'affichent dans le jeu) et joindre les 7 fichiers :
   - `Cepi_Windows_v2.4.0.zip`, `Cepi_macOS_v2.4.0.zip` et `Cepi_Linux_v2.4.0.zip` : le jeu complet de chaque système (pour les nouveaux joueurs, et quand la version de Godot change) ;
   - `Cepi.pck` (Windows), `Cepi_macOS.pck` (Mac) et `Cepi_Linux.pck` (Linux) : la mise à jour légère. Chaque jeu prend le fichier dont le nom contient son système (sans nom de système = Windows) ;
   - `SHA256SUMS.txt` : les empreintes de contrôle.
3. Laisser l'étiquette « Latest » (pas « Pre-release »), puis publier : tous les joueurs reçoivent la mise à jour au lancement suivant.

Police **Fredoka** (SIL Open Font License 1.1) · moteur **Godot Engine** (licence MIT).
