---
aliases:
tags:
  - manjaro
  - gnome
  - fedora
  - it
  - linux
  - ubuntu
done: false
created: 2025-05-27
sourse:
---
# 1. Gnome Extensions

[Расширения GNOME, о которых ТЫ НЕ ЗНАЛ (наверное) - YouTube](https://www.youtube.com/watch?v=l9h874zxHbQ)   - - - ***კარგია, გასარჩევია***.

1. **გაფართოებები: ( Extensions )**
   https://extensions.gnome.org/
   https://www.youtube.com/watch?v=1KCPh8W-6zs
2. **Appfolders Management extension**   - Помогает организо
вать иконки в меню приложений Gnome 3 и рассортировать их по папкам ( dzvel versiebshi )
3. ფანჯრების ჩაკეცვა/გახსნა   -  `gsettings set org.gnome.shell.extensions.dash-to-dock click-action 'minimize'`
4. **Arc Menu**  - - -  Красивое меню для GNome 3 (Сочетает в себе меню приложений и расширение Места)
5. **Caffeine**  - - -    не даст заснуть десктопу пока расширение активно
6. **Coverflow Alt-Tab** - - -  Красивое листание окон с помощью комбинации клавиш Alt-Tab
7. **Dash to Dock**  - - -   Красивый нижний бар для иконок приложений, с достаточно гибкими настройками
8. **dash to panel** - - -   ზედა პანელის ქვემოთ ჩამოწევა  ( windows-ის menubar-ზე დამსგავსება )
   7.1   **Icon Area Horizontal Spacing**     -   Уменьшает растояние между иконками მარცხენა   
   7.2   **Status Area Horizontal Spacing**   -   მარჯვენა
9. **Removable Drive Menu**        -    Безопасное извлечение USB-накопителей
10. **Sound Settings**              -    создает отдельную иконку, быстрого доступа к настройкам звука, в правом верхнем углу бара
11. **Sound Input & Output Device Chooser**  -   Добавляет возможность выбора между подключенной переферией (колонки и микрофон)в верхнем правом меню
12. **User Themes**. - - - -  Дает возможность добавлять пользовательские темы
13. **No Topleft Hot Corner**       -
14. **extensions** - - -  გაფართოებების ჩამონათვალი ზედა ზოლში
15. **frippery moveclock**   - - - - საათის მარჯვენა მხარეს გადაწევა
16. **Dynamic Panel Transparency**  - - - ფანჯრების დაპატარავებისას ზედა პანელი გამჭვირვალეა.full რეჯიმში პანელი მუქდება
17. **blur my shell**   - - - 
18. **compiz windows effect**       --   ფანჯრების გადაადგილების ეფექტი
19. **panel OSD**   - - -   შეტყობინებების ფანჯრის რედაქტირება
20. **panel scroll**    - - - 
21. **Vitals**   -  სისტემის მონიტორინგი
22. **AppIndicator and KStatusNotifierItem Support** - ზედა ზოლში ტრეის დამატება
23. **maximaze to empty workspace** - ფანჯრის გადიდებისას ავტომატურად გადადის ახალ გვერდზე, gnome 40- დან 
24. **Gesture improvements** - ჟესტების დამატებითი ფუნქციები gnome 40- დან
	1. 4-finger gestures for overview navigation - **OFF
	2. 4-finger gestures for workspace switching - **OFF
	3. Window swwitching - **ON
	4. Window manipulation - **ON
	5. Minimize Window - **OFF
25. **just perfection** - დამატებით ფუნქციების ჩამონათვალი
26. **sound input & output device chooser** - 
27. **Desktop Icons NG (DING)** -  desktop-ის გამოყენება (ფაილების დამატება)
28. 
----------------------------------------------------------------------
...
- სისტემის ინფო ტერმინალში
```bash
sudo apt install screenfetch
```
---------------------------------------------------------------------

- ფაილების წინასწარი ნახვა, გახსნის გარეშე ( როგორც MAC-ში ):
```bash
sudo apt-get install gnome-sushi
```
---------------------------------------------------------

-  ulauncher

```bash
pamac build ulauncher
```

# Fedora gnome

`version: fedora 36Beta, gnome 42.`

_შენიშვნა:_    **rpm fusion** და **flethub** სხვადასხვაა.

**dnf install** ... ოფიციალური რეპოზიტორიიდან აყენებს
**flatpak install** ... უშუალოდ flatpak ფაილებს აყენებს.
<br>

-   **sudo nano /etc/fstab**
    -   **compress=zstd:1** -ის მერე ვამატებთ `,defaults,noatime,discard=async` შემდეგი დანაყოფებისათვის **/, /home, /var/log**
-   **Optimize DNF Config**
    1.  sudo nano /etc/dnf/dnf.conf
        1.  fastestmirror=True
        2.  max_parallel_downloads=10
        3.  defaultyes=True
-   **სარკეების განახლება**:
    1.  sudo dnf autoremove
    2.  sudo dnf clean all
-   **System Update**
    1.  sudo dnf upgrade --refresh
-   **sudo dnf install timeshift**
-   RPM fusion: [link](https://docs.fedoraproject.org/en-US/quick-docs/setup_rpmfusion/) 
-   Installing plugins movies and music: [link](https://docs.fedoraproject.org/en-US/quick-docs/assembly_installing-plugins-for-playing-movies-and-music/)  
```bash
sudo dnf install gstreamer1-plugins-{bad-*,good-*,base} gstreamer1-plugin-openh264 gstreamer1-libav --exclude=gstreamer1-plugins-bad-free-devel
sudo dnf install lame* --exclude=lame-devel
sudo dnf group upgrade --with-optional Multimedia
```
-   instal FLATHUB :
    1.  [https://flathub.org/home](https://flathub.org/home) ან
    2.  sudo dnf install -y flatpak      (მაგრამ მაინც ითხოვს ბრაუზერიდან ინსტალაციას. ჯერ ალბათ ბაგია)
-   Installing Media Codecs: [link](https://docs.fedoraproject.org/en-US/quick-docs/assembly_installing-plugins-for-playing-movies-and-music/)
```bash
sudo dnf groupupdate multimedia --setop="install_weak_deps=False" --exclude=PackageKit-gstreamer-plugin
sudo dnf groupupdate sound-and-video
```
-   **gnome-tweaks**, *_extentions *_...
-   sudo dnf install gnome-shell-extension-dash-to-dock

### Сочетание клавиш для запуска терминала в Fedora (Gnome)
```bash
1. Зайти в Настройки > Устройства > Клавиатура > "+" (добавить сочетание клавиш).
2. Название: Terminal
3. Команда: gnome-terminal --profile=Default --geometry=95x35+250+60
4. Сочетание клавиш: Ctrl + Alt + T (как в Ubuntu).
```

