<!DOCTYPE html>
<!--[if IE 7]>
<html class="ie ie7" lang="en-US">
<![endif]-->
<!--[if IE 8]>
<html class="ie ie8" lang="en-US">
<![endif]-->
<!--[if !(IE 7) | !(IE 8)  ]><!-->
<html lang="en-US">
<!--<![endif]-->
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width">
	<title>ImageMagick® mapIcon generator | Example</title>
</head>
<body>
<?php
echo "<div 
style='position:absolute;
left:50%;width:500px;
text-align:center;
border:1px solid red;
padding:15px;'
>
<span style='font-family:arial;font-weight:bold;'>
Imagick is a native php extension to create and modify images using the ImageMagick® API</span>
<br>
http://php.net/manual/en/book.imagick.php
<hr>";
$myimage= '../experiment_host/php/monferrato_esagoni/icon/vuoto.png';

for ($i = 0; $i < 100; $i++) {

/* Create some objects */
$image = new Imagick($myimage);
$draw = new ImagickDraw();
//$pixel = new ImagickPixel( 'gray' );

/* New image */
//$image->newImage(800, 75, $pixel);


/* Black text */
$draw->setFillColor('black');

/* Font properties */
$color = new ImagickPixel('#fff');
$draw->setFont('/var/www/experiment_host/php/monferrato_esagoni/icon/Oswald-Regular.ttf');
$draw->setFontSize( 80 );
$draw->setFillColor($color);
$draw->setGravity (Imagick::GRAVITY_CENTER);

/* Create text */
$image->annotateImage($draw, 0, -10, 0, $i);

/* Give image a format */
$image->setImageFormat('png');


    file_put_contents ($i.".png", $image);
    echo "<img src='$i.png' width='38'> ";
}
echo "<hr><span style='font-family:arial;'>$i files scritti</span>";
echo "</div>";
?>
</body>
</html>
