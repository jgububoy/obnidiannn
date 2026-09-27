---
aliases:
  - mac terminal
  - mac zsh
  - mac oh my zsh
tags:
  - apple
  - Console-Terminal
  - Bash_ZSH
done: false
created: 2026-01-16
sourse:
---
# macbook terminal customisations

[GitHub - mahenzon/how-to-pretty-zsh](https://github.com/mahenzon/how-to-pretty-zsh?tab=readme-ov-file)  

![Как сделать красивый терминал? Oh My ZSH! - YouTube](https://www.youtube.com/watch?v=9tnwovsybWg) 
.

 
1. `echo $SHELL` - - - დეფაულთად რომელი გარემო აყენია. 
2. ` ps -p $$ ` - - - რომელი გარემოა გაშვებული ახლა. 
3. `which zsh` - - - zsh-ის მდებარეობა
4. `chsh -s $(which zsh)` - - - ტერმინალის დეფაულთ გარემო , რომელშც გაიხსნება . ანუ change shell , რომელიც იმყოფება $(which zsh) აქ. 
5. `zsh --version` - - - zsh -ის ვერსია


`/home/user/.zshrc` - - - oy my zsh -ის **კონფიგურაციის ფაილი,** მისი დაინსტალირების მერე შექმნილი. 


#### კარგი ***plugins* სია:** 

1. `z`  - - - განახებს საქაღალდეებს სადაც სადაც იყავი . (o my zsh -ში ჩაშენებულია, ჩაწერა უნდა მხოლოდ)
2. `git` 
3. `zsh-autosuggestions` (გარე წყაროდანაა, დასაყენებელია) - - -  გიჩვენებს ბრძანების აკრეფისას , სავარაუდო ვარიანტს. 
	- [GitHub - zsh-users/zsh-autosuggestions: Fish-like autosuggestions for zsh](https://github.com/zsh-users/zsh-autosuggestions?tab=readme-ov-file) ; 
	- [22:16 - YouTube](https://www.youtube.com/watch?v=9tnwovsybWg) ; 
4. `zsh-syntax-highlighting` - - -  სინტაქსის ფერების მხარდაჭერა.  ცოტა სხვანაირი დასაყენებელია და თავისი თემა უნდა .
	- [GitHub - zsh-users/zsh-syntax-highlighting: Fish shell like syntax highlighting for Zsh.](https://github.com/zsh-users/zsh-syntax-highlighting) 
	- [26:00 - YouTube](https://www.youtube.com/watch?v=9tnwovsybWg) 