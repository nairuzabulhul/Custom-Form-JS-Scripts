##HTML
```
<!-- Custom Alerts -->

<div id="dialogoverlay"></div>
<div id="dialogbox">
  <div>
    <div id="dialogboxhead"></div>
    <div id="dialogboxbody"></div>
    <div id="dialogboxfoot"></div>
  </div>
</div>


```


##CSS

```
/* Wizard Alert box */
#dialogoverlay{
	display: none;
	opacity: .8;
	position: fixed;
	top: 0px;
	left: 0px;
	background: #FFF;
	width: 100%;
	z-index: 10;
}
#dialogbox{
	margin-top: 120px;
	display: none;
	position: fixed;
	background: none;
	border-radius:7px; 
	width:550px;
	z-index: 10;
}
 
  #okButton{
    width:100px;
    height:40px;
    background: rgba(51,51,51,0.5);
    color:white;
    line-height: 5px;
  }
  
#dialogbox > div{ background:#FFF; margin:8px; }
#dialogbox > div > #dialogboxhead{ background: rgba(51,51,51,0.8); font-size:19px; padding:10px; color:#fff;}
#dialogbox > div > #dialogboxbody{ background: rgba(128,128,128,0.9); padding:15px; color:#fff;  
  font-family: 'Raleway', sans-serif !important; font-size:18px; letter-spacing: 1px;}
#dialogbox > div > #dialogboxfoot{ background:rgba(128,128,128,0.9); padding:10px; text-align:right; }



```


##JS
```
//Custom Alert
function CustomAlert(){
    this.render = function(dialog){

        var winH = $(window).innerHeight(); //
        var winW = $(window).innerWidth();
        var dialogoverlay =$("#dialogoverlay");
        var dialogbox = $("#dialogbox");

    
        dialogoverlay.css('display','block');
        dialogoverlay.css('height',winH + "px");

        dialogbox.css('left',(winW/2) - (550 * .5) + "px");
        dialogbox.css('top','100px');
        dialogbox.css('display','block');

        $("#dialogboxhead").text("Wizard Alert !");
        $("#dialogboxbody").text(dialog);
        $("#dialogboxfoot").html('<button id="okButton" class="btn" onclick="Alert.ok()">OK</button>');
    }

  //Click ok to hide the alert box  
 this.ok = function(){
    $('#dialogbox').css('display','none');
    $('#dialogoverlay').css('display','none');
 }
}
var Alert = new CustomAlert();

```
