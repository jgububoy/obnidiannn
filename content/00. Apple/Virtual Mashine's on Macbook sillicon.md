---
aliases:
  - virtualbox on mac
  - virtualmashine macbook
  - virtualbox on macbook
  - windows on mac
  - ვირტუალური მანქანები
  - paralels desktop
  - parallels desktop
tags:
  - apple
  - virtulization
done: false
created: 2026-02-12
sourse:
---
# Virtual Mashine's on Macbook sillicon

## 1. Parallels desktop

[Parallels desktop on Mac](Parallels%20desktop%20on%20Mac.md) 

პრაქტიკამ აჩვენა რომ  apple silicon-ზე **ყველაზე კარგად ეს ვირტუალური მანქანა მუშაობს**. 

>ესეც როგორ სხვა ყველა ვირტუალური მანქანები, რომლებსაც ვაყენებს silicon პროცესორებზე, მათში შემდგომ ARM ვერსია იმიჯების გამოყენება ჯობია. რადგანაც ზოგიერთ ვირტუალურ მანქანაში ან არეშვება , ან  თუ ეშვება წესიერად არ მუშაობს. 
 ***მოკლედ***: 
   macbook silicon -ზე ჯობია ARM -თვის განკუთვნილი იმიჯების გამოყენება. 

.
1. [Как запустить Windows на Mac M1/M2/M3/M4 Apple Silicon / How to install Windows or Linux on MacBook - YouTube](https://www.youtube.com/watch?v=iMyve4UIsIs) 
2. [Windows 11 на MacBook M1. Как сделать виртуальную машину на Parallels - YouTube](https://www.youtube.com/watch?v=8mwXS33UVUA) 
3. [Как установить Windows 10 на Mac с чипом M1 (Apple Silicon). О Windows 10 на ARM и проблемах - YouTube](https://www.youtube.com/watch?v=IR-iD_db14Q) 
4. [Parallels Desktop — ЛУЧШИЙ способ запустить Windows на Mac! БОЛЬШОЙ разбор от А до Я 2026 - YouTube](https://www.youtube.com/watch?v=iqZNK-G4alg) 
5. 

## 2. ვირტუალური მანქანა - VMware Fusion : 

> ცუდი არაა, კარგიცაა შეიძლება ითქვას. მაგრამ ***Parallels desktop*** მაინც ყველას ჯობია, 

1. [Установка Windows 11 на VMware Fusion в macOS (Apple M2 Pro). - YouTube](https://www.youtube.com/watch?v=MaZGrmEv3Rs&t=287s) 

2. ვირტუალირ მანქანის გამზადების შემდეგ , როდესაც **windows** -ის ინსტალაციას დაიწყებ, პროცესში ***თუ  ქსელის დრაივერი არაა*** ,  უშვებ შემდეგ ბრძანებას, რომ გაგატაროს ამ ეტაპზე და მერე დააყენო დრაივერი :  [Offline Install Fix (No Network Internet) M1 Mac](https://www.youtube.com/watch?v=Ub3gHDBQuAI) 

	1. ***fnKEY + shift + f10*** 
	2. და შედგყავს :  ` oobe\bypassnro `

ამ პროცესის შემდეგ, გადაიტვირთება და ისევ რომ მოვა აქამდე ეუბენბი ***არ მაქვს ინტერნეტი*** და აგძელებს. 
რომ ჩაიწერება სისტემა, ***VMware tool***-ს აინსტალირებ **menu ზოლიდან** [Установка Windows 11 - 12:50  - YouTube](https://www.youtube.com/watch?v=MaZGrmEv3Rs&t=287s) . 
სისტემა გადატვირთვას მოითხოვს. ჩაირთვება და ინტერნეტიც მოდის. 

ასევე  **VMware** - ს აქვს ***snapshot***-ებიც. : [snapshot_22:30 - YouTube](https://www.youtube.com/watch?v=MaZGrmEv3Rs&t=287s) 


VMware HotKey : 
1. ***ctrl + cmd + F***  - - - full screen
2. ***Ctrl + Shift + M*** - - - show/hide the VMware Fusion menu bar while in full-screen mode.


## 3. ვირტუალური მანქანა - UTM

> ***UTM*** ვირტუალური მანქანის გამოყენება არ ღირს. ოპტიმიზირებულია  და **ლეპტოპს ძან ახურებს** და **ელემენტსაც ძან სწრაფად აჯენს**
> ამას ***VMware Fusion***  ბევრად ჯობია ყველაფრით. 

1. [Как запустить Windows на Mac M1/M2/M3/M4 Apple Silicon / How to install Windows or Linux on MacBook - YouTube](https://www.youtube.com/watch?v=V0_ehi3JhBQ&t=1s) 
2. [How to Run Windows Server 2022 on Mac M chips with UTM! - YouTube](https://www.youtube.com/watch?v=gHpSZ-1eO3w) 

### UTM იმიჯების ლოკაციის შეცვლა: 

**UTM** -ში ვირტუალური მანქანების (იმიჯების) მდებარეობის შეცვლა სტანდარტული "**Settings**" მენიუდან პირდაპირ არ ხდება, თუმცა ამის გაკეთება მარტივად შეიძლება ფაილების გადაადგილებით.

აი, როგორ უნდა მოიქცეთ:

#### 1. ფაილების ლოკაციის ნახვა

ნაგულისხმევად, **UTM** ინახავს `.utm` პაკეტებს შემდეგ მისამართზე : `~/Library/Containers/com.utmapp.UTM/Data/Documents/`

#### 2. იმიჯების გადატანა ( ფაილი გადაგაქვს move -ით )

1. **გათიშეთ UTM** სრულად.
2. გახსენით **Finder** და დააჭირეთ `Command + Shift + G`.
3. ჩაწერეთ ზემოთ მოცემული მისამართი: `~/Library/Containers/com.utmapp.UTM/Data/Documents/`.
4. აქ დაგხვდებათ თქვენი ვირტუალური მანქანები (`.utm` გაფართოებით). **გადაიტანეთ (Move)** სასურველი ფაილი ახალ ადგილას (მაგალითად, გარე მყარ დისკზე ან სხვა საქაღალდეში).
5. გადატანის შემდეგ, უბრალოდ **ორჯერ დააწკაპუნეთ (Double-click)** გადატანილ `.utm` ფაილს.

ამ მოქმედებით UTM ავტომატურად დაამატებს ვირტუალურ მანქანას სიაში ახალი მისამართიდან.

---

#### მნიშვნელოვანი ნიუანსები:

- **გარე დისკის ფორმატი:** თუ იმიჯს გარე მყარ დისკზე გადაიტანთ, დარწმუნდით, რომ დისკი დაფორმატებულია **APFS** ან **Mac OS Extended** სისტემაში. `ExFAT`-ზე შესაძლოა წარმადობის ან ფაილის ზომის პრობლემები შეგექმნათ (რადგან ვირტუალური დისკები ხშირად დიდია).
    
- **ფაილების იმპორტი:** ასევე შეგიძლიათ UTM-ის მთავარ ფანჯარაში დააჭიროთ **"+"** ღილაკს, აირჩიოთ **"Open..."** და მიუთითოთ იმ ფაილის ახალი მდებარეობა.


## 4. VirtualBOX

[How to Install Windows 11 on Mac (M1, M2, M3, M4) // Run Windows 11 on Apple Silicon W/ VirtualBOX - YouTube](https://www.youtube.com/watch?v=yW0nYwgeWJs)

რეალურად არ გამიტესტავს და არ ჩამიწერია. ვიყენებ ***Parallels desktops***. 

