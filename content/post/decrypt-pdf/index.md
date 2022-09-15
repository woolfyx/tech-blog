---
title: Decrypt PDF file
description: Using QPDF to remove the owner password of a PDF file
hidden: false
slug: decrypt-pdf
date: 2022-09-15 00:00:00+0000
image: cover.jpg
categories:
    - Tips
---

I would like to share a small tips today.

## Step 1 - Install QPDF
The documentation is available here : https://qpdf.readthedocs.io/en/stable/index.html

Note: For MacOs user, this tool can be installed via [HomeBrew](https://formulae.brew.sh/formula/qpdf)

## Step 2 - Remove the owner password and the encryption
This is the easiest step, you just have to run this command : `qpdf --decrypt --password="user password" <source file>.pdf <destination file>.pdf`.  

Note: `User password` is the password to open the file. If no password is set to open the file, you can remove this argument.