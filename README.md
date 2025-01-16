для ubuntu
```bash
#проверяем что установлен lsb-release:
apt install lsb-release

#скачиваем sources.list в /etc/apt/sources.list (с заменой):
wget https://raw.githubusercontent.com/Lojaleto/sources/refs/heads/main/ubuntu/sources.list -O /etc/sources.list

#меняем кодовое имя дистрибутива
sed -Ei "s|DIST?|$(lsb_release -cs)|" /etc/apt/sources.list

#обновляем список пакетов, обновляем систему
apt update && apt upgrade -y
```

для debian до 11 включительно:
```bash
#проверяем что установлен lsb-release:
apt install lsb-release

#скачиваем sources.list в /etc/apt/sources.list (с заменой):
wget https://raw.githubusercontent.com/Lojaleto/sources/refs/heads/main/debian/sources.list -O /etc/sources.list

#меняем кодовое имя дистрибутива
sed -Ei "s|DIST?|$(lsb_release -cs)|" /etc/apt/sources.list

#обновляем список пакетов, обновляем систему
apt update && apt upgrade -y
```

для debian 12:
```bash
#скачиваем sources.list в /etc/apt/sources.list (с заменой):
wget https://raw.githubusercontent.com/Lojaleto/sources/refs/heads/main/bookworm/sources.list -O /etc/sources.list

#обновляем список пакетов, обновляем систему
apt update && apt upgrade -y
```
