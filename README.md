css3-loading
============

use css3 to create loading animation

###a simple start 
firstly will make a loading icon.

```html
    #loading{
		width:100px;
		height:100px;
		margin:100px;
		border-radius:100px;
		border: 20px solid #fff;
  		border-left: 20px solid rgba(0,0,0,0);
  		border-right:20px solid rgba(0,0,0,0);
  		animation: loading .5s infinite linear;
  		-webkit-animation: loading .5s infinite linear;

	}
	
```

THe next step is writing keyframe property.

```html
    @keyframes loading {
	    0% {
	        -moz-transform: rotate(0deg);
	    }

	    100% {
	        -moz-transform: rotate(360deg);
	    };
	}

	@-webkit-keyframes loading {
	    0% {
	        -webkit-transform: rotate(0deg);
	    }

	    100% {
	        -webkit-transform: rotate(360deg);
	    };
	}
	
```

see demo[<a href="http://codepen.io/Jack_Pu/pen/FyBuE">Codepen</a>] and <a href="https://github.com/JackPu/css3-loading/blob/master/css/simple-loading-animation.html">files</a>; 
====================
###make a bar loading 
we cam change the width of elment to create a bar loading.
```html
	@-webkit-keyframes loading{
		0%:{
			width:0;
		}
		100%{
			width: 100%;
		}
	}
	@keyframes loading{
		0%:{
			width:0;
		}
		100%{
			width: 100%;
		}
	}
```

see demo[<a href="http://codepen.io/Jack_Pu/pen/FyBuE">Codepen</a>] and <a href="https://github.com/JackPu/css3-loading/blob/master/css/bar-loading.html">files</a>; 

### now let's do something trouble. We can make a circle loading.

