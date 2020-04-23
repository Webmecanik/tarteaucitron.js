[![](https://data.jsdelivr.com/v1/package/gh/AmauriC/tarteaucitron.js/badge)](https://www.jsdelivr.com/package/gh/AmauriC/tarteaucitron.js) 
[![npm](https://img.shields.io/npm/v/tarteaucitronjs.svg)](https://www.npmjs.com/package/tarteaucitronjs) [![GitHub contributors](https://img.shields.io/github/contributors/AmauriC/tarteaucitron.js.svg)](https://github.com/AmauriC/tarteaucitron.js/graphs/contributors)

tarteaucitron.js
================
Comply to the european cookie law is simple with the french *tarte au citron*.

# What is this script?
The european cookie law regulates the management of cookies and you should ask your visitors their consent before exposing them to third party services.

Clearly this script will:
- Disable all services by default,
- Display a banner on the first page view and a small one on other pages,
- Display a panel to allow or deny each services one by one,
- Activate services on the second page view if not denied,
- Store the consent in a cookie for 365 days.

Bonus:
- Load service when user click on Allow (without reload of the page),
- Incorporate a fallback system (display a link instead of social button and a static banner instead of advertising).


# Installation guide for Webmecanik Automation

* Download the release zip and copy the directory on your site's server.

# How to use it with Webmecanik Automation

* Add the following code in the head tag `<head>` of your site
* Don't forget to check the tarteaucitron directory is correctly indicated in the `src

```html
<script type="text/javascript" src="/tarteaucitron/tarteaucitron.js"></script>

<script type="text/javascript">
tarteaucitron.init({
    "privacyUrl": "", /* Privacy policy url */

    "hashtag": "#tarteaucitron", /* Open the panel with this hashtag */
    "cookieName": "tarteaucitron", /* Cookie name */
    
    "orientation": "middle", /* Banner position (top - bottom) */
    "showAlertSmall": true, /* Show the small banner on bottom right */
    "cookieslist": true, /* Show the cookie list */

    "adblocker": false, /* Show a Warning if an adblocker is detected */
    "AcceptAllCta" : true, /* Show the accept all button when highPrivacy on */
    "highPrivacy": true, /* Disable auto consent */
    "handleBrowserDNTRequest": false, /* If Do Not Track == 1, disallow all */

    "removeCredit": false, /* Remove credit link */
    "moreInfoLink": true, /* Show more info link */
    "useExternalCss": false, /* If false, the tarteaucitron.css file will be loaded */

    //"cookieDomain": ".my-multisite-domaine.fr", /* Shared cookie for subdomain website */
                          
    "readmoreLink": "/cookiespolicy" /* Change the default readmore link pointing to opt-out.ferank.eu */
});
</script>
```

# Use Webmecanik service by adding the following code before the closing body tag `</body>`
### Don't forget to replace 'webmecanikurl' by your Automation instance's url
Exemple: 'https://my.instance.url/mtc.js'

```html
<script type="text/javascript">
        tarteaucitron.user.webmecanikurl = 'webmecanikurl/mtc.js';
        (tarteaucitron.job = tarteaucitron.job || []).push('webmecanik');
</script>
```
## Don't forget to delete the script below from your webpage
```html
<script>
    (function(w, d, t, u, n, a, m) {
        w['MauticTrackingObject'] = n;
        w[n] = w[n] || function() {
            (w[n].q = w[n].q || []).push(arguments)
        }, a = d.createElement(t), m = d.getElementsByTagName(t)[0];
        a.async = 1;
        a.src = u;
        m.parentNode.insertBefore(a, m)
    })(window, document, 'script', 'webmecanikurl', 'mt');
    mt('send', 'pageview');
</script>
```

You can visit the tarteaucitron creator's website by clicking on the link below
[Visit opt-out.ferank.eu](https://opt-out.ferank.eu/)

