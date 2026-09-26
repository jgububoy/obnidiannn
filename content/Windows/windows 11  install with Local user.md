---
aliases:
tags:
  - windows
done: false
created: 2026-09-25
sourse:
---
# windows 11 install with Local user

ინსტალაციისას ბევრი სხვადასხავა პრობლემები აქვს ხოლმე. 
აქ მოყრილია ყველა რასაც შევეჩეხე. 

## 1. windows installation encountered an unexpected error 

[FIX 0x80070001 - 0x4002f ERROR CODE \| Windows 11 Installation Problem - YouTube](https://www.youtube.com/watch?v=0GSnpdIZNU8) 

ინსტალაციის პროცესში ***error*** -ს აგდებს ხოლმე...

![[CleanShot 2026-09-26 at 18.24.36@2x.png]]
## 2. windows 11 local user

[Как войти в Windows 11 без учетной записи Microsoft при первом запуске - YouTube](https://www.youtube.com/watch?v=yS-o-PV_EFY)
.
> ზოგადად ამდენი მახინაცია რომ არ გააკეთო, 
> ***რეკომენდირებულია*** :  
> 1. ინსტალაციისას ვაბშე ინტერნეტის კაბელი გამოაძრო
> 2. პროცესში, ეტყვი არ მაქვს ინტერნეტი და დაგაყენებიებს ***ლოკალურ უზერს***. 

.
მიადგები გრაფას შეიყვანე ექაუნთიო . . . 
![](_attachments/80cf38d8079edd2c9855c0dc445c902e.png)
.
1. **კრეფ კლავიატურაზე**:

```shell
shift + F10
```

2. **გამოსულ ტერმინალში შეგავს შემდეგი**: 

```shell
start ms-cxh:localonly
```

3. გამოვა ***ლოკალური უზერის*** შექმნის გრაფა. 

