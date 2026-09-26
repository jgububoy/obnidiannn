---
aliases:
  - timeshift
tags:
  - linux
  - it
  - Backup
---
# timeshift

### 1. install

To check if Timeshift is already installed in your distribution, search it from the Application launcher and Menu. It usually found under System  Tools.

You can also check it from the terminal by running the following command.

```bash
$ which timeshift
/usr/bin/timeshift
```

If Timeshft is not installed, you can install it like below.

### 1.1 Install Timeshift in Arch Linux

Timeshift is available in AUR, so you can install it using any AUR helper tools such as **[Paru](https://ostechnix.com/how-to-install-paru-aur-helper-in-arch-linux/)** or **[Yay](https://ostechnix.com/yay-found-yet-another-reliable-aur-helper/)** [Yay](Yay.md) like below:

```bash
$ paru -S timeshift
```

Or,

```bash
$ yay -S timeshift
```

If you don't have any AUR helper programs, you can manually install Timeshift by running the following commands:

```bash
$ git clone https://aur.archlinux.org/timeshift.git
$ cd timeshift/
$ makepkg -sri
```
---
<br>

### 1.2 Install Timeshift in Fedora

TImeshift is included in the default repositories of Fedora. To install it on Fedora, run:

```bash
$ sudo dnf install timeshift
```
---
<br>

### 1.3 Install Timeshift in Ubuntu and its derivatives

On Ubuntu and its derivative distributions, you can install Timeshift via its official PPA:

```bash
$ sudo add-apt-repository -y ppa:teejee2008/ppa
$ sudo apt-get update
$ sudo apt-get install timeshift
```



---

<br>

### 2. How to use Timeshift from the command line?

At first, make sure that the timeshift is installed in your system. If not, then install it using `sudo apt install timeshift`

###   [   ](https://dev.to/rahedmir/how-to-use-timeshift-from-command-line-in-linux-1l9b#creating-a-restore-point)  Creating a Restore point

Now, launch your terminal and type the following command

```
sudo timeshift --create --comments "A new backup" --tags D
```

[![Restore Point](https://res.cloudinary.com/practicaldev/image/fetch/s--JHXkw2e0--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/r56r5mely8pxuyaq4a4z.png)](https://res.cloudinary.com/practicaldev/image/fetch/s--JHXkw2e0--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/r56r5mely8pxuyaq4a4z.png)

(Creating a restore point/snapshot may take several minutes, depends on the size of the files & your hardware resources)

```bash
-- comments "A new backup"
```

You can write anything as a comment, it doesn't matter that much. 

```bash
--tags D
```

There are several tags, that specify what kind of backup it is.

As an example

`--tags D` stands for Daily Backup

`--tags W` stands for Weekly Backup

`--tags M` stands for Monthly Backup

`--tags O` stands for On-demand Backup

You can put any tag as your wish, after the comments

###   [   ](https://dev.to/rahedmir/how-to-use-timeshift-from-command-line-in-linux-1l9b#restoring-a-snapshot)  Restoring a snapshot

```bash
sudo timeshift --restore
```

This command shows you a list of created snapshots & ask, from  which snapshot you want to restore the system, you have to select the  snapshot index to proceed further

[![snapshot_list](https://res.cloudinary.com/practicaldev/image/fetch/s--4nQBu9NR--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/9fjqisv0mjmjlnvyk7mw.png)](https://res.cloudinary.com/practicaldev/image/fetch/s--4nQBu9NR--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/9fjqisv0mjmjlnvyk7mw.png)

After that, press the Enter key to continue, when It asks about  reinstalling the GRUB2 bootloader, press the 'y' key, then press the  Enter key again & finally, press the 'y' key to start the system  restore...

[![list_2](https://res.cloudinary.com/practicaldev/image/fetch/s--rgo-FVYT--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/o3mnmo4tdfdb6zhwzm4j.png)](https://res.cloudinary.com/practicaldev/image/fetch/s--rgo-FVYT--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/o3mnmo4tdfdb6zhwzm4j.png)

[![list_3](https://res.cloudinary.com/practicaldev/image/fetch/s--aA-M4LW5--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/xfyaea6tm63ebg47pxu1.png)](https://res.cloudinary.com/practicaldev/image/fetch/s--aA-M4LW5--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://dev-to-uploads.s3.amazonaws.com/i/xfyaea6tm63ebg47pxu1.png)

At this moment, you have restored the system successfully,  and the  PC will take a reboot to ensure that your restoration is fully done.



---

