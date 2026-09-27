---
aliases:
tags:
  - FTP_FTPS_SFTP
  - network
done: false
created: 2026-08-24
sourse:
---
# SSL certificate problem

[Link_1](https://confluence.atlassian.com/bitbucketserverkb/ssl-certificate-problem-unable-to-get-local-issuer-certificate-816521128.html)
When using Windows, the problem resides that git by default uses the "Linux" crypto backend, so the _GIT_ operation may not complete occasionally. Starting with _Git_ for Windows 2.14, you can configure Git to use _SChannel_, 
the built-in Windows networking layer as the crypto backend. To do that, just run the following command in the _GIT_ client: 
(ერთერთი მუშა ვარიანტი)

```bash
git config --global http.sslbackend schannel
```

[Link2](https://komodor.com/learn/how-to-fix-ssl-certificate-problem-unable-to-get-local-issuer-certificate-git-error/)



