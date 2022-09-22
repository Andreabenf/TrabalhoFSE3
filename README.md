#Trabalho 3 de fse!

##A esp-idf já se encontra atrelada a este repositório, mas é importante frisar que a mesma ddeve se encontrar na versão v4.4-dev-1254-g639e7ad494

primeiramente:
cclone o repositório
```sh
cd client
 . ../esp-idf/export.sh

idf.py menuconfig

```
No menu, coloque seu wifi


Agora devemos buildar o projeto e inserir na placa
```sh
idf.py build fullclean
idf.py -p /dev/ttyUSB0 erase_flash #importante apagar o que tiver na placa!
idf.py -p /dev/ttyUSB0 flash monitor
```

