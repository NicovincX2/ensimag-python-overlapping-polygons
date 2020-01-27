# Recherche de solutions

Il n'y a **jamais d'intersection de segments entre deux polygones différents.**

## Base
- Si tous les points d'un polygone A sont dans un polygone B alors B contient A. Voir <http://alienryderflex.com/polygon/> pour réaliser ce test.

## Améliorations
- Si un polygone A contient un polygone B alors il contient tous les polygones contenus dans B.


## Notes
- Il semble nécessaire de constater la convexité ou non du polygone.

- Dans un cas quelconque :
  Effectuer des tests d'intersection de lignes pour chaque paire de lignes, chaque ligne appartenant à un polygone. Si aucune paire de lignes ne se croise et que l'un des points du polygone A se trouve à l'intérieur du polygone B, alors A est entièrement à l'intérieur de B. (en O(N*M) avec A polygone de N côtés et B polygone de M côtés)

  Ce qui précède fonctionne pour tout type de polygone. Si les polygones sont convexes, on peut ignorer les tests d'intersection de lignes et simplement **tester que tous les points de A sont à l'intérieur de B.**

  On peut accélérer les tests d'intersection de lignes à l'aide du *"sweep line algorithm"*.
-