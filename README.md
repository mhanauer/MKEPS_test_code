---
title: "Diss Power"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```
Diss code cleaning
MKEPS_psycho_unpublish_July 15, 2020_13.13
```{r}
setwd("~/Desktop")
mkeps_test = read.csv("MKEPS_psycho_unpublish_July 15, 2020_13.13.csv", header = TRUE, na.strings = c("", " "))
### Delete second row
mkeps_test = mkeps_test[-c(1:2),]
### Keep
# Q2 program evaluation or research experience
#Q3 Age
#Q38 Education level
## Q4 lanauge
mkeps_test = mkeps_test[c("Q2", "Q3", "Q4")]
mkeps_test_complete = na.omit(mkeps_test)
mkeps_test_complete_elig
mkeps_test_complete_elig = subset(mkeps_test_complete, Q4 == "Full professional working proficiency" | Q4 == "Native or bilingual proficiency")
mkeps_test_complete_elig
```



 

