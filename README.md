<img width='100px' src="https://lh6.ggpht.com/A-yid4qbc4wci0KS4jls8roFYv3lMkFXYlisLryRxHBzEIwmadqX3Lc6OZNocQkBXB0=w300"
 alt="easy button" align="right" />
huffpostlabs-btn
================

Mobile friendly buttons made easy.

Why call these buttons mobile friendly?
---
- Converts HTML elements with the ```onclick``` event handler into elements that can also handle more complex mobile events.
- ```onclick``` event handler is also fired on the ```touchend``` event if and only if:
	- The ```ontouchstart``` event was recently fired within 10px of the ```touchend``` event.
- ```onclick``` event is canceled upon the firing of the ```touchend``` event so that the target event is only handled once.
- If a user instead drags away from the place where the initial ```touchstart``` event was fired, then the event is cancelled.
	- This allows the user to scroll past a button without an event firing.

Step By Step Use:
---
- complement all ```onclick="onclickstring"``` with the ```data-huffpostlabs-btn``` tag.
- create a ```HuffpostLabsBtnMaster``` to convert your buttons: ```var myBtnMaster = new HuffpostLabsBtnMaster(context)``` 
	- Where context is the HTML container that contains your buttons.
- HuffpostLabsBtnMaster will find all of the elements with the ```data-huffpostlabs-btn```, grab each elements onclick handler, and retrofit each element with better event handling that calls that handler.

Example Usage:
---
```
	<script src="http://aberke.github.io/huffpostlabs-btn/btn-master.js"></script>
	<div id='all-my-btns-container'>
		<p>la da daaaa</p>
		<span data-huffpostlabs-btn onclick='f1()'>CLICK OR TOUCH TO FIRE f1</span>
		<span data-huffpostlabs-btn onclick='f2()'>CLICK OR TOUCH TO FIRE f2</span>
		<p>More HTML</p>
	</div>
	<script>
		var container = document.getElementById('all-my-btns-container');
		var myBtnMaster = new HuffpostLabsBtnMaster(container);
	</script>
```


Pull Requests:
===
Yes Please.


