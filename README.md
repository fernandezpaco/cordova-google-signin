# cordova-google-signin
Polymer component for google-signin in cordova apps

Use this component instead of <google-signin> when you are packing your app using cordova

You will need InAppBrowser plugin

```html
 <cordova-google-signin 
    id="cordovasignin" 
    client_id="715517905347-vss7aqemaamj2vlvokivjrecig4tbu4o.apps.googleusercontent.com"
    client_secret= "3czRmsT30F8VG1ROYtMNT64a">
  </cordova-google-signin>
  <script type="text/javascript">
	document.addEventListener("deviceready", onDeviceReady, false);
	function onDeviceReady() {	    
	    window.open = cordova.InAppBrowser.open;
	    document.querySelector("#cordovasignin").getToken();
	}
  </script>
```