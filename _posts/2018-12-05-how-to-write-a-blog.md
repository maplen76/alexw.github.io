---
layout: post
title:  "R Proxy Configutaion"
---

R Configuration
===

### Configuring R to Use an HTTP or HTTPS Proxy  

To set the required environment variables you should add them to the R environment file (which is [read by R at startup](http://stat.ethz.ch/R-manual/R-patched/library/base/html/Startup.html)). On RStudio Server this file is found at **R_HOME/etc/Renviron.site**. On RStudio Desktop this file is found in the user home directory at **~/.Renviron**. You can easily access your .Renviron file by running the command `file.edit('~/.Renviron')` within RStudio  

Note that these files might not exist in the default installation of R so you may need to create them if they aren't already present.  

```{r}
http_proxy=http://proxy.dom.com/
http_proxy_user=user:passwd

https_proxy=https://proxy.dom.com/
https_proxy_user=user:passwd
```
### how to change the default working directory

1. Navigate to 'Rprofile.site', open it in text-editor.  
2. insert right at the top of the file in the first line the following command which tells R to set the working directory at start-up to the PATH you are specifying within the brackets (be sure you use double backslashes "\\" for Windows!)  
```
setwd("xxxx:\\xxxx\\xxxx")
```
