<!DOCTYPE html> 
<html>
  <head>
	<script type="text/javascript" src="/javascript/jquery.js"></script>  
	<script type="text/javascript" src="/javascript/jquery.fileupload.js"></script> 
<script type="text/javascript">                                    
    $(function() {                                                   
      $('#fileupload').fileupload({                                  
        url: 'https://<%= BUCKET %>.s3.amazonaws.com/',       
        type: 'POST',                                                
        autoUpload: true,                                            
        formData: {                                                  
          key: "<%= "#{SecureRandom.uuid}/${filename}" %>",                                        
          AWSAccessKeyId: "<%= ACCESS_KEY_ID %>",                   
          acl: "public-read",                                        
          policy: "<%= policy %>",                                  
          signature: "<%= signature %>",                            
          success_action_status: "201"     
        }                                                            
      });                                                            
    });                                                              
</script>                                                          
  </head>
  <body>                                                                   
	<form action="/upload" method="post" enctype="multipart/form-data">
	  <input type="file" id="fileupload" name="file">                  
	  <input type="submit" value="Save">                               
	</form>                                                            
  </body>
</html>
  <div class="item">
	<img src="http://www.jqueryscript.net/images/Simplest-Responsive-jQuery-Image-Lightbox-Plugin-simple-lightbox.jpg" alt="Flower">
  </div>
</div>

<!-- Left and right controls -->
<a class="left carousel-control" href="#myCarousel" role="button" data-slide="prev">
  <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
  <span class="sr-only">Previous</span>
</a>
<a class="right carousel-control" href="#myCarousel" role="button" data-slide="next">
  <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
  <span class="sr-only">Next</span>
</a>
</div>
</div>

</body>
</html>
