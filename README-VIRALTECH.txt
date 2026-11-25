# ViralTech Market — VTM27 Major Update (release candidate)

## Contenu intégré
Cette version assemble l'interface et l'activation ViralTech Market avec le moteur Afterglow fourni dans l'archive source.

- Firmware annoncés par le projet Afterglow : 12.00, 12.02, 12.50, 12.52, 13.00, 13.02, 13.04, 13.50, 13.52, 14.00 et 14.02.
- Moteur navigateur : `jb.js`, `core.js`, `mem.js`, `int64.js`, `ps4_offsets.js` et `afterglow.js` issus de l'archive Afterglow.
- Payloads : `hen.bin` et `goldhen.bin` issus de l'archive Afterglow.
- Correctifs noyau : les onze fichiers `patchset-*.bin` correspondants sont inclus.
- Activation ViralTech : endpoint conservé dans `activation-config.js`.
- Compatibilité de l'activation précédente : les enregistrements `vtm27_activation_v1` sont migrés vers `vtm27_activation_v2` sur le même navigateur.
- Présentation : catalogue et informations commerciales restent sur la page d'accueil. Aucun élément publicitaire n'est injecté dans la page d'exécution du moteur.

## Utilisation et publication
1. Faire une copie de sauvegarde du dépôt GitHub actuel.
2. Extraire le contenu de cette archive.
3. Publier le contenu du dossier à la racine de `vtm27g.github.io`.
4. Vérifier que `activation-config.js` pointe toujours vers le service d'activation déployé.
5. Ouvrir `https://vtm27g.github.io/` depuis le navigateur de la console.
6. Effectuer d'abord un test de présentation et d'activation, puis un test du moteur sur une console de test sans données importantes.

## Avertissement de stabilité
Le moteur est un exploit noyau. Aucun changement logiciel ne peut garantir zéro échec, zéro redémarrage ou zéro Kernel Panic. Le README Afterglow décrit les firmwares pris en charge et les essais réalisés par ses auteurs, mais l'intégration ViralTech Market de cette archive n'a pas été testée sur matériel PS4 dans cet environnement. Ne présentez pas cette version comme garantie sans essais réels sur chaque firmware et modèle ciblés.

Les firmwares non répertoriés par le moteur doivent être refusés. Ne forcez pas l'exécution avec des offsets d'une autre version.

## Vérification du binaire PS4-HEN
Le README de l'archive Afterglow annonce pour `hen.bin` le MD5 `6417a84a72f9c7988f0e33b3ae190542` (version corrigée), mais le fichier réellement fourni dans cette archive produit le MD5 `e7df7fb94e58a1b4a4a5e7dda4f190e1`. Ces valeurs ne correspondent pas. Pour éviter de risquer un gel de console, PS4-HEN est donc désactivé dans le sélecteur de cette release candidate. GoldHEN reste le choix activé par défaut. Ne réactivez PS4-HEN qu'après obtention et vérification d'un binaire correspondant au hash attendu ou confirmation fiable de l'auteur.

## Activation
La validation initiale dépend du service distant configuré. L'accès local est mémorisé dans le navigateur pour éviter de redemander le code à chaque visite. Comme tout contrôle côté navigateur, un marqueur local peut être modifié par un utilisateur ayant le contrôle de l'appareil : la décision d'autorisation réelle doit rester côté serveur.

## Fichiers techniques et licences
Consulter `TECHNICAL.md`, `UPSTREAM-README.md`, `LICENSE` et `LICENSE-raw13g`. Les composants conservent leurs licences et attributions d'origine.
