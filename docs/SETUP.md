# Installation et compilation

## Lancement sans build

```bash
git clone https://github.com/EngGhada/Calendrier-.git
cd Calendrier-
python -m http.server 8000
```

Visitez `http://localhost:8000`.

## Modifier les styles

Installez Dart SASS, puis compilez le point d'entrée :

```bash
npm install --global sass
sass sass/main.sass assets/css/main.min.css --style=compressed --source-map
```

## Tester les jours

La disponibilité dépend de `new Date().getDate()`. En dehors de décembre, le
comportement reste basé sur le numéro du jour du mois. Pour une démonstration
contrôlée, utilisez temporairement une valeur fixe dans les outils de
développement, sans publier cette modification.

## Audio

Certains navigateurs limitent la lecture automatique. Ici, le son est déclenché
par un clic utilisateur ; vérifiez néanmoins que l'onglet n'est pas silencieux.
