komendy:
- ip a
- cat /etc/resolv.conf
- ping
- ifup
- ifdown

- yum install git (dla centos)
- git clone
- python httpchat.py

- curl -X POST -d '{"text":"hello world"}' http://10.0.5.5:8888/chat
- yum install curl

- systemctl stop firewalld

---
---


Ustawianie parametrów sieci
---------------------------

![alt text][network]

[network]: ./network.png "Logo Title Text 2"

1. na 1 z komputerów zainstaluj oprogramowanie ``http-chat`` dostępne pod adresem ``https://github.com/jkanclerz/http-chat``

Wejściowe parametry sieci
-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  | 10.0.5.5 | |
| MASKA  | 255.255.255.0 | |
|   |  | |
| PC 2  |  | |
| IP - address  | 10.0.5.4 | |
| MASKA  | 255.255.255.0 | |

Weryfikacja połączenia

Polecenie -> ping

Efekt -> działa


Statyczna konfiguracja parametrów połączenia
Wejściowe parametry sieci
-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  | 192.168.10.10 | |
| MASKA  | 255.255.255.0 | |
|   |  | |
| PC 2  |  | |
| IP - address  | 172.16.100.100 | |
| MASKA  | 255.255.0.0 | |

Weryfikacja połączenia

Polecenie -> ping


Efekt -> nie działa


Nowa statyczna konfiguracja 
-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  | 172.16.100.10 | |
| MASKA  | 255.255.255.0 | |
|   |  | |
| PC 2  |  | |
| IP - address  | 172.16.100.20 | |
| MASKA  | 255.255.255.0 | |

Weryfikacja połączenia

Polecenie -> ping


Efekt -> działa


Warto wiedzieć
--------------

-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
| Lokalizacja pliku z konfiguracją sieci| /etc/resolv.conf | |
| UP -> Wyłączenie interfejsu sieciowego| ifup | |
| DOWN -> Włączenie interfejsu sieciowego| ifdown | |
| Sprawdzenie obecnych parametrów | | |
| lista wszystkich interfejsów | | |
| Które interfejsy jakie porty słuchają | | |
