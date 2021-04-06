# alarex_infra
alarex infra repository

bastion_IP = 84.252.131.121
someinternalhost_IP = 10.129.0.9

## HW04 Cloud bastion

### Подключение в одну строку

`ssh  -J appuser@84.252.131.121 appuser@10.129.0.9`

### Подключение по алиасу
В конфиг ~/.ssh/config добавить

```
Host someinternalhost
  Hostname 10.129.0.9
  User appuser
  ProxyJump appuser@84.252.131.121
```
