---
aliases:
tags:
  - apple
done: false
created: 2026-09-25
sourse:
---
# Create New File on finder

## txt file

ერთხელ დააყენოთ "**სწრაფი მოქმედება / Quick Action (Быстрое действие)** ", რომელიც **კონტექსტურ მენიუში** (მარჯვენა ღილაკზე) გაჩნდება:

1. გახსენით პროგრამა ***Automator*** ( მოძებნეთ Spotlight-ში ).
2. აირჩიეთ ***Quick Action (Быстрое действие)**.*
3. ზედა მენიუში, სადაც წერია ***"Workflow receives current (Процесс получает текущее)"***, აირჩიეთ ***files or folders(файлы ან папки),*** ხოლო "**in**" ველში — ***Finder***.
4. მარცხენა სიაში მოძებნეთ ***Run AppleScript(ыполнить AppleScript.)*** და გადმოიტანეთ **მარჯვენა** სამუშაო არეში.
5. ჩაწერეთ შემდეგი **კოდი** არსებულის ნაცვლად:

> ***AppleScript***: კოდში სინამდვილეშ **AppleScript** - ია და არა **Bash**. ობსიდიანი არ კითხულობს ალბათ და მაგიტო.

```shell
tell application "Finder"
    set selection_folder to (folder of the front window) as alias
    make new file at selection_folder with properties {name:"untitled.txt"}
end tell
```

6. შეინახეთ სახელით: **"Create New Text File"**.

ახლა ნებისმიერ საქაღალდეში მარჯვენა ღილაკით დაჭერისას, მენიუში **Быстрые действия** (Quick Actions)  (ან პირდაპირ სიის ბოლოში) დაინახავთ ამ ბრძანებას. 

> macOS აქვს ერთ-ერთი ***უცნაურობა***: **Quick Actions** (Быстрые действия) კონტექსტურ მენიუში მხოლოდ მაშინ ჩნდება, როცა რაღაც ობიექტი (ფაილი ან საქაღალდე) უკვე მონიშნულია. ცარიელ ადგილზე დაჭერისას სისტემა თვლის, რომ „მოქმედება“ არაფერზეა შესასრულებელი.

## Markdown file

ყველაფერი იგივე რაც ზემოთ, უბრალოდ **კოდი** არის სხვა ჩასაწერი : 

```shell
tell application "Finder"
	try
		set currentFolder to (folder of the front window) as alias
	on error
		set currentFolder to (path to desktop folder) as alias
	end try
	
	set fileName to "NewDocument.md"
	set newFile to make new file at currentFolder with properties {name:fileName}
	select newFile
end tell
```

