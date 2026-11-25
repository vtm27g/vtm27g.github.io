# ViralTech Market — Console Host (Afterglow integration)

## Ce que contient cette version
- Host console, et non un site vitrine classique.
- Écran d'activation ViralTech Market conservant le point d'accès du service de licence de la version fournie.
- Confirmation de licence avec date locale, puis écran de sélection du payload.
- Carrousel de présentations commerciales locales pendant l'attente et le compte à rebours de lancement.
- Publicités/présentations : accessoires gaming, gestion de stock, création web et visibilité digitale.
- Présentation de GoldHEN sous le libellé « GoldHEN · présentation ViralTech Market ». Le binaire GoldHEN et ses crédits ne sont pas modifiés.
- Moteur Afterglow complet et fichiers d'origine copiés depuis l'archive Afterglow fournie.

## Firmwares annoncés par le projet Afterglow fourni
12.00, 12.02, 12.50, 12.52, 13.00, 13.02, 13.04, 13.50, 13.52, 14.00 et 14.02.

Il ne s'agit pas de tous les sous-firmwares imaginables entre 12.00 et 14.02 : seuls les onze firmwares listés dans le README source sont annoncés. Le moteur doit refuser les versions sans profil correspondant.

## Pourquoi les publicités ne s'affichent pas sur la page d'exécution
La documentation technique Afterglow explique que la page d'exécution doit rester très légère : toute ressource supplémentaire peut modifier le timing et l'allocation mémoire au moment critique. Le carrousel est donc placé sur l'écran de lancement, avant la navigation vers `jb.html`. Il s'arrête avant le démarrage de la chaîne d'exploitation. La page `jb.html` ne charge aucune publicité, analytics, police distante ou image animée pendant l'exécution.

## Branding GoldHEN
Le nom affiché dans le choix du payload et dans l'interface du host peut être accompagné de « Présentation ViralTech Market ». Le binaire `goldhen.bin` n'est pas modifié : son identité, ses crédits et ses conditions de redistribution sont conservés. Cette archive ne prétend pas que ViralTech Market est l'auteur de GoldHEN.

## Activation
Le code est vérifié par le service configuré dans `activation-config.js`. Après validation, l'enregistrement est mémorisé dans le stockage local du navigateur. Effacer les données du navigateur peut supprimer cet enregistrement. Le contrôle local sert à éviter une nouvelle saisie sur le même navigateur ; il ne remplace pas une validation serveur.

## Publication et cache
1. Sauvegarder le dépôt actuel.
2. Extraire le contenu de cette archive à la racine du dépôt GitHub Pages.
3. Vérifier que `activation-config.js` contient toujours le bon endpoint.
4. Publier tous les fichiers sans modifier les dossiers `patchset` ou les binaires.
5. Effacer l'ancien cache du navigateur de la console ou attendre la mise à jour du manifeste.
6. Tester d'abord l'activation et l'écran de lancement, puis les firmwares sur console de test.

Le manifeste `cache.appcache` est régénéré pour cette archive. La compatibilité du cache dépend du navigateur de la console.

## Avertissement
L'exploit noyau peut échouer et provoquer un redémarrage ou un Kernel Panic. Le projet Afterglow décrit les essais et limites dans `README.md` et `TECHNICAL.md`. Les vérifications effectuées ici sont statiques ; aucune console PS4 physique n'a été testée dans cet environnement.

## Licences et crédits
Conserver `LICENSE`, `LICENSE-raw13g`, `README.md` et `TECHNICAL.md`. Les fichiers provenant d'Afterglow, raw13g et GoldHEN gardent leurs crédits et leurs licences d'origine.
