# movie-prediction-web-application-usinng-data-mining-
<!DOCTYPE html>
<html>
<title></title>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Poppins">
<style>
body,h1,h2,h3,h4,h5 {font-family: "Poppins", sans-serif}
body {font-size:16px;}
.w3-half img{margin-bottom:-6px;margin-top:16px;opacity:0.8;cursor:pointer}
.w3-half img:hover{opacity:1}
h2,p{color:red;}
p1{color:red;}
</style>
<body>
<nav class="w3-sidebar w3-black w3-collapse w3-top w3-large w3-padding" style="z-index:3;width:300px;font-weight:bold;" id="mySidebar"><br>
  <a href="javascript:void(0)" onclick="w3_close()" class="w3-button w3-hide-large w3-display-topleft" style="width:100%;font-size:22px">Close Menu</a>
  <div class="w3-container">
    <h3 class="w3-padding-64"><b>Movie<br>Prediction</b></h3>
  </div>
  <div class="w3-bar-block">

    <a href="#" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white">Home</a> 
    <a href="http://www.imdb.com/" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white">*IMDB</a>
    <a href="upcoming.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white">Rating for upcoming movies</a> 
    <a href="#services" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white">comedy</a> 
    <a href="#designers" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white">horror</a> 
    <a href="#packages" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white">fiction</a> 
    <a href="#contact" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white">thriller</a>
    <a href="graph.html" onclick="w3_close()" class="w3-bar-item w3-button w3-hover-white">Pie chart</a>
  </div>
</nav>
<!---------------------------------------------------------------------------------------------------------------------->

<script>
function rating()//for released movie
{
  var imdb; 
  imdb =   Number(document.getElementById("movie").value);
  budget = Number(document.getElementById("cost").value);

  if((imdb>=9 && imdb<=10)&& (budget>0))
  {
    alert("This is a superhit Movie Go for it !");
  }

  if((imdb>=7 && imdb<=9) && (budget<1000))
  {
    alert("This is a hit Movie Go for it");
  }

  if((imdb>=5 && imdb<=7) && (budget<1000))
  {
    alert("This is a Average movie!");
  }

  if((imdb>=3 && imdb<=5) && (budget<1000))
  {
    alert("Sorry This is a flop movie IMDB rating is too low");
  }

  if((imdb>=0 && imdb<=3) && (budget<1000))
  {
    alert("underrated");
  }

  if(imdb<10 &&  budget>1000)
  {
    alert("budget exceeded!");
  }
}
</script>

<!-- regression claculation-->

<!-- Top menu on small screens -->
<header class="w3-container w3-top w3-hide-large w3-black w3-xlarge w3-padding">
  <a href="javascript:void(0)" class="w3-button w3-yellow w3-margin-right" onclick="w3_open()">&#9776;</a>
  <span>BOX OffiCe</span>
</header>

<!-- Overlay effect when opening sidebar on small screens -->
<div class="w3-overlay w3-hide-large" onclick="w3_close()" style="cursor:pointer" title="close side menu" id="myOverlay"></div>

<!-- !PAGE CONTENT! -->
<div class="w3-main" style="margin-left:340px;margin-right:40px">


<div class="w3-container">
  <h2>Predicting your movie</h2><!--for upcoming movie-->
  <br>

  <button onclick="document.getElementById('id01').style.display='block'" class="w3-button w3-red">check status for released movie</button>
  <div id="id01" class="w3-modal w3-animate-opacity">
    <div class="w3-modal-content w3-card-4">
     
        <span onclick="document.getElementById('id01').style.display='none'" 
        class="w3-button w3-large w3-display-topright">&times;</span>
        <h2></h2>
      </header>
      <div class="w3-container">
    
<p>
<input class="w3-input" type="text" name="name" style="width:90%" required>
<label>Name of the movie</label>
</p>

<p>
<input class="w3-input" type="text" name="imdb" id="movie" style="width:90%" required>
<label>*IMDB Rating</label>
</p>

<p>
<input class="w3-input" type="text" name="budget" id="cost" style="width:90%" required>
<label>Budget(In crore)</label>
</p>
<br>
<p>
<select class="w3-select" id="genre" name="option">
  <option value="" disabled selected><p>Choose Genre</p></option>
  <option value="1">Action</option>
  <option value="2">Comedy</option>
  <option value="3">Drama</option>
  <option value="4">Horror</option>
  <option value="5">Thriller</option>
  <option value="6">Romantic</option>
</select>
</p>
<p>
<button onclick="rating()">Click me</button>
</p>
    </div>
    </div>
  </div>
</div>
<!---------------------------------------------------------------------------------------------------------------------->
    <!--upcoming movie-->
    <script>
function upcoming_rating()//for upcoming  movies

{
  var actor;
  var cost_of_making;
  var type; 
  actor= Number(document.getElementById("actors").value);
  cost_of_making = Number(document.getElementById("cost").value);
  type = Number(document.getElementById("genre").value);

  if((imdb>=9 && imdb<=10)&& (budget>0))
  {
    alert("This is a superhit Movie Go for it !");
  }

  if((imdb>=7 && imdb<=9) && (budget<1000))
  {
    alert("This is a hit Movie Go for it");
  }

  if((imdb>=5 && imdb<=7) && (budget<1000))
  {
    alert("This is a Average movie!");
  }

  if((imdb>=3 && imdb<=5) && (budget<1000))
  {
    alert("Sorry This is a flop movie IMDB rating is too low");
  }

  if((imdb>=0 && imdb<=3) && (budget<1000))
  {
    alert("underrated");
  }

  if(imdb<10 &&  budget>1000)
  {
    alert("budget exceeded!");
  }
}
</script>
<div class="w3-container">

   
<!---------------------------------------------------------------------------------------------------------------------->
  <!-- Header -->
  <div class="w3-container" style="margin-top:80px" id="showcase">
  
   
    <hr style="width:50px;border:5px solid red" class="w3-round">
  </div>
  
  <!-- Photo grid (modal) -->
  <div class="w3-row-padding">
    <div class="w3-half">
        <img src="int.jpg" style="width:100%" onclick="onClick(this)" alt="*IMDB (9.0/10) SCIENCE-FICTION SUPERHIT ">
      <img src="bat.jpg" style="width:100%" onclick="onClick(this)" alt="*IMDB (9.0/10)   ACTION    SUPERHIT">
      <img src="maxresdefault.jpg" style="width:100%" onclick="onClick(this)" alt="IMDB(8/10) ACTION SUPERHIT">
        <img src="pad1.jpg" style="width:100%" onclick="onClick(this)" alt="*IMDB (6/10) Fiction HIT">
          <img src="jawani.jpg" style="width:100%" onclick="onClick(this)" alt="IMDB 8/10 Romantic HIT">
          <img src="beyond.jpg" style="width:100%" onclick="onClick(this)" alt="IMDB 8/10 Animation HIT">

    </div>

    <div class="w3-half">
      <img src="ram.jpg" style="width:100%" onclick="onClick(this)" alt="*IMDB (7.6/10)     Classical Drama and History    Superhit">
      <img src="lunch.jpg" style="width:100%" onclick="onClick(this)" alt="IMDB 8/10  Drama HIT Won OSCAR AWARD">
      <img src="logan.jpg" style="width:100%" onclick="onClick(this)" alt="IMDB 8.7/10 ACTION SUPERHIT">
      <img src="ana.jpg" style="width:100%" onclick="onClick(this)" alt="*IMDB (6.5/10)    HORROR   HIT  ">
      <img src="lion.jpg" style="width:100%" onclick="onClick(this)" alt="IMDB 8/10 Roamantic HIT">
      
    </div>
  </div>

  <!-- Modal for full size images on click-->
  <div id="modal01" class="w3-modal w3-black" style="padding-top:0" onclick="this.style.display='none'">
    <span class="w3-button w3-black w3-xxlarge w3-display-topright">&times;</span>
    <div class="w3-modal-content w3-animate-zoom w3-center w3-transparent w3-padding-64">
      <img id="img01" class="w3-image">
      <p id="caption"></p>
    </div>
  </div>

  <!-- Services -->
  <div class="w3-container" id="services" style="margin-top:75px">
    <h1 class="w3-xxxlarge w3-text-black"><b>Our Services.</b></h1>
    <hr style="width:290px;border:5px solid red" class="w3-round">
    <p color="red">We are predicting the movie based on some facts and figures and analyse your data on some excellent data mining techniques.Data from the Internet Movie Database (IMDB) was gleaned and various data mining and prediction techniques such as multi-linear regression, regression tree and K-nearest neighbors were used to devise a model that can predict an Indian movie’s ranking with an RMSE of 1.5 on a scale of 1 to 10. </p>
    <p>
    </p>
  </div>
  
  
<div class="w3-content w3-display-container">
   <img class="mySlides" src="swadesh1.jpg" style="width:100%">
   <img class="mySlides" src="bat.jpg" style="width:100%">
  <img class="mySlides" src="maxresdefault.jpg" style="width:100%">
  <img class="mySlides" src="iron1.jpg" style="width:100%">
 

  <button class="w3-button w3-black w3-display-left" onclick="plusDivs(-1)">&#10094;</button>
  <button class="w3-button w3-black w3-display-right" onclick="plusDivs(1)">&#10095;</button>
</div>      

  <!-- Contact -->
  <div class="w3-container" id="contact" style="margin-top:75px">
    <h1 class="w3-xxxlarge w3-text-green"><b>Contact Us.</b></h1>
    <hr style="width:290px;border:5px solid red" class="w3-round">
  
    <form action="/action_page.php" target="_blank">
      <div class="w3-section">
        <label>Name</label>
        <input class="w3-input w3-border" type="text" name="Name" required>
      </div>
      <div class="w3-section">
        <label>Email</label>
        <input class="w3-input w3-border" type="text" name="Email" required>
      </div>
      <div class="w3-section">
        <label>Message</label>
        <input class="w3-input w3-border" type="text" name="Message" required>
      </div>
      <button type="submit" class="w3-button w3-block w3-padding-large w3-red w3-margin-bottom">Send Message</button>
    </form>  
  </div>

</div>




<script>

function w3_open() {
    document.getElementById("mySidebar").style.display = "block";
    document.getElementById("myOverlay").style.display = "block";
}
 
function w3_close() {
    document.getElementById("mySidebar").style.display = "none";
    document.getElementById("myOverlay").style.display = "none";
}

// Modal Image Gallery
function onClick(element) {
  document.getElementById("img01").src = element.src;
  document.getElementById("modal01").style.display = "block";
  var captionText = document.getElementById("caption");
  captionText.innerHTML = element.alt;
}

</script>
<script>
var slideIndex = 1;
showDivs(slideIndex);

function plusDivs(n) {
  showDivs(slideIndex += n);
}

function showDivs(n) {
  var i;
  var x = document.getElementsByClassName("mySlides");
  if (n > x.length) {slideIndex = 1}    
  if (n < 1) {slideIndex = x.length}
  for (i = 0; i < x.length; i++) {
     x[i].style.display = "none";  
  }
  x[slideIndex-1].style.display = "block";  
}
</script>

</body>
</html>
