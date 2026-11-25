# ViralTech Market — refonte présentation VTM28

## Ce qui change
- Refonte de la page d’accueil en blanc et bleu, responsive et allégée pour navigateur console.
- Présentation commerciale après activation : confirmation explicite, date d’activation et accès au host via bouton.
- Catalogue des univers : gaming, accessoires, gestion de stock, logiciels métiers, sites Web, e-commerce, SEO, marketing, SMS, hébergement, données, automatisation, 3D, LED et maintenance.
- Visuel commercial généré pour ViralTech Market et décliné en visuels locaux.
- Campagnes locales hors connexion : Black Friday du 26 au 30 novembre 2026 ; Noël du 1er au 26 décembre ; fin d’année du 27 décembre au 15 janvier 2027. Le thème normal revient automatiquement après les périodes.
- Conservation du système d’activation V1 et de la configuration Cloudflare Worker fournie.
- Conservation des fichiers de moteur, offsets, payloads et patchs d’origine de l’archive ViralTech. Le moteur n’a pas été remplacé par celui d’Afterglow.

## Déploiement
Sauvegarder le dépôt GitHub, puis téléverser tout le contenu de cette archive à la racine de `vtm27g.github.io`. Garder `activation-config.js` et le Worker existants. Vider le cache du navigateur de test si l’ancienne page persiste.

## Important
La campagne Black Friday est fixée aux dates demandées pour 2026. Noël et fin d’année suivent les plages annuelles indiquées. La programmation se base sur l’horloge locale de la console : elle fonctionne hors connexion, mais une date/heure incorrecte sur l’appareil peut afficher une campagne incorrecte.

La confirmation d’activation reprend le stockage local V1 et le format de réponse du Worker existant. La sécurité définitive de la licence dépend toujours de la validation serveur. Aucun changement n’est fait au code de l’exploit, aux offsets ou aux payloads.

Les images sont des visuels commerciaux générés et intégrés localement, pas des photographies documentaires des locaux ou du stock réel de ViralTech Market.
