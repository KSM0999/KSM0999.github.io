---
layout: default
title: cURL cheatsheet
---
Lance un curl vers une application HTTP et imprime la sortie dans output.html :

```bash
curl -s -o http://$TARGET/index.html -o output.html -i
```

	-s : silent mode, garde seulement en sortie la réponse à la requête, pas les messages d'erreurs ou les informations de progression
	-o : chemin ou nom du fichier d'output.
	-i : inclure les headers de la réponse dans l'output et pas seulement le contenu.

Lance un curl vers une application HTTPS en ignorant les certificats :

```bash
curl -s -k https://$TARGET/index.html -i
```

Lance un curl en spécifiant la valeur de certaines en-têtes :

```bash
curl -H 'Authorization: Basic DS3aYH4fUS=' -H 'Header: true' http://$TARGET/ -i
```

Lance un curl en requête POST avec des données en suivant toute redirection :

```bash
curl -X POST -L -d 'username=admin&password=admin' http://$TARGET/ -i
```

Lance un curl en requête GET en spécifiant un cookie :

```bash
curl -b 'PHPSESSID=dsfjdofij4dsifja3uhzd1' http://$TARGET/
```

