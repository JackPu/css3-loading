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

```html

THe next step is writing keyframe property.

	
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

```html
see demo[<a href="http://codepen.io/Jack_Pu/pen/FyBuE">Codepen</a>] and <a href="https://github.com/JackPu/css3-loading/blob/master/css/simple-loading-animation.html">files</a>; 
=======
	
```

see demo[<a href="http://codepen.io/Jack_Pu/pen/FyBuE">Codepen</a>] and <a href="https://github.com/JackPu/css3-loading/blob/master/css/simple-loading-animation.html">files</a>; 

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

now let's do something trouble. We can make a circle loading.

Firstly, we'll create a circular ring.

```html
#circle-loader-wrap{
	overflow: hidden;
	position: relative;
	margin:20px;
	width:100px;
	height:100px;
	box-shadow:0px 0px 20px rgba(0,0,0,.1) inset;
	background-color: #eee;
	border-radius:50px;
}
#circle-loader-wrap:after{
	content: '';
	position: absolute;
	left:20px;
	top:20px;
	width:60px;
	height:60px;
	border-radius: 50%;
	background-color:#1ba1e2; 
	box-shadow:0 0 10px rgba(0,0,0,.2);

}

```

Secondly we'll make the scrollbar.

```html
#circle-loader-wrap > div{
			overflow: hidden;
			position: absolute;
			width: 50%;
			height:100%;
		}

		.left-wrap{
			left: 0;
		}
		.right-wrap{
			left:50%;
		}
		.left-wrap .loader{
			border-top-left-radius: 0;
			border-bottom-left-radius: 0;
			transform-origin:0 50% 0;
			-webkit-transform-origin:0 50% 0;
			animation:loading-left 3s infinite linear 0;
			-webkit-animation:loading-left 3s infinite linear 0;	
			
		}
		.right-wrap .loader{
			left:-100%;
			border-bottom-right-radius: 0;
			border-top-right-radius: 0;	
			transform-origin:100% 50% 0;
			-webkit-transform-origin:100% 50% 0;
			animation:loading-right 3s infinite linear ;
			-webkit-animation:loading-right 3s infinite linear ;	
		}
		.loader{
			position: absolute;
			left:100%;
			top:0;
			width:100%;
			height:100%;
			border-radius: 1000px;
			background-color: #111;

		}

```
Thirdly,we'll write keyframes

```html
@keyframes loading-left{
			0%{
				transform:rotate(0deg)
			}
			25%{
				transform:rotate(180deg)
			}
			50%{
				transform:rotate(180deg)
			}
			75%{
				transform:rotate(360deg)
			}
			100%{
				transform:rotate(360deg)
			}
		}
		@-webkit-keyframes loading-left{
			0%{
				-webkit-transform:rotate(0deg)
			}
			25%{
				-webkit-transform:rotate(180deg)
			}
			50%{
				-webkit-transform:rotate(180deg)
			}
			75%{
				-webkit-transform:rotate(360deg)
			}
			100%{
				-webkit-transform:rotate(360deg)
			}
		}
		@keyframes loading-right{
			0%{
				transform:rotate(0deg)
			}
			25%{
				transform:rotate(0deg)
			}
			50%{
				transform:rotate(180deg)
			}
			75%{
				transform:rotate(180deg)
			}
			100%{
				transform:rotate(360deg)
			}
		}

		@-webkit-keyframes loading-right{
			0%{
				-webkit-transform:rotate(0deg)
			}
			25%{
				-webkit-transform:rotate(0deg)
			}
			50%{
				-webkit-transform:rotate(180deg)
			}
			75%{
				-webkit-transform:rotate(180deg)
			}
			100%{
				-webkit-transform:rotate(360deg)
			}
		}

```html

see demo[<a href="http://codepen.io/Jack_Pu/pen/citru">Codepen</a>]  and <a href="https://github.com/JackPu/css3-loading/blob/master/css/circle-loading.html">files</a>; 


