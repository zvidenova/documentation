---
layout: page
title:  How to install Open Classifieds on VULTR
date:   2015-08-10
categories: HowTo
tags: HowTo
permalink: /install-oc-on-vultr/
---
# How to install Open Classifieds on VULTR

## Introduction

Open Classifieds is an Open Source (GPL v3) project that lets you easily create your own fully customizable classifieds site. OC can be used to create car/auto sales, job search board, buying & selling real estate and almost anything you can think of. Thousands of web developers trust Open Classifieds to run their big classifieds websites.

## Requirements

+ Apache 2+
+ PHP 5.5+
+ Short Tags
+ GD support
+ mod_rewrite
+ mcrypt
+ Gettext
+ Curl
+ MySQL 5+

You can follow [this guide](https://www.vultr.com/docs/how-to-install-apache-mysql-and-php-on-ubuntu) to install LAMP.

## Configure the Database

To install Open-Classifieds, you will need a Database and a Username. Follow [this link](http://docs.yclas.com/create-mysql-database/) to know how to create a MySQL Database.

Log in to MySQL with the root account.

    mysql -u root -p

The system will prompt you for a password. Use your MySQL root password.

Now, create a database to use for Open Classifieds. We will call it _openclassifieds_ in this example.

    CREATE DATABASE openclassifieds;

Next, create a database user and assign a password. You can replace username _ocuser_ and _password_ to your password.

    CREATE USER ocuser@localhost IDENTIFIED BY '_password_';  

Grant permission to access the database.

    GRANT ALL PRIVILEGES ON openclassifieds.* TO ocuser@localhost;

Now set the new user and reload the privileges.

    FLUSH PRIVILEGES;

Exit MySQL

    exit


## <a name="installation"></a>[Installation](#installation)

+ Download **[install-openclassifieds.php](https://raw.githubusercontent.com/open-classifieds/openclassifieds2/master/install-openclassifieds.php)**
+ Upload it to Apache's document root
+ Run **http://yourdomain.com/install-openclassifieds.php**
+ Press **Download and Install**
+ Follow the steps
+ Log in to your **Admin Panel**, create some **Categories** and **Locations**
+ Working!

Watch this video for more detailed instructions.

<a href="https://www.youtube.com/watch?v=L2-b8r8DAfU" target="_blank"><img src="http://img.youtube.com/vi/L2-b8r8DAfU/0.jpg" 
alt="Open classifieds 1 file installation" width="480" height="360" border="10" /></a>
