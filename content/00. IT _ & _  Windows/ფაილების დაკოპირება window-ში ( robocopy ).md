---
aliases:
  - რობოკოპი
  - robocopy
tags:
  - bat_file
  - it
done: false
created: 2025-04-26
sourse:
---
# ფაილების დაკოპირება window-ში

[Robocopy \| Microsoft Learn](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/robocopy) 

**bat** ფაილში:

```bash
robocopy Destination-A Destination-B /e /purge
robocopy Destination-A Destination-B /e       - - -    ( როგორც ჩვეულებრივი კოპირება )
.
"Destination-A"   - - - მისამართის ასე ბრჭყალებში ჩასმა,  პრაბელის პრობლემას აგვარებს 
```

***/e*** - ***ჩვეულებრივი კოპირებაა***.( **იგივე სახელის ფაილებს გადააწერს**, რაც იყო იმას უხლებელს ტოვებს ). **აკოპირებს** ყველა კატალოგს, ცარიელების ჩათვლით. და **Destination-B** -ში **რაც მანამდე იყო *არ შლის***. ანუ ***ამატებს ახალ ფაილებს***.

***/purge*** - **Destination-B**-ში ყველაფერს **შლის** რაც არ არის **Destination-A** -ში. გამოიყენება "***/e***" -სთან ერთად და ამიტო იგივე ფაილებს ხელახლა არ აკოპირებს. 

---

***სერვერზე ატვირთვისას*** რაღაც პრობლემები იყო და AI-იმ ეს მირჩია: 

`/E /R:2 /W:5 /V /TS /FP`

```bash
robocopy Destination-A Destination-B /E /R:2 /W:5 /V /TS /FP   - - -  ( როგორც ჩვეულებრივი კოპირება )
.
"Destination-A"   - - - მისამართის ასე ბრჭყალებში ჩასმა,  პრაბელის პრობლემას აგვარებს 
```
.

