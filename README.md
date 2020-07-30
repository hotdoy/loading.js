# loading.js

Add a loading and simple page state (```loading```, ```loaded``` and ```unloading```) to any site.

## Usage

### Add related js and css.
Add this in the ```<head>```.
<link href="/path/to/css/loading.css" type="text/css" rel="stylesheet">

This one goes all the way down just before the closing ```</body``` tag. It really should be the last thing you load.
<script src="/path/to/js/loading.js"></script>

### Add loader element.

Add ```<div data-loading></div>``` after the opening body tag (or anywhere you need it).

You can add ``` data-loaded-state-delay="100"``` to add a delay to the page ```loaded``` state, forcing the loader to stay in place for a set amount of time after the script is loaded.

ex: ```<div class="transition" data-loading data-loaded-state-delay="100"></div>``` would wait half a second before boing removed.

### Unloading
I also added a ```unloading``` class when a user leaves the page. By default the whole page will fade out. Check out ```loading.css```. It's pretty obvious.

### More
It's  CSS so have fun. You should probably know that the loader is being removed using a transitionEnd event. So only use css transition to remove the loader, and animations if you need to... well... animate something inside of it, like a logo or something. This also prevent event bubbling and I'm too lazy to do something about it.

