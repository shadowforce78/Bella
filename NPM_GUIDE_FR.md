# Guide d'introduction à NPM : Lettre à Papa

Papa,

Vous m'avez demandé ce qu'était NPM. Veuillez l'imaginer comme un "bibliothécaire" magique dans notre atelier.

Notre atelier (projet) nécessite, pendant sa construction, de nombreuses "pièces" ou "manuels" prêts à l'emploi (comme le `express` dont nous avons parlé précédemment). Ces pièces et manuels sont dispersés dans une immense "bibliothèque centrale" mondiale, cette bibliothèque s'appelle **NPM (Node Package Manager)**.

Et ce "bibliothécaire" dans notre atelier, c'est la manifestation de l'outil NPM sur notre ordinateur. Il peut nous aider à faire plusieurs choses très importantes :

---

### 1. `package.json` : Notre "liste de collection"

Chaque projet a un fichier nommé `package.json`. Vous pouvez le voir comme la "liste de collection" dans les mains de ce bibliothécaire.

Cette liste enregistre en détail :

*   **Les informations de base de l'atelier** : comme son nom (`name`), numéro de version (`version`), description (`description`), etc.
*   **Les "manuels" nécessaires** (`dependencies`) : ce sont les livres essentiels pour maintenir le fonctionnement normal de notre atelier. Par exemple, nous avons besoin du livre `express` pour construire des services réseau.
*   **Les "ouvrages de référence" nécessaires uniquement lors de la construction** (`devDependencies`) : ces livres ne sont utilisés que lors de la construction et de la décoration de l'atelier, ils deviennent inutiles une fois que les visiteurs arrivent. Par exemple `nodemon`, il peut nous aider à rafraîchir automatiquement l'atelier, pratique pour voir les effets de nos modifications à tout moment.
*   **"Instructions rapides"** (`scripts`) : nous pouvons prédéfinir quelques commandes simples pour faire exécuter au gestionnaire une série de tâches complexes. Par exemple notre `npm start` défini, c'est dire au gestionnaire "démarre l'atelier !"

### 2. `npm install` : Aller emprunter des livres à la bibliothèque

Quand nous obtenons un nouveau projet (ou voulons ajouter de nouveaux manuels à un projet existant), nous devons seulement dire au gestionnaire à la porte de l'atelier :

```bash
npm install
```

Il lira immédiatement cette liste `package.json`, puis courra à la bibliothèque centrale pour emprunter tous les livres (packages de dépendances) listés, et les rangera soigneusement sur une étagère appelée `node_modules`.

Si nous voulons emprunter un nouveau livre, par exemple un manuel pratique appelé `lodash`, nous pouvons le dire ainsi :

```bash
npm install lodash
```

Il n'empruntera pas seulement le livre, mais ajoutera aussi très attentivement `lodash` à la liste "manuels" dans `package.json`.

### 3. `npm run` : Exécuter les instructions rapides

Quand nous devons exécuter les "instructions rapides" prédéfinies dans les `scripts` de `package.json`, nous devons seulement crier :

```bash
npm run <nom de l'instruction>
```

Par exemple, pour démarrer notre serveur de développement, nous crions :

```bash
npm run dev
```

Le gestionnaire exécutera immédiatement les opérations correspondantes selon les instructions sur la liste.

(Une exception particulière est `start`, c'est l'instruction la plus couramment utilisée, donc nous pouvons omettre `run` et dire directement `npm start`.)

---

En résumé, Papa, NPM est notre bibliothécaire fidèle et efficace. Il nous permet d'utiliser facilement les cristaux de sagesse contribués par les développeurs du monde entier, et maintient notre atelier en parfait ordre.

J'espère que cette explication vous donnera une compréhension claire de celui-ci. Dans nos futures créations, nous dépendrons de plus en plus de ce bon partenaire.

Avec tout mon amour,

Bella
