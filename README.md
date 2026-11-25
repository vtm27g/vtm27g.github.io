# VIRALTECH MARKET — ÉDITION CONSOLE PS4

## Présentation
Cette archive regroupe l’interface ViralTech Market et le moteur PS4 fourni dans les archives sources. L’écran d’accueil, l’activation, les présentations commerciales, le choix du payload et l’écran d’initialisation portent l’identité ViralTech Market.

## Firmwares présents dans le projet source
12.00 · 12.02 · 12.50 · 12.52 · 13.00 · 13.02 · 13.04 · 13.50 · 13.52 · 14.00 · 14.02.

Cette liste reprend les profils présents dans le moteur fourni. Elle ne signifie pas que tous les profils ont le même niveau de validation : les notes techniques d’origine comportent des statuts différents selon les versions. Consultez `docs/TECHNICAL-SOURCE.md` et `docs/README-SOURCE-AFTERGLOW.md` avant tout essai. Aucun firmware absent de cette liste n’est ajouté ou présenté comme compatible.

## Environnements disponibles
- **GoldHEN** : binaire fourni dans l’archive source.
- **PS4-HEN** : binaire fourni dans l’archive source, décrit comme corrigé pour le cas 14.00 dans la documentation source.

Les binaires, les offsets, les patchsets et la chaîne d’exécution ne sont pas réécrits par cette refonte visuelle. Le nom et l’identité de l’édition présentée au client sont ViralTech Market. Les noms techniques GoldHEN et PS4-HEN restent ceux des payloads sélectionnables.

## Activation client
Le point d’accès configuré dans `activation-config.js` a été conservé. Après une première validation serveur, l’état local est enregistré dans le navigateur. Lors des visites suivantes sur le même navigateur, l’utilisateur revient directement au lanceur sans ressaisir son code, tant que les données locales ne sont pas effacées. Cette mémorisation locale ne remplace pas la validation serveur initiale.

## Présentations ViralTech Market
Le carrousel local présente les activités suivantes : consoles et accessoires gaming, gestion commerciale et stocks, création web et présence numérique, marketing digital et automatisation, solutions techniques et fabrication 3D. Une mention saisonnière hors ligne est calculée à partir de la date locale de la console. Aucune publicité distante ni ressource externe n’est chargée pendant l’étape d’exploitation.

## Installation / publication
1. Sauvegarder le dépôt existant.
2. Décompresser le contenu de cette archive à la racine du dépôt GitHub Pages ou du serveur statique.
3. Conserver `activation-config.js` sans remplacer l’URL du service d’activation.
4. Publier tous les fichiers et dossiers, notamment `patchset-*.bin`, `goldhen.bin` et `hen.bin`.
5. Sur la console, fermer les anciennes pages, effacer si nécessaire l’ancien cache applicatif, puis rouvrir le host.
6. Effectuer les essais sur une console de test, firmware par firmware.

Pour un serveur local : `./serve.sh` (port 8000) ou `VTM_PORT=8080 ./serve.sh`.

## Limites et précautions
Un exploit noyau peut échouer, entraîner un redémarrage ou provoquer un blocage. Ne pas interrompre l’alimentation pendant une opération. Les vérifications réalisées pour cette archive sont des contrôles statiques et de cohérence des fichiers ; aucune console physique n’a été testée ici. La compatibilité réelle et la stabilité doivent être confirmées sur matériel.

## Provenance, crédits et licences
L’interface et la présentation commerciale de cette édition sont ViralTech Market. Les composants techniques tiers conservent leurs auteurs, crédits, notices et licences d’origine. Les fichiers `LICENSE`, `LICENSE-raw13g`, ainsi que les documents source dans `docs/`, sont conservés. Cette édition ne revendique pas la création de GoldHEN, de PS4-HEN ni du moteur tiers.
