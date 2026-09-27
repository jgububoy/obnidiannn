---
aliases:
  - macbook terminal
  - unix brdzanebebi
  - terminal macbook
  - terminal on macbook
  - mac terminal
tags:
  - apple
  - linux
  - Console-Terminal
done: false
created: 2026-01-13
sourse:
---
# terminal keys on macbook

1. `networksetup -getmacaddress en0 ` - wifi **მაკ** მისამართი
2. `networksetup -getmacaddress en1` - ethernet **მაკ** მისამართი
3. 
4. `touch [file_name]` - - - ტექსტური ფაილის ***მხოლოდ ჩექმნა***.
5. `nano [file_name]` - - -  ფაილის შექმნა და თან გახსნა. 
6. `nano ~/file1` ( ან: `~/picture/file.txt` ) - - - დირექტორიას არ იცვლი ისე, ***არსებული ფაილის*** **nano** პროგრამაში ***ფაილის გახსნა***. 
7. `cat [file_path & name]` - - - comand line -ში ტექსტის ***შიგთავსის ნახვა.*** 
8. 
9. `/` - - - ( **სლეში** ), სისტემის უმაღლესი დონე (**Root directory**).  ***მაგ***: `/Users/nika/Documents/file.txt`
10. `~` - - - **( Tilde) :** აღნიშნავს  პირად საქაღალდეს (**Home Directory**). მაგალითად: `~/Documents` იგივეა, რაც `/Users/nika/Documents/file.txt` 
11. `.` - - - **(წერტილი):** აღნიშნავს მიმდინარე საქაღალდეს.
12.  `..` - - - **(ორი წერტილი):** აღნიშნავს ერთი საფეხურით ზედა (მშობელ) საქაღალდეს.
13. 
14. `pwd` - - - (**Print Working Directory**) გიჩვენებთ ზუსტად სად იმყოფებით ახლა.
15. `ls` - - - ( **List** ) გიჩვენებთ, რა ფაილები და საქაღალდეებია მიმდინარე მისამართზე
16. `cd` - - - ( **Change Directory** ) გადაგიყვანთ სასურველ მისამართზე ( მაგ: `cd ~/Desktop`)
17. `clear` ; `ctrl + l` - - - ეკრანის გაწმენდვა
18. 
19. `git log` : 
	- **`q` ღილაკი :** (Quit)  - - - ყველაზე მთავარი. უბრალოდ დააჭირე `q`-ს და მაშინვე დაბრუნდები ტერმინალის ჩვეულებრივ რეჟიმში.
	- **Space (ჰარამხანა) :** - - - გადადის შემდეგ გვერდზე.
	- **ისრები (ზევით/ქვევით) :**  - - - ნელი სქროლვა.
	- **`/` (Slash) :**  - - - თუ რამეს ეძებ ლოგებში, დააჭირე `/`, ჩაწერე სიტყვა და დააჭირე **Enter**.
20. 
21. `echo $SHELL` - - - დეფაულთად რომელი გარემო აყენია. 
22. ` ps -p $$ ` - - - რომელი გარემოა გაშვებული ახლა. 
23. `which zsh` - - - zsh-ის მდებარეობა
24. `chsh -s $(which zsh)` - - - ტერმინალის დეფაულთ გარემო , რომელშც გაიხსნება . ანუ change shell , რომელიც იმყოფება $(which zsh) აქ. 
25. `zsh --version` - - - zsh -ის ვერსია
26. `ifconfig` - - - ip და mac მისამართის გაგება ქსელის ადაპტერის
27. 