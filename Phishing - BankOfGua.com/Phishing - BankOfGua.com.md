# Phishing - BankOfGua.com

## Introduction
BankOfGua.com is a phishing site, disguising itself as Bank of Guam. A simple mispelling of the last word, "Guam", may trick unsuspecting victims. It seeks to gather the victim's Login ID, Password, OTP, Email, Email Password.

<br/><br/><br/>

## Login
Below is a screencapture of the phishing login page.

<img src="Asset01-PhishLogin.png" width="75%" height="75%"><br/>

Victims input their Login ID and Password.

After clicking `Login`, their information is POSTed and redirected to `/i/mi8.php`

Once there, victims are prompted for their Access Code, which is then POSTed to `/i/emi91.php`. Victims are then redircted to `/i/mail.html`

Victims are prompted to enter their Email Address and Email Password, which aare POSTed to `/i/emi9.php`

Victims are then redirected to the actual homepage for Bank Of Guam