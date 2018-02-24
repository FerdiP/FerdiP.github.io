---
title: SD Card with foxBMS
layout: post
---

An SD Card female connector is available on foxBMS Extension board. It is therefore, available for us to store and read some data under, such as, text files. Let's begin this task by several preparations!

## [Notices]
The version of foxBMS's embedded software I am using is NOT the newest version-1.0.0. There might needed changes, but I hope that the following jobs can be integrated easily into the newest software version.

## [Requirements] 
1/ A SD Card, which is formated under FAT. You can do it by Quick Format in Windows. 

2/ [FatFs](http://elm-chan.org/fsw/ff/00index_e.html) Module by Chan. I used FatFs R0.13a. For a easier setup, I recommend to download the "FatFs sample projects for various platforms" (scroll down to the end of the page and click to download!). 

3/ A running foxBMS project on Eclipse. Debugging with Eclipse is not important, because I got problems while using Eclipse under Debug mode. So, it must only compile and generate ".hex" file.

## [Getting Start]
![Fig1: Connections at SD Card module on BMS Extension board](https://github.com/FerdiP/FerdiP.github.io/blob/master/images/2017-12-24-sd-card-with-foxbms/SD_Card_Schematic.png)

## [Programming]
1/ Naviagate to "../foxBMS_primary/src/module/" . Create a new folder: sdcard.

2/ Remember that we downloaded the "FatFs sample projects for various platforms"? For the task I am doing, I need to copy those files: "ff.h", "ff.c", "ffconf.h", "ffunicode.c", "integer.h", "diskio.h", "mmc_stm32f1.c". For anyone that are familiar to FatFs, the file "mmc_stm32f1.c" has the same function as "diskio.c". Therefore, I prefer to rename "mmc_stm32f1.c" into "diskio.c". 


## [Running]