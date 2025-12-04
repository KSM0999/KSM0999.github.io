---
layout: default
title: cURL cheatsheet
---
# Penetration tester's cURL cheatsheet
## Get request to a HTTP web application

```bash
curl -s -o http://$TARGET/index.html -o output.html -i
```

	-s : silent mode.
	-o : output file path.
	-i : include headers in response.
## Get request to a HTTPS web application

```bash
curl -s -k https://$TARGET/index.html -i
```

	-s : silent mode.
	-k : ignore certificate.
	-i : include headers in response.
## Lance un curl en spécifiant la valeur de certaines en-têtes :

## Get request while specifying 

```bash
curl -H 'Authorization: Basic DS3aYH4fUS=' -H 'Header: true' http://$TARGET/ -i
```
## Lance un curl en requête POST avec des données en suivant toute redirection :

```bash
curl -X POST -L -d 'username=admin&password=admin' http://$TARGET/ -i
```
## Lance un curl en requête GET en spécifiant un cookie :

```bash
curl -b 'PHPSESSID=dsfjdofij4dsifja3uhzd1' http://$TARGET/
```

