# cordova-google-signin
Polymer component for google-signin in cordova apps

Use this component instead of <google-signin> when you are packing your app using cordova

You will need InAppBrowser plugin

As described in https://developers.google.com/identity/protocols/OAuth2InstalledApp your secret key is not supposed to be secret for installed apps

```html
 <cordova-google-signin 
    id="cordovasignin" 
    client_id="your-client-id"
    client_secret= "your-secret-key">
  </cordova-google-signin>
  <script type="text/javascript">
	document.addEventListener("deviceready", onDeviceReady, false);
	function onDeviceReady() {	    
	    window.open = cordova.InAppBrowser.open;
	    document.querySelector("#cordovasignin").getToken();
	}
  </script>
```