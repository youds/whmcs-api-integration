# WHMCS API Integration
Fully featured WHMCS API Implementation, including; 
 * Client Registration, 
 * Domains 
 * Hostings 
 * Support
 
This is basically everything you need for the WHMCS API facility and it supports all actions available on the WHMCS API (as of November 2018) - there is a really intuitive nature to this code base which basically takes on board the allowed parameters and settings and then gives you the ability to generate requests based upon this information - one method with the action to perform and the parameters needed is all it takes to have a fully operational API that gives back clean, clear consise error messages almost like there is a single method for each request. 
 
For your convienance, there is a very nice test.php page which allows you to run tests on the API which can be found here http://www.youds.com/services/themes-and-plugins/whmcs-api-integration/code/test.php

Example Code:
```
$whmcs = new Hosting($url, $apiKey);
$whmcs->send('GetTickets', array('limitnum' => 100));
```

There is also a really nice feature which will return a nice HTML output of the required values of each request plus a list of available requests as well, with optional category filtering 

```
$whmcs = new Hosting($url, $apiKey);
$whmcs->listParams('GetTickets');
$whmcs->list($module);
```

Alternatively, it will give you everything on one page.

```
$whmcs = new Hosting($url, $apiKey);
echo $whmcs->listAll($module);
```

If you need support or assistance head over to http://www.youds.com/ and we'd be happy to help.
