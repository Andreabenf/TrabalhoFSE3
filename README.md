## Trabalho 3 de Fundamento de Sistemas Embarcados

**Nome** | **Matricula** | **GitHub** 
---------|:-------------:|:----------:
André Aben-Athar de Freitas | 170056155 | Andreabenf
Lucas Ganda Carvalho| 170039668 | lucasgandac

## Descrição
Esse trabalho é um projeto constituído por uma ESP32 conectada à Wi-fi por protocolo MQTT que permite o controle e visualização dos dados de sensores.

No nosso projeto está implementado a leitura e controle de um sensor de temperatura, um de umidade, um LED PWM e o modo bateria/energia.

## Execução

*Obs* : A esp-idf já se encontra atrelada a este repositório, mas é importante frisar que a mesma deve se encontrar na versão v4.4-dev-1254-g639e7ad494

1. Clone o repositório e entra na pasta :
```sh
cd client

```
2. Execute o export
```

 . ../esp-idf/export.sh
```
3. Rode o menuconfig
```
idf.py menuconfig

```

4. No menu, coloque seu wifi


5. Agora build o projeto e insira-o na placa
```
idf.py build fullclean
idf.py -p /dev/ttyUSB0 erase_flash #importante apagar o que tiver na placa!
idf.py -p /dev/ttyUSB0 flash monitor
```

