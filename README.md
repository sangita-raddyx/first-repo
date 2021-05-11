# first-repo
login using ajax code

 $(document).ready(function () {
 
$('#myForm').submit(function(e){

   event.preventDefault();
   
   var data = $(this).serialize();
   
    var url = $(this).attr('action');
   
   $.ajax({
   
     url:url,
     
     type:'post',
     
     data:data,
     
     dataType:'json',
     
     success:function(response) {
     
       if(response == 1) {
       
         console.log('success');
	 
       } else {
       
         console.log('login fails');
	 
        }
	
     }
     
   });
   
});

});
