#arch , #manjaro , #linux  
# Snap on ARCH

### Установка

[Установите](https://wiki.archlinux.org/title/Установите) [snapd](https://aur.archlinux.org/packages/snapd/)AUR или его [git](https://wiki.archlinux.org/title/Git) версию, [snapd-git](https://aur.archlinux.org/packages/snapd-git/)AUR.

В пакет входит `snapd` демон,  а также *snap-confine*, который обеспечивает монтирование, изоляцию и запуск snap-**пакетов**.

**Совет:** `snapd` устанавливает скрипт в `/etc/profile.d/` для экспорта путей в исполняемым файлам, входящим в snap-пакеты. Для  того чтобы эти изменения вступили в силу потребуется перезагрузка.


### Настройка

В пакет также входят несколько [systemd](https://wiki.archlinux.org/title/Systemd_(Русский)) unit файлов, которые обеспечивают возможность обновления всех установленных snap-пакетов, при выходе новой версии.

Для того чтобы `snapd` демон запускался, когда *snap* обращается к нему, запустите  `snapd.socket`.

```bash
systemctl start snapd.socket
```

Вы также можете активировать его при старте системы.

```bash
systemctl enable snapd.socket
```

Для того чтобы автоматически обновлять пакеты активируйте `snapd.refresh.timer`:

```bash
systemctl start snapd.refresh.timer
```



### Управление snap-пакетами

Для управления пакетами используется утилита *snap*.

#### Поиск

Для поиска пакетов, доступных для установки используйте команду *find*:

```bash
snap find
```

Это выведет список всех доступных пакетов. Для поиска конкретного пакета используйте:

```bash
snap find критерий_поиска
```

#### Установка пакетов

Установить snap-пакет можно с помощью команды:

```bash
snap install имя_пакета
```

Установка требует root привилегий. Установка с правами пользователя  на данный момент невозможна. При установке snap загружается в `/var/lib/snapd/snaps` и монтируется в `/snap/*имя_пакета*`.

Кроме того, создаются также юнит-файлы для каждого snap-пакета и добавляются в ` /etc/systemd/system/multi-user.target.wants/`, для того чтобы snap-пакеты монтировались при каждом запуске системы. Вы можете просмотреть список установленных пакетов командой:

```bash
snap list
```

Вы также можете устанавливать **snap-пакеты локально,** с жесткого диска: 

```bash
snap install --devmode /path/to/snap
```



#### Обновление пакетов

Для того чтобы обновить snap-пакеты выполните:

```bash
snap refresh
```

#### Удаление пакетов

Для того чтобы удалить пакет выполните:

```bash
snap remove snapname
```

#### Удаление

Удаление пакета [snapd](https://aur.archlinux.org/packages/snapd/)AUR не приводит к удалению всех каталогов и файлов, которые создаются при  его использовании. Лучше всего удалить все snap-пакеты с помощью *snap remove*, перед тем как удалять сам пакет. Однако, на данный момент невозможно удалить snap-пакет *ubuntu-core*. Для того чтобы полностью удалить все файлы следуйте инструкции ниже.

1. Отмонтируйте все активные snap-пакеты из `/snap`.  

```bash
umount $(mount | grep snap | awk '{print $3}')
```

2. Удалите следующие каталоги:

```bash
rm -rf /var/lib/snapd
rm -rf /snap
```

3. Удалите все файлы, отвечающие за монтирование snap-пакетов из `/var/lib/snapd/snaps` в `/snap` при загрузке.

```bash
find /etc/systemd/system -name "snap-*.mount" -delete
find /etc/systemd/system -name "snap.*.service" -delete
find /etc/systemd/system/multi-user.target.wants -name "snap-*.mount" -delete
find /etc/systemd/system/multi-user.target.wants -name "snap.*.service" -delete
```

## 

## Советы и рекомендации

### Classic snaps

Some snaps (e.g. Skype and Pycharm) use classic confinement. However, classic confinement requires the `/snap` directory, which is not FHS-compliant. Therefore, the snapd package  does not ship this directory. However, if the user wants to, he can  manually create a symlink from `/snap` to `/var/lib/snapd/snap`, to allow the installation of classic snaps:

```
# ln -s /var/lib/snapd/snap /snap
```