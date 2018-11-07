# codepath (Week 7 Assignment)
# WordPress Exploitations

# 1. SQLI with WordPress
WordPress is very vulberable to SQLI. SQLI is when a hacker inserts malicious SQL code/queries to get information of the databases.
Locating a function that doesn't check for any additional prriviledges will allow unauthorized users to inject malicious code to the database.
Another way a vulnerability is present if user-submitted data isn't checked to meet requirements.
ie: Adding letters or special characters to a phone number field.
These vulnerabilities can be avoided by making sure any data is checked to make sure its filled correctly, and user priviledges are checked so they can't spoof themselves as an admin.
Most vulnerabilites are due to an outdated version of WordPress, so keeping up to date version of WordPress will minimize vulnerabilities.
A good way to protect from SQLI is the santize function WordPress provides to developers. Santize function eliminates ALL excessive or disallowed characters in an text entry.
Most attack vulnerabilites are from <form> elements in the website, which means:
Contact forms (text)
Login (text and password)
Comment forms (textbox)
Ad pop ups (timed script events)
Shopping Carts (submit buttons)
Search Bars (text)

# 2. XSS with WordPress
XSS is arguably the most dangerous attack on WordPress. XSS stands for Cross-Site Scripting, which is where an attacker injects code without notification to a website user.
The main culprit is JavaScript being used in the WordPress website, as JavaScript is only going to get more advanced and powerful, the potential damage XSS can do is also increasing.
Tupes of attacks are Stored XSS, Reflected XSS, and DOM XSS 
A Stored XSS attack is server wide. How it works is the malcious code is accepted by the web server, so when a user loads the web page that has the malicious code, the user is shown the XSS code that was injected.
This is true for every single user that loads the attacked webpage.
Reflected XSS are when the input field allows <script> tags.
Mainly when you input a url in a text field, you can manipulate the URL where it has a <script> tag which then runs the malicous script and the user is displayed the attack.
DOM XSS is when malicious code is used to modify the DOM environment of the webpage.
DOM elements are <head>, <body>, <html>, <div>, <form>, etc.
The tag structure of a website make up the DOM structure.
This attack is the least common of the 3 XSS attacks

# 3. Brute Forcing WordPress
Brute force is meant to be a simple way of gaining access into WordPress.
A program tries endless possibility of usernames and passwords, eventually it will guess the correct one.
This attack focuses on the laziness and disregard of the need for security.
When a brute force attack is attacking the server, the database can become extremely laggy and unresponsive.
To protect against brute force, use a strong password and don't use common usernames
ie: admin/password user/pass etc
Can also protect the WordPress login webpage by setting up an IP address filter
The filter can deny ALL IP's except specific IP addresses given.
ie: allow from 192.168.1.1
deny from all
