*****************************  scrollAnimate.js  ********************************

no tough syntaxes there is only one line toremember to work on

the instance of calass Scroll is already defined as "atipo"
you just have to consider two lines only and let atipo do all the
rest.

//syntax

atipo(object,screen-param,anim-func1,anim-func2);

at the end when you have added all the object you wanted to atipo
write,
atipo.chk();

eg,

$(document).ready(function(){
	atipo(object,screen-param,anim-func1,anim-func2);
	/code/
	atipo(object,screen-param,anim-func1,anim-func2);
	/code/
	//at the end
	atipo.chk();
});

1) object -> refrence to the tag.

2) screen param:
	the screen is being measured from bottom the full length is
	scaling from 0-1 i.e. for half the screen from boottom it will
	be 0.5, what this does is you are giving the trigger to atipo
	so thet when the object passes though it, atipo triggers the 
	animate functions.
	NOTE: In case the object has property fixed or you want it to 
	animate alltime without giving any trigger value,
	i.e. whenever the page is scrolled the animation should occur
	just pass "null" in the place of screen param,
	
	eg, atipo(object,null,anim-func1,anim-func2);

3) aim-func1: atipo will call it whenever the page is scrolled down
	      considering the trigger values.

4) aim-func2: atipo will call it whenever the page is scrolled down
	      considering the trigger values.

eg,

	function fn1(){
		$("p").css({"color":"red"});
	}
	function fn2(){
		$("p").css({"color":"green"});
	}
	function fn3(){
		$("h1").css({"color":"red"});
	}
	function fn4(){
		$("h1").css({"color":"green"});
	}
    
	atipo.func(document.getElementsByTagName("p")[0],0.5,fn1,fn2);
	atipo.func(document.getElementsByTagName("h1")[0],null,fn3,fn4);
	atipo.chk();


just give this in your $(document).ready function in the html file
or js file.

tag jquery in your page
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>

This will help you to pass your own animations rather than the ones other scroll 
libraries give you and you have no other option
but now you are the one who is going to decide what should happen and when it should happen
by just using two lines


