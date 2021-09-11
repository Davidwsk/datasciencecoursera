---
title: "HelloWorld.md"
author: "David"
date: "9/2/2021"
output: html_document
---

## This is a markdown file

```
hw1_data <- read.csv("hw1_data.csv")

str(hw1_data)

head(hw1_data)

nrow(hw1_data)

tail(hw1_data)

nrow(hw1_data[is.na(hw1_data$Ozone), ])

mean(hw1_data[!is.na(hw1_data$Ozone), ]$Ozone)

comp_data <- hw1_data[complete.cases(hw1_data[,c("Ozone", "Temp", "Solar.R")]),]
mean(comp_data[(comp_data$Ozone > 31) & (comp_data$Temp > 90), "Solar.R"])

comp_data1 <- hw1_data[complete.cases(hw1_data[,c("Temp", "Month")]),]

nrow(comp_data)
nrow(comp_data1)

mean(comp_data1[comp_data1$Month == 6, "Temp"])

comp_data2 <- hw1_data[complete.cases(hw1_data[,c("Ozone", "Month")]),]
max(comp_data2[comp_data2$Month == 5, "Ozone"])

```