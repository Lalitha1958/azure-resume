# azure-resume
My own azure resume

## First steps

- Frontend folder contains the website

```html
<!DOCTYPE html>
<!--[if lt IE 8 ]><html class="no-js ie ie7" lang="en"> <![endif]-->
<!--[if IE 8 ]><html class="no-js ie ie8" lang="en"> <![endif]-->
<!--[if (gte IE 8)|!(IE)]><!--><html class="no-js" lang="en"> <!--<![endif]-->
<head>

   <!--- Basic Page Needs
   ================================================== -->
   <meta charset="utf-8">
	<title>LJ Resume</title>
	<meta name="description" content="">
	<meta name="author" content="">

   <!-- Mobile Specific Metas
   ================================================== -->
	<meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1">

	<!-- CSS
    ================================================== -->
   <link rel="stylesheet" href="css/default.css">
	<link rel="stylesheet" href="css/layout.css">
   <link rel="stylesheet" href="css/media-queries.css">
   <link rel="stylesheet" href="css/magnific-popup.css">

   <!-- Script
   ================================================== -->
   <script src="js/modernizr.js"></script>
   <script src="main.js"></script>

   <!-- Favicons
	================================================== -->
	<link rel="shortcut icon" href="favicon.png" >

</head>

<body>

   <!-- Header
   ================================================== -->
   <header id="home">

      <nav id="nav-wrap">

         <a class="mobile-btn" href="#nav-wrap" title="Show navigation">Show navigation</a>
	      <a class="mobile-btn" href="#" title="Hide navigation">Hide navigation</a>

         <ul id="nav" class="nav">
            <li class="current"><a class="smoothscroll" href="#home">Home</a></li>
            <li><a class="smoothscroll" href="#about">About</a></li>
	         <li><a class="smoothscroll" href="#resume">Resume</a></li>
         </ul> <!-- end #nav -->

      </nav> <!-- end #nav-wrap -->

      <div class="row banner">
         <div class="banner-text">
            <h1 class="responsive-headline">Hi, I'm LJ</h1>
            
            <p>and this page has been viewed <a id="counter"></a> times :) </p> 
            <ul class="social">
               <li><a href="https://www.linkedin.com/in/lalitha-j-685ba121b/"><i class="fa fa-linkedin"></i></a></li>
               <li><a href="https://github.com/Lalitha1958/azure-resume"><i class="fa fa-github"></i></a></li>
            </ul>
         </div>
      </div>

      <p class="scrolldown">
         <a class="smoothscroll" href="#about"><i class="icon-down-circle"></i></a>
      </p>

   </header> <!-- Header End -->


   <!-- About Section
   ================================================== -->
   <section id="about">

      <div class="row">

         <div class="three columns">

            <img class="profile-pic"  src="https://cdn3.vectorstock.com/i/1000x1000/54/32/water-wave-lj-logo-swoosh-letter-lj-logo-design-vector-37075432.jpg" alt="" />

         </div>

         <div class="nine columns main-col">

            <h2>ABOUT ME</h2>

            <p> Hi, I'm LJ, <span>Student at <a href="https://www.mlac-edu.in/">Maharani lakshmi ammanni college for women.</a></span>
               
         </br>
      </br>
       I built this page as part of the <span><a href="https://github.com/Lalitha1958/azure-resume">Future ready Talent Project.</a></span>
            

         </div> <!-- end .main-col -->

      </div>

   </section> <!-- About Section End-->


   <!-- Resume Section
   ================================================== -->
   <section id="resume">

      <!-- Education
      ----------------------------------------------- -->
      <div class="row education">

         <div class="three columns header-col">
            <h1><span>Certifications</span></h1>
         </div>

         <div class="two columns main-col">

            <div class="row item">

               <div class="twelve columns">

                  <h3>Digital Marketing certified</h3>
                  <p class="info"><em class="date">October 2021</em></p>

               </div>

            </div> <!-- item end -->

            <div class="row item">

               <div class="twelve columns">

                  <h3>NCC B certificate</h3>
                  <p class="info"><em class="date">2021</em></p>

               </div>

            </div> <!-- item end -->

            


      

   </section> <!-- Resume Section End-->


   <!-- footer
   ================================================== -->
   <footer>

      <div class="row">

         <div class="twelve columns">

            <ul class="social-links">
               <li><a href="https://www.linkedin.com/in/lalitha-j-685ba121b/"><i class="fa fa-linkedin"></i></a></li>
               <li><a href="https://github.com/Lalitha1958/azure-resume"><i class="fa fa-github"></i></a></li>
            </ul>

            <ul class="copyright">
               <a href="https://www.styleshout.com/free-templates/ceevee/"> Template by CeeVee </a>
                
            </ul>

         </div>

         <div id="go-top"><a class="smoothscroll" title="Back to Top" href="#home"><i class="icon-up-open"></i></a></div>

      </div>

   </footer> <!-- Footer End-->

   <!-- Java Script
   ================================================== -->
   <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
   <script>window.jQuery || document.write('<script src="js/jquery-1.10.2.min.js"><\/script>')</script>
   <script type="text/javascript" src="js/jquery-migrate-1.2.1.min.js"></script>

   <script src="js/jquery.flexslider.js"></script>
   <script src="js/waypoints.js"></script>
   <script src="js/jquery.fittext.js"></script>
   <script src="js/magnific-popup.js"></script>
   <script src="js/init.js"></script>

</body>

</html>
```

- main.js contains visitor counter code

```js
window.addEventListener('DOMContentLoaded', (event) =>{
    getVisitCount();
})

const functionApi = '';

const getVisitCount = () => {
    let count = 30;
    fetch(functionApi).then(response => {
        return response.json()
    }).then(respomse =>{
        console.log("Website called function API.");
        count =  response.count;
        document.getElementById("counter").innerText = count;
    }).catch(function(error){
        console.log(error);
    });
    return count;
}
```