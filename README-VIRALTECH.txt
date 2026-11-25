# ViralTech Market — raw13g personnalisé

## Modifications appliquées
- Remplacement du branding visible « RAW GAME » par ViralTech Market.
- Ajout d'un logo SVG local `viraltech-logo.svg`.
- Ajout d'un écran de présentation temporaire avec les tarifs et contacts fournis.
- Ajout d'un écran d'activation après la présentation.
- La page `jb.html` vérifie également l'activation avant de charger `jb.js`, afin d'éviter un accès direct accidentel à la page d'exécution.
- Mise à jour de `cache.appcache` et de la version de l'entrée `jb.js?v=20`.
- Les fichiers d'exploit, les tables d'offsets et les payloads binaires d'origine n'ont pas été modifiés.

## Règle d'activation actuelle
Le code local doit comporter 10 chiffres, commencer par `26` et avoir une somme de chiffres divisible par 7.

**Limite importante :** cette règle et le drapeau `localStorage` sont entièrement côté navigateur. Ils peuvent être inspectés, contournés ou effacés par un utilisateur qui contrôle la console. Ce n'est pas une licence sécurisée ni une protection contre la copie. Une vraie validation exige un service de licence distant ou une autre architecture de confiance.

## À propos de la stabilité
Les fichiers `core.js`, `jb.js`, `mem.js`, `int64.js`, `ps4_offsets.js`, `rpc_worker.js`, `goldhen.bin`, `payload2.bin` et les patchs binaires sont conservés tels quels. Le verrou est placé avant le chargement du module de l'exploit, sans modifier la chaîne d'exploitation elle-même. Cela réduit le risque de casser cette chaîne, mais ne garantit pas l'absence de Kernel Panic : l'exécution d'un exploit reste intrinsèquement risquée et dépend du firmware et de l'état de la console.

## Déploiement
Téléverser le contenu du dossier `raw13g.github.io-main` dans la racine du dépôt GitHub Pages en conservant l'arborescence. Le manifeste AppCache est obsolète dans les navigateurs modernes, mais a été conservé pour rester cohérent avec le projet original ciblant le navigateur PS4.
