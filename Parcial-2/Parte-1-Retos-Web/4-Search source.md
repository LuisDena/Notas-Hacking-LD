# Search source
## Objetivo
The developer of this website mistakenly left an important artifact in the website source, can you find it?The website is [here](http://saturn.picoctf.net:59405/)
## Pistas
P1:How could you mirror the website on your local machine so you could use more powerful tools for searching?

## Datos de acceso al nivel
```bash
Usuario: Dena
Contraseña: Notedigo
```
## Solución
```bash
Pass siguiente lvl:picoCTF{1nsp3ti0n_0f_w3bpag3s_8de925a7}
-------------------------------------------------------
Entramos a la pagina y inspeccionamos el codigo fuente de la misma donde encontraremos un comentario y buscamos por todos los archivos que ahí se encuentrar, exploramos todos para finalmente encontrarlo en el de css
--------------------------------------------------------
|   |   |
|---|---|
||<!DOCTYPE html>|
||<html lang="en">|
|||
||<head>|
||<!-- basic -->|
||<meta charset="utf-8">|
||<meta http-equiv="X-UA-Compatible" content="IE=edge">|
||<!-- mobile metas -->|
||<meta name="viewport" content="width=device-width, initial-scale=1">|
||<meta name="viewport" content="initial-scale=1, maximum-scale=1">|
||<!-- site metas -->|
||<title>flexed</title>|
||<meta name="keywords" content="">|
||<meta name="description" content="">|
||<meta name="author" content="">|
||<!-- bootstrap css -->|
||<link rel="stylesheet" href="[css/bootstrap.min.css](http://saturn.picoctf.net:59405/css/bootstrap.min.css)">|
||<!-- owl css -->|
||<link rel="stylesheet" href="[css/owl.carousel.min.css](http://saturn.picoctf.net:59405/css/owl.carousel.min.css)">|
||<!-- style css -->|
||<link rel="stylesheet" href="[css/style.css](http://saturn.picoctf.net:59405/css/style.css)">|
||<!-- responsive-->|
||<link rel="stylesheet" href="[css/responsive.css](http://saturn.picoctf.net:59405/css/responsive.css)">|
||<!-- awesome fontfamily -->|
||<link rel="stylesheet" href="[https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css)">|
||<!--[if lt IE 9]>|
||<script src="https://oss.maxcdn.com/html5shiv/3.7.3/html5shiv.min.js"></script>|
||<script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script><![endif]-->|
||</head>|
||<!-- body -->|
|||
||<body class="main-layout">|
||<!-- loader -->|
||<div class="loader_bg">|
||<div class="loader"><img src="[images/loading.gif](http://saturn.picoctf.net:59405/images/loading.gif)" alt="" /></div>|
||</div>|
|||
||<div class="wrapper">|
||<!-- end loader -->|
|||
||<div id="content">|
||<!-- header -->|
||<header>|
||<!-- header inner -->|
||<div class="head-top">|
||<div class="container">|
|||
||<div class="row">|
||<div class="col-xl-4 col-lg-4 col-md-4 col-sm-4">|
||<div class="email">|
||<a href="[#](http://saturn.picoctf.net:59405/index.html#)"><img src="[images/mail_icon.png](http://saturn.picoctf.net:59405/images/mail_icon.png)" /> Email : demo@gmail.com</a>|
||</div>|
||</div>|
||<div class="col-xl-4 col-lg-4 col-md-4 col-sm-4">|
||<div class="logo">|
||<a href="[index.html](http://saturn.picoctf.net:59405/index.html)"><img src="[images/logo.png](http://saturn.picoctf.net:59405/images/logo.png)" /></a>|
||</div>|
||</div>|
||<div class="col-xl-4 col-lg-4 col-md-4 col-sm-4">|
||<div class="contact_nu">|
||<a href="[#](http://saturn.picoctf.net:59405/index.html#)"> <img src="[images/phone_icon.png](http://saturn.picoctf.net:59405/images/phone_icon.png)" /> Contact : +71 71234567</a>|
||</div>|
||</div>|
||</div>|
||</div>|
||</div>|
||<div class="bg">|
||<div class="container">|
||<nav class="navigation navbar-expand-md navbar-dark ">|
|||
||<button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarsExample04" aria-controls="navbarsExample04" aria-expanded="false" aria-label="Toggle navigation">|
||<span class="navbar-toggler-icon"></span>|
||</button>|
|||
||<div class="collapse navbar-collapse" id="navbarsExample04">|
||<ul class="navbar-nav mr-auto">|
||<li class="nav-item active">|
||<a class="nav-link" href="[index.html](http://saturn.picoctf.net:59405/index.html)">Home <span class="sr-only">(current)</span></a>|
||</li>|
||<li class="nav-item">|
||<a class="nav-link" href="[#about](http://saturn.picoctf.net:59405/index.html#about)">About </a>|
||</li>|
||<li class="nav-item">|
||<a class="nav-link" href="[#yoga](http://saturn.picoctf.net:59405/index.html#yoga)"> Yoga</a>|
||</li>|
||<li class="nav-item">|
||<a class="nav-link" href="[#pricing](http://saturn.picoctf.net:59405/index.html#pricing)">Pricing</a>|
||</li>|
||<li class="nav-item">|
||<a class="nav-link" href="[#online](http://saturn.picoctf.net:59405/index.html#online)">Yoga Online</a>|
||</li>|
|||
||<li class="nav-item">|
||<a class="nav-link" href="[#contact](http://saturn.picoctf.net:59405/index.html#contact)">Contact us</a>|
||</li>|
|||
||</ul>|
||</div>|
||</nav>|
||</div>|
||</div>|
||<!-- end header inner -->|
||</header>|
||<!-- end header -->|
||<!-- start slider section -->|
||<div class="slider_section banner_main">|
||<div id="myCarousel" class="carousel slide" data-ride="carousel">|
||<ol class="carousel-indicators">|
||<li data-target="#myCarousel" data-slide-to="0" class="active"></li>|
||<li data-target="#myCarousel" data-slide-to="1"></li>|
||<li data-target="#myCarousel" data-slide-to="2"></li>|
||</ol>|
||<div class="carousel-inner">|
||<div class="carousel-item active">|
||<img class="first-slide" src="[images/banner.jpg](http://saturn.picoctf.net:59405/images/banner.jpg)" alt="First slide">|
||<div class="container">|
||<div class="carousel-caption relative">|
||<h1>Gather<br>|
||<strong class="dark_brown">New Body Energy</strong></h1>|
|||
||<a href="[#](http://saturn.picoctf.net:59405/index.html#)">contact us</a>|
||</div>|
||</div>|
||</div>|
||<div class="carousel-item">|
||<img class="second-slide" src="[images/banner.jpg](http://saturn.picoctf.net:59405/images/banner.jpg)" alt="Second slide">|
||<div class="container">|
||<div class="carousel-caption relative">|
||<h1>Gather<br>|
||<strong class="dark_brown">New Body Energy</strong></h1>|
|||
||<a href="[#](http://saturn.picoctf.net:59405/index.html#)">contact us</a>|
||</div>|
||</div>|
||</div>|
||<div class="carousel-item">|
||<img class="third-slide" src="[images/banner.jpg](http://saturn.picoctf.net:59405/images/banner.jpg)" alt="Third slide">|
||<div class="container">|
||<div class="carousel-caption relative">|
||<h1>Gather<br>|
||<strong class="dark_brown">New Body Energy</strong></h1>|
|||
||<a href="[#](http://saturn.picoctf.net:59405/index.html#)">contact us</a>|
||</div>|
||</div>|
||</div>|
||</div>|
||<a class="carousel-control-prev" href="[#myCarousel](http://saturn.picoctf.net:59405/index.html#myCarousel)" role="button" data-slide="prev">|
||<span class="carousel-control-prev-icon" aria-hidden="true"></span>|
||<span class="sr-only">Previous</span>|
||</a>|
||<a class="carousel-control-next" href="[#myCarousel](http://saturn.picoctf.net:59405/index.html#myCarousel)" role="button" data-slide="next">|
||<span class="carousel-control-next-icon" aria-hidden="true"></span>|
||<span class="sr-only">Next</span>|
||</a>|
||</div>|
||</div>|
||<!-- end slider section -->|
|||
||<!-- six_box|
||end six_box The flag is not here but keep digging :)-- >|
|||
||<!-- We Do Yogas -->|
||<div id="yoga" class="weyoga">|
||<div class="container">|
||<div class="row">|
||<div class="col-md-12">|
||<div class="title">|
||<h2>How to <strong class="black"> We Do Yogas</strong></h2>|
||</div>|
||</div>|
||</div>|
||<div class="row">|
||<div class="col-xl-3 col-lg-3 col-md-3 col-sm-12">|
||<div class="yogo_three_box">|
||<figure><img src="[images/1.png](http://saturn.picoctf.net:59405/images/1.png)" alt="#" /></figure>|
||<h3>Ashtanga Yoga</h3>|
||<p>simply dummy text of the printing and typesetting industry. Lorem </p>|
||</div>|
||</div>|
||<div class="col-xl-4 col-lg-4 col-md-4 col-sm-12">|
||<div class="yogo_three_box">|
||<figure><img src="[images/2.png](http://saturn.picoctf.net:59405/images/2.png)" alt="#" /></figure>|
||<h3>Hatha Yoga</h3>|
||<p>simply dummy text of the printing|
||<br>and typesetting industry. Lorem </p>|
||</div>|
||</div>|
||<div class="col-xl-5 col-lg-5 col-md-5 col-sm-12">|
||<div class="yogo_three_box">|
||<figure><img src="[images/3.png](http://saturn.picoctf.net:59405/images/3.png)" alt="#" /></figure>|
||<h3>Kundalini Yoga</h3>|
||<p>simply dummy text of the printing|
||<br>and typesetting industry. Lorem </p>|
||</div>|
||</div>|
||<a class="readmore" href="[#](http://saturn.picoctf.net:59405/index.html#)">Read More</a>|
||</div>|
||</div>|
||</div>|
||<!-- end We Do Yogas -->|
|||
||<!-- footer -->|
||<div id="contact" class="contact">|
||<div class="container">|
||<div class="row">|
||<div class="col-md-12">|
||<div class="title">|
||<h2>Contact<strong class="black"> Us</strong></h2>|
||</div>|
||</div>|
||</div>|
||</div>|
||</div>|
||<div class="container-fluid">|
|||
||<div class="row">|
||<div class="col-xl-6 col-lg-6 col-md-6 col-sm-12 padding">|
|||
||<form class="main_form">|
||<div class="row">|
|||
||<div class="col-xl-12 col-lg-12 col-md-12 col-sm-12">|
||<input class="form-control" placeholder="Name" type="text" name="Name">|
||</div>|
||<div class="col-xl-12 col-lg-12 col-md-12 col-sm-12">|
||<input class="form-control" placeholder="Email" type="text" name="Email">|
||</div>|
||<div class="col-xl-12 col-lg-12 col-md-12 col-sm-12">|
||<input class="form-control" placeholder="Phone" type="text" name="Phone">|
||</div>|
||<div class="col-xl-12 col-lg-12 col-md-12 col-sm-12">|
||<textarea class="textarea" placeholder="Message" type="text" name="Message"></textarea>|
||</div>|
||<div class="col-xl-12 col-lg-12 col-md-12 col-sm-12">|
||<button class="send">Send</button>|
||</div>|
||<div class="col-xl-12 col-lg-12 col-md-12 col-sm-12">|
||<ul class="mail-icon">|
||<li><img src="[images/phone_icon.png](http://saturn.picoctf.net:59405/images/phone_icon.png)" /> (+71) 75896472 (+72) 258963475</li>|
||<li><img src="[images/mail_icon.png](http://saturn.picoctf.net:59405/images/mail_icon.png)" /> Demo@gmail.com</li>|
|||
||</ul>|
||</div>|
||<div class="col-xl-12 col-lg-12 col-md-12 col-sm-12">|
||<ul class="social_icon">|
||<li> <a href="[#](http://saturn.picoctf.net:59405/index.html#)"><i class="fa fa-facebook-f"></i></a></li>|
||<li> <a href="[#](http://saturn.picoctf.net:59405/index.html#)"><i class="fa fa-twitter"></i></a></li>|
||<li> <a href="[#](http://saturn.picoctf.net:59405/index.html#)"><i class="fa fa-instagram"></i></a></li>|
||</ul>|
||</div>|
||</div>|
||</form>|
||</div>|
|||
||<div class="col-xl-6 col-lg-6 col-md-6 col-sm-12 padddd">|
||<div class="map_section">|
||<div id="map">|
||</div>|
||</div>|
||</div>|
||</div>|
||</div>|
||</div>|
|||
||</div>|
||<footer>|
||<div class="footer">|
||<div class="copyright">|
||<div class="container">|
||<div class="row">|
||<div class="col-xl-12 col-lg-12 col-md-12 col-sm-12">|
||<p>© 2019 Flexed Design by<a href="[https://html.design/](https://html.design/)"> Free Html Template</a></p>|
||</div>|
||</div>|
||</div>|
||</div>|
||</div>|
||</footer>|
||<!-- end footer -->|
||</div>|
||</div>|
||<div class="overlay"></div>|
||<!-- Javascript files-->|
||<script src="[js/jquery.min.js](http://saturn.picoctf.net:59405/js/jquery.min.js)"></script>|
||<script src="[js/popper.min.js](http://saturn.picoctf.net:59405/js/popper.min.js)"></script>|
||<script src="[js/bootstrap.bundle.min.js](http://saturn.picoctf.net:59405/js/bootstrap.bundle.min.js)"></script>|
||<script src="[js/owl.carousel.min.js](http://saturn.picoctf.net:59405/js/owl.carousel.min.js)"></script>|
||<script src="[js/custom.js](http://saturn.picoctf.net:59405/js/custom.js)"></script>|
||<script src="[js/jquery.mCustomScrollbar.concat.min.js](http://saturn.picoctf.net:59405/js/jquery.mCustomScrollbar.concat.min.js)"></script>|
|||
||<script src="[js/jquery-3.0.0.min.js](http://saturn.picoctf.net:59405/js/jquery-3.0.0.min.js)"></script>|
||<script type="text/javascript">|
||$(document).ready(function() {|
||$("#sidebar").mCustomScrollbar({|
||theme: "minimal"|
||});|
|||
||$('#dismiss, .overlay').on('click', function() {|
||$('#sidebar').removeClass('active');|
||$('.overlay').removeClass('active');|
||});|
|||
||$('#sidebarCollapse').on('click', function() {|
||$('#sidebar').addClass('active');|
||$('.overlay').addClass('active');|
||$('.collapse.in').toggleClass('in');|
||$('a[aria-expanded=true]').attr('aria-expanded', 'false');|
||});|
||});|
||</script>|
|||
||<script>|
||// This example adds a marker to indicate the position of Bondi Beach in Sydney,|
||// Australia.|
||function initMap() {|
||var map = new google.maps.Map(document.getElementById('map'), {|
||zoom: 11,|
||center: {|
||lat: 40.645037,|
||lng: -73.880224|
||},|
||});|
|||
||var image = 'images/maps-and-flags.png';|
||var beachMarker = new google.maps.Marker({|
||position: {|
||lat: 40.645037,|
||lng: -73.880224|
||},|
||map: map,|
||icon: image|
||});|
||}|
||</script>|
||<!-- google map js -->|
||<script src="[https://maps.googleapis.com/maps/api/js?key=AIzaSyA8eaHt9Dh5H57Zh0xVTqxVdBFCvFMqFjQ&callback=initMap](https://maps.googleapis.com/maps/api/js?key=AIzaSyA8eaHt9Dh5H57Zh0xVTqxVdBFCvFMqFjQ&callback=initMap)"></script>|
||<!-- end google map js -->|
|||
||</body>|
|||
||</html>|
--------------------------------------------------------style.css
/*--------------------------------------------------------------------- File Name: style.css ---------------------------------------------------------------------*/
/*--------------------------------------------------------------------- import Fonts ---------------------------------------------------------------------*/
 @import url('https://fonts.googleapis.com/css?family=Rajdhani:300,400,500,600,700');
 @import url('https://fonts.googleapis.com/css?family=Poppins:100,100i,200,200i,300,300i,400,400i,500,500i,600,600i,700,700i,800,800i,900,900i');
 @import url('https://fonts.googleapis.com/css?family=Raleway:100,100i,200,200i,300,300i,400,400i,500,500i,600,600i,700,700i,800,800i,900,900i');
/*--------------------------------------------------------------------- basic ---------------------------------------------------------------------*/
 body {
     color: #666666;
     font-size: 14px;
     font-family: 'Roboto';
     line-height: 1.80857;
     font-weight: normal;
}
 html {
     scroll-behavior: smooth;
}

 button:focus {
     outline: none;
}
 ul, li, ol {
     margin: 0px;
     padding: 0px;
     list-style: none;
}
 p {
     margin: 0px;
     font-weight: 300;
     font-size: 15px;
     line-height: 24px;
}
 a {
     color: #222222;
     text-decoration: none;
     outline: none !important;
}
 a, .btn {
     text-decoration: none !important;
     outline: none !important;
     -webkit-transition: all .3s ease-in-out;
     -moz-transition: all .3s ease-in-out;
     -ms-transition: all .3s ease-in-out;
     -o-transition: all .3s ease-in-out;
     transition: all .3s ease-in-out;
}
 img {
     max-width: 100%;
     height: auto;
}
 :focus {
     outline: 0;
}
 .btn-custom {
     margin-top: 20px;
     background-color: transparent !important;
     border: 2px solid #ddd;
     padding: 12px 40px;
     font-size: 16px;
}
 .lead {
     font-size: 18px;
     line-height: 30px;
     color: #767676;
     margin: 0;
     padding: 0;
}
 .form-control:focus {
     border-color: #ffffff !important;
     box-shadow: 0 0 0 .2rem rgba(255, 255, 255, .25);
}
 .navbar-form input {
     border: none !important;
}
 .badge {
     font-weight: 500;
}
 blockquote {
     margin: 20px 0 20px;
     padding: 30px;
}
 button {
     border: 0;
     margin: 0;
     padding: 0;
     cursor: pointer;
}
 .full {
     float: left;
     width: 100%;
}
 .layout_padding {
     padding-top: 90px;
     padding-bottom: 90px;
}
 .layout_padding_2 {
     padding-top: 75px;
     padding-bottom: 75px;
}
 .light_silver {
     background: #f9f9f9;
}
 .theme_bg {
     background: #38c8a8;
}
 .margin_top_30 {
     margin-top: 30px !important;
}
 .full {
     width: 100%;
     float: left;
     margin: 0;
     padding: 0;
}
/**-- heading section --**/
 .main_heading {
     text-align: center;
     display: flex;
     justify-content: center;
     position: relative;
     margin-bottom: 50px;
}
 .main_heading h2 {
     padding: 0;
     font-size: 48px;
     line-height: 60px;
     font-weight: 400;
     position: relative;
     letter-spacing: -0.5px;
     color: #114c7d;
     border-left: solid #38c8a8 10px;
     padding-left: 15px;
}
 .main_heading h2 strong {
     background: #38c8a8;
     color: #fff;
     font-weight: 600;
     padding: 0 15px;
     line-height: 68px;
}
 .white_heading_main h2 {
     color: #fff;
}
 .small_main_heading {
     margin-top: 25px;
     float: left;
     width: 100%;
     border-bottom: solid rgba(0, 0, 0, 0.07) 1px;
     margin-bottom: 25px;
}
 .small_main_heading h2 {
     padding: 2px 0 20px 0;
     color: #114c7d;
     font-weight: 400;
     font-size: 28px;
     background-image: url('../images/fevicon.png');
     background-repeat: no-repeat;
     padding-left: 55px;
     letter-spacing: -0.5px;
}
 .small_main_heading h2 strong {
     color: #38c8a8;
     font-weight: 600;
}
 .main_bt {
     background: #38c8a8;
     color: #fff;
     padding: 8px 25px 8px 20px;
     float: left;
     font-size: 15px;
     font-weight: 300;
     border-left: solid #114c7d 5px;
     border-radius: 0;
}
 a.readmore_bt {
     color: #fff;
     font-weight: 300;
     text-decoration: underline !important;
}
 .main_bt:hover, .main_bt:focus {
     background: #114c7d;
     border-left: solid #38c8a8 5px;
     color: #fff;
}
 .margin_top_50 {
     margin-top: 50px;
}
 .margin_bottom_30_all {
     margin-bottom: 30px;
}
 .text_align_center {
     text-align: center;
}
/*---------------------------- preloader area ----------------------------*/
 .loader_bg {
     position: fixed;
     z-index: 9999999;
     background: #fff;
     width: 100%;
     height: 100%;
}
 .loader {
     height: 100%;
     width: 100%;
     position: absolute;
     left: 0;
     top: 0;
     display: flex;
     justify-content: center;
     align-items: center;
}
 .loader img {
     width: 280px;
}
/*--------------------------------------------------------------------- header ---------------------------------------------------------------------*/
 header {
     min-height: 90px;
     background: transparent;
     padding-top: 15px;
     position: absolute;
     width: 100%;
     top: 0;
     left: 0;
     z-index: 998;
}
 header .container-fluid {
     max-width: 1850px;
}
 .right_header_info {
     width: 100%;
     float: left;
     padding: 20px 0 0;
}
 .right_header_info ul {
     list-style: none;
     padding: 0;
     margin: 0;
     float: right;
}
 .right_header_info ul li {
     display: inline;
     font-size: 16px;
     margin-left: 45px;
     color: #eaeaea;
     font-weight: 400;
     float: left;
}
 .right_header_info ul li a {
     color: #eaeaea;
     font-weight: 300;
}
 .button_user a {
     float: left;
     min-width: 75px;
     height: 35px;
     text-align: center;
     line-height: 35px;
     position: relative;
     top: -3px;
     padding: 0 15px;
     margin: 0 2px;
}
 .button_user a {
     float: left;
     min-width: 75px;
     height: 40px;
     text-align: center;
     line-height: 38px;
     position: relative;
     top: -7px;
     padding: 0 15px;
     margin: 0 2px;
     border: solid #eaeaea 1px;
}
 .button_user a:hover, .button_user a:focus, .button_user a.active {
     background: #e3d105;
     color: #fff;
     border-color: #e3d105;
     color: #222;
}
 #sidebarCollapse {
     background: transparent;
}
 .slider_section {
     min-height: 100vh;
     padding-bottom: 100px;
}
 .contact_nu {
    float: right;
}
/** menu section **/
 .head-top {
     padding-bottom: 20px;
}
 .email {
     padding-top: 31px;
}
 .email a {
    font-size: 16px;
}
 .email a:hover {
     color: #000;
}
 .email img {
    padding-right: 10px;
}
 .contact_nu {
     padding-top: 31px;
}
 .contact_nu a {
    font-size: 16px;
}
 .contact_nu a:hover {
     color: #000;
}
 .contact_nu img {
    padding-right: 10px;
}
 .bg {
    background-color: #5ab337d6;
}

 .navbar-expand-md .navbar-nav .nav-link {
     padding: 15px 48px;
     font-size: 16px;
     color: #000;
     line-height: 18px;
}
/** banner_main picoCTF{1nsp3ti0n_0f_w3bpag3s_8de925a7} **/
 .carousel-indicators li {
     width: 20px;
     height: 20px;
     border-radius: 11px;
     background-color: #070000;
}
 .carousel-indicators li.active {
    background-color: #35a30a;
}
 .carousel-indicators {
     left: inherit;
     top: 53%;
     width: 20px;
     display: block;
}
 .carousel-indicators li {
     margin: 8px 0;
}
 .banner_main {
     position: relative;
}
 .relative {
    position: absolute;
     top: 50%;
     transform: translateY(-50%);
     bottom: auto;
     text-align: left;
}
 .banner_main .carousel-caption h1 {
    color:#35a30a;
     font-size: 124px;
     line-height: 120px;
     font-weight: 500;
     padding-bottom: 85px;
}
 .dark_brown {
    color: #000000;
     font-weight: 500;
}
 .banner_main .carousel-caption a {
    display: block;
     background: #fff;
     color: #050000;
     max-width: 230px;
     padding: 12px 0px;
     width: 100%;
     font-size: 18px;
     text-align: center;
     text-transform: uppercase;
     font-weight: 500;
     border: #35a30a solid 1px;
}
 .banner_main .carousel-caption a:hover {
     background: #58c62c;
     color: #fff;
}
 .carousel-control-prev-icon {
    display: none;
}
 .carousel-control-next-icon {
    display: none;
}
 .banner_main .carousel-item img {
    width: 100%;
}
 .slider_section {
     min-height: inherit;
}


 .title {
     text-align: center;
     padding-bottom: 60px;
}
 .title h2 {
     font-size: 60px;
     font-weight: normal;
     line-height: 46px;
     color: #58c62c;
     padding-bottom: 20px;
}

/** contact **/
 .black {
     color: #000;
     font-weight: normal;
}
 .contact {
     margin-top: 90px;
}
 .contact .title {
     padding-bottom: 60px;
     text-align: left;
}
 .contact .title h2 {
     font-size: 60px;
     font-weight: normal;
     line-height: 46px;
     color: #58c62c;
     padding: 0;
}
 #map {
     height: 100%;
     min-height: 480px;
}
 .main_form {
     background: #13240c;
     padding: 40px 63px;
     padding-left: 224px;
}
 .form-control {
     border-radius: inherit;
     margin-bottom: 20px;
     padding: 8px 2px;
     background: transparent;
     border-bottom: #fff solid 1px !important;
     border: transparent;
}
 .form-control:focus {
     box-shadow: inherit;
     background: transparent;
     border-bottom: #fff solid 1px !important;
}
 .textarea {
     background: transparent;
     border-bottom: #fff solid 1px !important;
     border: transparent;
     padding-top: 6px;
     width: 100%;
     color: #fff;
     opacity: 1;
}
 .send {
     font-family: poppins;
     float: right;
     margin: 0 auto;
     display: block;
     background: #fff;
     color: #000;
     max-width: 120px;
     padding: 6px 0px;
     width: 100%;
     font-size: 18px;
     margin-top: 20px 
}
 .send:hover {
     background: #35a30a ;
     color: #fff;
}
 .padddd {
    padding-left: 0px;
     padding-right: 0;
}
 .map_section {
     height: 100%;
}
 .padding {
    padding-right: 0px;
     padding-left: 0;
}

/** end contact **/
/** footer **/
 .copyright {
     background: #317914;
}
 .copyright p {
     color: #fff;
     text-align: center;
     padding: 25px 0px;
     font-size: 17px;
}
 .copyright a {
     color: #fff;
}
 .copyright a:hover {
     color: #000;
}
/** end footer **/
/*--------------------------------------------------------------------- ener page css ---------------------------------------------------------------------*/
```
## Notas Adicionales

| Comando  | Descripción | 
|------------|--------------|

## Referencias 
