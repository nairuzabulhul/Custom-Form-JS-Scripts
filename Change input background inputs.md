```
$("#groupSize").keyup(function(){
    // $("#groupSize").toggleClass("red");
    // $("#groupSize").val().length !== 0 
    // console.log(typeof($(this).val()));
      
    if( $("#groupSize").val().length !== 0 && $("#groupSize").val() !== "0"){
      // console.log('red');
      $("#groupSize").css('background','white');
    }else{
      $("#groupSize").css('background','red');
    }


});

 ```
 
 ###Note:
 
 Change the input background color to red if it is empty, and white once the user starts typing 
 
 

