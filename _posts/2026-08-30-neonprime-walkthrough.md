layout: writeup
title: "Name of the Challenge"
tags: [web, ctf]
date: 2026-08-30
Challenge Name

##Enumeration
I opened my web browser and navigated to http://10.10.10.50.

The page loaded a very simple white screen with just one line of text:

"Welcome to NeonPrime. Nothing to see here..."

It looks like a static page. My instinct when I see a simple web page in a CTF is to check the HTML Source Code. Developers often leave comments in the code that they forget to remove.

I pressed Ctrl+U (or Right Click -> View Page Source).

## Exploitation
Looking through the HTML, near the bottom of the file, I spotted an HTML comment that looked suspicious:

<!-- 
    TODO: Remove this flag before production!
    FLAG: THM{v13w_s0urc3_1s_k3y}
-->
There it is! The flag was hidden in a comment within the source code.
