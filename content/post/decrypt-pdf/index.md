---
title: Decrypt PDF file
description: Using QPDF to remove the restrictions of your PDF files
hidden: false
slug: decrypt-pdf
date: 2022-09-15 00:00:00+0000
image: cover.jpg
categories:
    - Tips
---

In short, a PDF file can have 2 passwords:

- User: to open a file
- Owner: to restrict changing the permissions

If you download a file, which belongs to you, in many cases some restrictions should be applied on it and in many situations you may want to remove these but you may not have the owner's password. That's okay, here is an easy solution based on the **qpdf** tool.

## Install QPDF
The documentation is available here : https://qpdf.readthedocs.io/en/stable/index.html.  
Below an easy way to install it:

- For MacOs user, this tool can be installed via [HomeBrew](https://formulae.brew.sh/formula/qpdf): `brew install qpdf`
- For Debian-based systems, this tool can be install via apt: `apt install qpdf`

## Remove the owner password and the encryption
This is the easiest step, you just have to run this command : `qpdf --decrypt --password="user password" "source file.pdf" "destination file.pdf"`.  

Note: the `--password` argument is optional. If the file does not require any password to open it, you can ommit this part.

Et voilà!
