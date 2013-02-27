---
comments: true
date: 2013-01-20 15:30:00
published: true
layout: post
slug: appsunday-arq
title: "#AppSunday: Arq"
categories:
- AppSunday
---

{% img center no-border http://cdn.fmartingr.com/blog/uploads/2013/01/appsunday-arq/main-screen.png "Main ARQ 2 Screen" %}

Have you ever heard of *TimeMachine*? That Apple app that makes backups of your hard drive with a really nice interface to restore backups from finder. Well, Arq is that but without the nice interface and the backups are made to Amazon S3 instead of an external hard drive.
<!-- more -->
Backups to internet? Are you crazy? Maybe, but I find this pretty convenient since my MAC is a laptop with two USB ports and I don't want to have one of them always busy with a external hard drive for Time Machine. And by the way, all backups are encrypted.

{% img center no-border http://cdn.fmartingr.com/blog/uploads/2013/01/appsunday-arq/exclude-filters.png "I don't want cache files!" %}

You can filter whatever you don't want to be stored. For example, I have checked the `~/Library` folder excluding every folder/file with `cache` on its name, and also I've unchecked manually -left in the screenshot- iTunes and mail folders. Since all my mail accounts are IMAP and my music are synced with iTunes Match I don't really want those being stored.

{% img center no-border http://cdn.fmartingr.com/blog/uploads/2013/01/appsunday-arq/s3-budget.png "Please, no more than $4 from S3" %}

Arq also let you configure how much money do you want to spend on your S3 Bucket. Just type in how much money -or how much space- you want to have, and Arq will do the calculations. If you're near to your space limit, old files will be removed. I've a $4 limit but my monthly bill has never reached two bucks.

If you don't have a backup solution for your computer is worth giving it a try. Arq has saved my life two times already. Also made a full OS reinstall less more painful.

> **Arq 3 update:** At the time of writing a new version of Arq was released with Amazon Glacier support. Since I have not tested it I can say anything, but apparently have less costs if you don't access frequently to the files and it seems that you can configure S3 and Glacier at the same time.

You can download a 30 day trial from [Arq's website](http://www.haystacksoftware.com/arq/), after that, the complete version costs $29, but it's totally worth the price.