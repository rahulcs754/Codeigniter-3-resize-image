# Codeigniter-3-resize-image
You can use resize image 


```php 

$im = new Imagick("File Path"); 
$im->thumbnailImage(1024,800);  
$im->writeImages("File Path", true);
$im->destroy(); 


```


# Convert pdf to image 


```php

$im = new Imagick(); 
$im->setResolution(1200,800);   
$im->readimage("File Path"); 
$im->setImageFormat('jpg');     
$im->writeImage("File Path"); 
$im->clear(); 
$im->destroy();


```

# Delete old file before update 

```php
$path = './uploads/MasterMarketing/';

$wheref = array('sno'=>$postData['cat_id']);
$image =  $this->Common_Model->select_data('masterdata',' ',$wheref);
 
if(file_exists($path.$image[0]->filename))	{
	@unlink($path.$image[0]->filename);
 }
```
