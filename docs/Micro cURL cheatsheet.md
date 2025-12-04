---
layout: default
title: cURL cheatsheet
---
# Penetration tester's cURL cheatsheet
## GET request to a HTTP web application

```bash
curl -s -o http://$TARGET/index.html -o output.html -i
```

	-s : silent mode.
	-o : output file path.
	-i : include headers in response.
## GET request to a HTTPS web application

```bash
curl -s -k https://$TARGET/index.html -i
```

	-s : silent mode.
	-k : ignore certificate.
	-i : include headers in response.
## GET request while specifying multiple headers values :

```bash
curl -H 'Authorization: Basic DS3aYH4fUS=' -H 'Header: true' http://$TARGET/ -i
```

	-H : "header name: value"
## POST request specifiying a data content :

```bash
curl -X POST -L -d 'username=admin&password=admin' http://$TARGET/ -i
```
## GET request specifying a cookie :

```bash
curl -b 'PHPSESSID=dsfjdofij4dsifja3uhzd1' http://$TARGET/
```

