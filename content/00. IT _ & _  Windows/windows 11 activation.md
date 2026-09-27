---
aliases:
  - წინდოწს აქტივაცია
  - ვინდოუს აკტივაცია
  - ვინდოუს აქტივაცია
  - windows aktivacia
  - windows aqtivacia
  - windows aqtivation
  - ვინდოუსის აქტივაცია
tags:
  - windows
done: false
created: 2026-03-30
sourse:
---
# windows 11 activation

### 1. ( გასატესტია )
ინტერნეტი უნდა იყოს ჩართლი: 

**powershell**: 

მგონი ეს ***LTS*** ვერსია **windows** -ში ააქტიურებს. მეორე მოთო  დმა ავ ვერსიაში არ იმუშავა, 

[Чистая Windows без мусора: 12:50 -  13:15 - YouTube](https://www.youtube.com/watch?v=YkkoSUIKrPU) 

```powershell
irm https://get.activated.win | iex
შემდეგ ვაჭერთ თანმიმდევრობით: ( ასარჩევი იქნება რა გინდა რომ გააკეთო... )
1
enter
0
```

### 2.  ( გატესტილია )
ინტერნეტი უნდა იყოს ჩართლი: 

run **CMD** by administrator:

```powershell
slmgr /ipk  W269N-WFGWX-YVC9B-4J6C9-T83GX
slmgr /skms kms8.msguides.com
slmgr /ato
```



