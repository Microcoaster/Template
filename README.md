<div align="center">

<img src="docs/banniere.png" alt="[NOM DU MODULE]" width="100%">

</div>

[Une phrase qui dit ce que fait le module, concrètement. Pas « module de gestion de X », mais ce qui bouge, ce qui s'allume, ce qui est mesuré.]

[Un paragraphe sur le principe : quelle pièce mécanique est pilotée, par quel composant, et ce qui déclenche l'action.]

Comme les autres modules, il se configure au premier démarrage par portail captif, puis rejoint le serveur en WebSocket.

**Version [0.1.0]**

## Principe

[Expliquer la logique, pas la liste des fonctions. Si le module a une machine à états, la montrer.]

```
ETAT_A       ce qui est vrai dans cet état
ETAT_B       ce qui déclenche le passage ici
ETAT_FAULT   ce qui l'a provoqué
```

## Sécurité

[Ce qui arrive si la liaison tombe, si un capteur ment, si un ordre se perd. Quel est l'état sûr, et pourquoi c'est celui-là.]

[Quelles bornes locales protègent le matériel : durée maximale, seuil de courant, délai de garde.]

## Matériel

| Élément | Broche | Rôle |
|:--|:--|:--|
| [Composant] | GPIO [n] | [Ce qu'il fait] |

## Réglages

| Paramètre | Effet |
|:--|:--|
| `[PARAMETRE_MS]` | [Ce que ça change quand on l'augmente ou le diminue] |

## Compiler et téléverser

Nécessite [PlatformIO](https://platformio.org/) dans Visual Studio Code.

```bash
pio run                  # compilation
pio run -t upload        # téléversement du firmware
pio run -t uploadfs      # téléversement du portail vers LittleFS
pio device monitor       # console série, 115200 bauds
```

## Première mise en service

1. Alimenter le module. Il crée un point d'accès WiFi.
2. S'y connecter et ouvrir `http://192.168.4.1`.
3. Renseigner le réseau de destination.
4. Le module redémarre, rejoint le réseau et s'annonce auprès du serveur.

Les identifiants WiFi restent en mémoire du module, jamais dans le dépôt.

## État

[Ce qui marche, ce qui reste à écrire. Être franc : un dépôt qui annonce plus qu'il ne fait finit par se retourner contre son auteur.]

---

<sub>MicroCoaster · Auteurs : [AUTEURS]</sub>
