## Exercising *spring-boot-gridfs* with [curl](https://curl.haxx.se/ "curl Homepage")
---
### Storing files into GridFS.
Store the file `Joker.png` using curl's **-F** option to initiate a multi-part binary POST of the image file.
```bash
$ curl -F file=@Joker.png http://localhost:8080/files
```
### List existing files stored in GridFS
```bash
$ curl http://localhost:8080/files
```
Response: 
```json
["Joker.png"]
```
### Retrieve file from GridFS
Retrieve the file `Joker.png` from GridFS and store it on the local file system as file `Joker.new.png`.
```bash
$ curl -o Joker.new.png  http://localhost:8080/files/Joker.png
```
