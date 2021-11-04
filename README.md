<h1>deepai</h1>

a small library for usage deepai.org api

<h1>usage</h1>
<pre>
<?php

use Solid\Deepai\Deepai;

require_once 'vendor/autoload.php';
$deepai = new Deepai('api key');
/*
you first should be take your api-key in Deepai construct 

after that you can use this
*/

$deepai->setImage(''); // you can use a url or a local file path
$deepai->colorize();
/*
you can use  colorize,toonify,suoerResolution for edit your pics 

*/
try {

   $url = $deepai->apply()->getUrl();
   //get edited image url
   
   $deepai->apply()->save();
   //save edited image to local file
   
} catch (\GuzzleHttp\Exception\GuzzleException $e) {
}



</pre>
