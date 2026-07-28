# Sécurité, accessibilité et limites

## Surface de sécurité

Le projet est entièrement statique : aucun compte, aucune base de données et
aucune donnée personnelle ne sont traités.

## Bonnes pratiques

- conserver les ressources locales sous contrôle de version ;
- éviter d'injecter des citations provenant d'une source non fiable ;
- déployer avec HTTPS et des en-têtes de sécurité adaptés ;
- utiliser une politique CSP si des services externes sont ajoutés.

## Accessibilité

L'utilisation de boutons et de `<dialog>` fournit une base sémantique correcte.
Les améliorations prioritaires sont :

- ajouter un libellé explicite à chaque case ;
- indiquer visuellement et par attribut l'état verrouillé ;
- gérer le focus lors de l'ouverture et de la fermeture ;
- proposer un contrôle pour couper le son ;
- vérifier les contrastes et le mouvement réduit.

## Limites fonctionnelles

La progression n'est pas persistée et la règle repose sur le jour courant du
navigateur. Le projet constitue une démonstration front-end, pas un calendrier
multi-utilisateur.
