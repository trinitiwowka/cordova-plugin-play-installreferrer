
  

#  `cordova-plugin-play-installreferrer`

  

  

<p  align="center">
<a  href="https://badge.fury.io/js/cordova-plugin-play-installreferrer"><img  src="https://badge.fury.io/js/cordova-plugin-play-installreferrer.svg"  alt="npm version"  height="18"></a>
<a  href="https://opensource.org/licenses/Apache-2.0">
<img  src="https://img.shields.io/npm/dm/cordova-plugin-play-installreferrer.svg"  alt="License" />
</a>
<a  href="https://codeclimate.com/github/codeclimate/codeclimate/maintainability"><img  src="https://api.codeclimate.com/v1/badges/a99a88d28ad37a79dbf6/maintainability"/>
</a>
<a  href="https://opensource.org/licenses/Apache-2.0">
<img  src="https://img.shields.io/badge/License-Apache%202.0-blue.svg"  alt="License" />
</a>

</p>

  

  
  
  

> Cordova plugin to retrieve referral content from Google play using Google Play Store's Install Referrer API(Android)

  

  

  

##  API

  

  

  

The plugin exposes the following method:

  

  

  

```javascript
installReferrer.getReferrer(success, error);
```

  

  

  

####  Parameters:

  

  

* __success:__ success callback
The response object will have the object which contains all the referrer details and some of the common attributes are following

	.  **responseCode**:  response code(0/1/2)
	 . **clickTs**:  Referrer link click time stamp
	.  **installTs**: Install time stamp
	.  **isInstantExperienceLaunched**:  whether instant app launched or not

  

* __error:__ error callback


**Notes**

 - By default if the plugin method is called then the response will be like following
 

	    {
	      "clickTs": "0",
	      "installTs": "0",
	      "isInstantExperienceLaunched": "false",
	      "responseCode": "0",
	      "utm_medium": "organic",
	      "utm_source": "google-play"
	    }

 - if the url is like following 
   https://play.google.com/store/apps/details?id=com.example.application
   &referrer=utm_source%3Dgoogle %26utm_medium%3Dcpc  and its clicked   in a device having playstore then the  response will look like following

 

	     {
	      "clickTs": "<valid_ts>",
	      "installTs": "<valid_ts>",
	      "isInstantExperienceLaunched": "false",
	      "responseCode": "0",
	      "utm_medium": "cpc",
	      "utm_source": "google"
	    }

  

  

##  Installation

  

The plugin can be installed via [Cordova-CLI](https://cordova.apache.org/docs/en/dev/guide/cli/index.html#The%20Command-line%20Interface) and is publicly available on [NPM](https://www.npmjs.com/package/cordova-plugin-play-installreferrer).

  
  

Execute from the projects root folder:

```javascript

$  npm  i  cordova-plugin-play-installreferrer

$  cordova  plugin  add  cordova-plugin-play-installreferrer

```

  

Or install a specific version:

  

```javascript

$  npm  i  cordova-plugin-play-installreferrer@<latest_version>

$  cordova  plugin  add  cordova-plugin-play-installreferrer@<latest_version>

```

  

Or install the latest head version:

  

```javascript

$  cordova  plugin  add https://github.com/swayangjit/cordova-plugin-play-installreferrer.git

```

Or install from local source:

  

```javascript

$  cordova  plugin  add  <path>  --nofetch  --nosave  --link

```