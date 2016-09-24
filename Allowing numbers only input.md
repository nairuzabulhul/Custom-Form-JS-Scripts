```

("#groupSize").keypress(function(e){

    var val = $(this).val()
    var reg = /^0/gi;
    if (val.match(reg)) {
        $(this).val(val.replace(reg, ''));
    }
  
     //if the letter is not digit then display error and don't type anything
     if (e.which != 8 && e.which != 0 && (e.which < 48 || e.which > 57)) {
        //display error message
        // $("#errmsg").html("Digits Only").show().fadeOut("slow");
               return false;
    }
    

});

```

###Note:

Allowing numbers only to be entered as input in a form. Also, restrict users from using 0 as first digit 
