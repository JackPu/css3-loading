css3-loading
============

use css3 to create loading animation

###a simple start
firstly will make a loading icon.
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
THe next step is writing keyframe property.
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
