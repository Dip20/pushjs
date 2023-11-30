### This is a custom browser notification

Reference : [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/API/Notifications_API/Using_the_Notifications_API)

``` javascript

function  askNotificationPermission() {

    // function to actually ask the permissions
	function  handlePermission(permission) {
		// set the button to shown or hidden, depending on what the user answers
	     notificationBtn.style.display  = Notification.permission  ===  "granted"  ?  "none"  :  "block";
	}

	// Let's check if the browser supports notifications
	if (!("Notification"  in window)) {
		console.log("This browser does not support notifications.");
	
	} else {
		Notification.requestPermission().then((permission) => {
			handlePermission(permission);

		});
	}
}

```