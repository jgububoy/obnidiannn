---
aliases:
  - sync.sh
  - script
  - pull push
  - pull and push
  - pull & push
tags:
  - git
  - linux
done: false
created: 2026-09-01
sourse:
---
# git script

სკრიპტით  დასაფულად და დასაფუშად.

```shell
#!/bin/bash 
# ეს სკრიპტი ამატებს, აკომიტებს, სინქრონიზებს სერვერთან --rebase-ით და აგზავნის ცვლილებებს 

TODAY=$(date) 
HOST=$(hostname) 

# 1. ვამატებთ და ვპაკავთ ცვლილებებს ლოკალურად 
git add . 
git commit -m "Changes committed: $TODAY from $HOST" 

# 2. ვქაჩავთ სერვერიდან სხვების მიერ გაგზავნილ ცვლილებებს rebase-ით (შენი კომიტები დროებით გადაიდება და ზემოდან მიეყოლება) 
git pull --rebase 

# 3. ვგზავნით სერვერზე 
git push
```

.
![](_attachments/3168377301af851438d973ce77c7702c.png)
.
