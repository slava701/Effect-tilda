<?php
include("db.php");
session_start();
$enable_captcha=false;
$res['success']=false;

if( $_SERVER["REQUEST_METHOD"] == "POST" ) {

$recaptcha=$_POST['g-recaptcha-response'];

if( !empty( $recaptcha ) ) {

if( $enable_captcha ){

include("getCurlData.php");
$google_url="https://www.google.com/recaptcha/api/siteverify";
$secret='6Ld-ogsTAAAAAK0DpO4o4Ama4OPg3xS-Quamaqkq';
$ip=$_SERVER['REMOTE_ADDR'];
$url=$google_url."?secret=".$secret."&response=".$recaptcha."&remoteip=".$ip;
$res=getCurlData($url);
$res= json_decode($res, true);
}


if( $res['success'] or !$enable_captcha ){

/* Include login check code */

} else { /* do something else */ }
}
}
?>
