# Architecture du Calendrier de l'Avent

## Organisation front-end

Le projet utilise des fichiers statiques et un module JavaScript principal.
`index.html` fournit les 25 boutons et le composant `<dialog>`. `script.js`
orchestre les interactions et importe les citations depuis `quotes.js`.

## Flux d'une interaction

```mermaid
sequenceDiagram
    actor U as Utilisateur
    participant B as Bouton du jour
    participant J as script.js
    participant M as Fenêtre modale
    U->>B: clique sur une case
    B->>J: transmet le numéro
    J->>J: compare avec la date courante
    alt jour disponible
        J->>J: joue le son et révèle l'image
        J->>M: insère la citation et ouvre le dialogue
        M-->>U: affiche la surprise
    else jour futur
        J-->>U: conserve la case fermée
    end
```

## Architecture SASS 7-1

- `abstracts/` : variables et mixins réutilisables ;
- `base/` : resets et déclaration des polices ;
- `components/` : calendrier et fenêtre modale ;
- `page/` : composition générale de la page ;
- `main.sass` : point d'entrée qui assemble les modules.

Le CSS minifié généré est versionné afin que le projet fonctionne sans étape de
build pour une simple démonstration.
