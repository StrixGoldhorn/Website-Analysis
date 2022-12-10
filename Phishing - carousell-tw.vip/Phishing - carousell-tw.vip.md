# Phishing - carousell-tw.vip

## Warning: Enter the site at your own risk, the site probably logs your IP

### Do NOT fill in any personal info



## Introduction

Found this site while browsing PhishTank



## Login Page

The link brings you to a site which simulates a login page for DBS PayLah.

When the user chooses to login, it redirects the user to `/GetStarted.php`, which asks for the user's phone number.<br/>

Upon submitting, it brings the user to `/MS code.php?p=XXXXXXXX`, where the query `p` is the phone number inputted in the previous page.<br/>

The page asks for the user's bank ID and PIN.<br/>

After which, the user is brought to `/opt.php`, where the user would enter the OTP sent to their devices.<br/>

## User Interation

While visiting the site, the site will constantly send POST requests to `/zy/api/api.php`.<br/>

Responses include having no response, `{"ok":"no"}`, `{"ok":"ok"}`, and `[{"msg":"<MESSAGE>"}]`, where `<MESSAGE>` is a string that presumably the criminals enter, seeing how varied responses are.


## XSS Discovery

Seeing as the criminals are able to craft responses based on user input, it can be inferred that they see the data that is POSTed to the server.<br/>

Hence, we decided to try a simple XSS attack. The payload simply loads an image that would ping a server that we had access to.<br/>

On the server, we were able to see that there was constant pings originating from `180.232.15.79`. Interestingly enough, the referrer header had `https[://]dbssingaporer[.]top/` as its value. Upon visiting the site, a similar phishing site was discovered.<br/>

## Afterwords

Though a seemingly more complex phishing website than most, it appears the scammers give little care about security. The obvious XSS vulnerability suggests a certain level of ignorance of basic cybersecurity issues.