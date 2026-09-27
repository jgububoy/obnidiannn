# ssh comands

#### გასაღების გენერირება: 

- `ls -al ~/.ssh` - - - ***ადგილმდებარეობა***
- `ssh-keygen -t ed25519 -C "comment"` - - - ***ახალი გასაღების გენერირება*** (coment-მაილია ზოგადად) 
- `ssh-keygen -t ed25519 -f ~/.ssh/key2 -C "comment"` - - - შეიქმნება ახალი **ssh ფაილები** ( არსებულს, **ძველს არ წაშლის** ) სახელად ამ შემთხვევაში_ **Key2**. რომელიც განთავსებული იქნება `~/.ssh/` მისამართზე.

აქვე: 
- `ssh server_username@server_ip` - - - ***სერვერზე შესვლა*** 

#### SSH Agent 

- `eval "$(ssh-agent -s)"` - - - Agent-ის გაშვება. 
- `ssh-add ~/.ssh/id_ed25519` - - - ***id_ed25519***  გასაღების დამატება **Agent**-ში
- `ssh-add -l` - - -  - -  დამატებული გასაღებების ნახვა

#### OpenSSH Server -ის გამართვა

- `sudo apt update && sudo apt install -y openssh-server` -  -  - OpenSSH-Server -ის **ინსტალაცია**
- `sudo systemctl enable --now ssh` - - - ჩართვა/ავტომატური გაშვება 
- `sudo systemctl status ssh` - - - **სტატუსის შემოწმება**: ( უნდა იყოს:  `active (running)` )
- `sudo ufw allow ssh` - - - ***ფაირვოლი***: ( საჭიროების შემთხვევაში პორტის გასახსნელად )
- `sudo systemctl disable --now ssh` - - - სერვერის დაუყოვნებლივ **გათიშვა** და ავტომატური გაშვების გამორთვა

##### ***macOS*** -ზე : 

- `sudo launchctl disable system/com.openssh.sshd ` - - - server-ის დაუყონებლივ **გათიშვა**
- `sudo launchctl stop com.openssh.sshd` - - - server-ის დაუყონებლივ **გათიშვა**. 
- `sudo launchctl list | grep ssh` - - - შემოწმება

#### public key-ის ატვირთვა და *სერვერზე შესვლა*: 

- `ssh-copy-id server_username@server_ip` - - - public key-ის ***ატვირთვა სერვერზე***.
	- **server_username** - - - სერვერის უზერი, ***რომელზეც გვინდა დაკავშირება***.
	- **server_ip** - - - სერვერის IP მისამართი. 
- `ssh server_username@server_ip` - - - ***სერვერზე შესვლა*** (მაგ: **ssh vm@192.168.100.15**  )

#### SSH სესიის დასრულება

* `logout` - - - აკრიფო ბრძანება, ან
* `Ctrl + D` - - - კლავიატურის კომბინაცია.
