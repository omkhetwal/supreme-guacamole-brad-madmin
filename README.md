1. Navbar 

```html
<!DOCTYPE html>
<html>

<head>
  <!--Import Google Icon Font-->
  <link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
  <!--Import materialize.css-->
  <link type="text/css" rel="stylesheet" href="css/materialize.min.css" media="screen,projection" />
  <link type="text/css" rel="stylesheet" href="css/main.css" />

  <!--Let browser know website is optimized for mobile-->
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Custom Materialize Theme</title>
</head>

<body>
  <nav class="blue darken-2">
    <div class="container">
      <div class="nav-wrapper">
        <a href="index.html" class="brand-logo">Madmin</a>
        <a href="#" data-activates="side-nav" class="button-collapse show-on-large right">
          <i class="material-icons">menu</i>
        </a>
        <ul class="right hide-on-med-and-down">
          <li class="active">
            <a href="index.html">Dashboard</a>
          </li>
          <li>
            <a href="posts.html">Posts</a>
          </li>
          <li>
            <a href="categories.html">Categories</a>
          </li>
          <li>
            <a href="comments.html">Comments</a>
          </li>
          <li>
            <a href="users.html">Users</a>
          </li>
        </ul>
        <!-- Side nav -->
        <ul id="side-nav" class="side-nav">
          <li>
            <div class="user-view">
              <div class="background">
                <img src="img/ocean.jpg" alt="">
              </div>
              <a href="#">
                <img src="img/person1.jpg" alt="" class="circle">
              </a>
              <a href="#">
                <span class="name white-text">John Doe</span>
              </a>
              <a href="#">
                <span class="email white-text">jdoe@gmail.com</span>
              </a>
            </div>
          </li>
          <li>
            <a href="index.html">
              <i class="material-icons">dashboard</i> Dashboard</a>
          </li>
          <li>
            <a href="posts.html">Posts</a>
          </li>
          <li>
            <a href="categories.html">Categories</a>
          </li>
          <li>
            <a href="comments.html">Comments</a>
          </li>
          <li>
            <a href="users.html">Users</a>
          </li>
          <li>
            <div class="divider"></div>
          </li>
          <li>
            <a class="subheader">Account Controls</a>
          </li>
          <li>
            <a href="login.html" class="waves-effect">Logout</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>








  <!--Import jQuery before materialize.js-->
  <script type="text/javascript" src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
  <script type="text/javascript" src="js/materialize.min.js"></script>
  <script>
    $(document).ready(function () {
      //Init Side nav
      $('.button-collapse').sideNav();

    });
  </script>
</body>

</html>
```



```css

```







# 2. Stats section


```html
<!-- Section  : Stats-->


<section class="section section-stats center">
  <div class="row">
    <div class="col s12 m6 l3">
      <div class="card-panel blue lighten-1 white-text center">
         <i class="material-icons medium">insert_emoticon</i>
         <h5>Monthly Visitors</h5>
          <h3 class="count">28300</h3>
          <div class="progress grey lighten-1">
              <div class="determinate white" style="width: 40%;">
              </div>
          </div>
      </div>
    </div>

      <div class="col s12 m6 l3">
        <div class="card-panel center">
          <i class="material-icons medium">mode_edit</i>
          <h5>Blog posts</h5>
          <h3 class="count">111</h3>
          <div class="progress grey lighten-1">
            <div class="determinate  blue lighten-1" style="width: 20%;">
            </div>
          </div>
        </div>
      </div>

        <div class="col s12 m6 l3">
          <div class="card-panel blue lighten-1 white-text center">
            <i class="material-icons medium">mode_comment</i>
            <h5>Comments</h5>
            <h3 class="count">1200</h3>
            <div class="progress grey lighten-1">
              <div class="determinate white" style="width: 40%;">
              </div>
            </div>
          </div>
        </div>

          <div class="col s12 m6 l3">
            <div class="card-panel center">
              <i class="material-icons medium">supervisor_account</i>
              <h5>Users</h5>
              <h3 class="count">340</h3>
              <div class="progress grey lighten-1">
                <div class="determinate white" style="width: 10%;"></div>
              </div>
            </div>
          </div>
  </div>

</section>


```





# 3   Animation in count

```html

```


**Time Duration**

```js

      $('.count').each(function(){
          $(this).prop('Counter',0).animate({
            Counter:$(this).text()
          },
                  {
                    duration:1200,
                    easing:'swing',
                    step: function (now) {
                      $(this).text(Math.ceil(now));
                    }
                  });
      });

```




**Step 2 for animation**

```javascript

<script>
    $('.section').hide();

    setTimeout(function () {

      $(document).ready(function () {


        // show sections


        $('.section').fadeIn();
        //Init Side nav
        $('.button-collapse').sideNav();



        $('.count').each(function(){
          $(this).prop('Counter',0).animate({
                    Counter:$(this).text()
                  },
                  {
                    duration:1200,
                    easing:'swing',
                    step: function (now) {
                      $(this).text(Math.ceil(now));
                    }
                  });
        });

      });

    },1000)






  </script>
```





---


### Preloader


```html
<!--  Preloader   -->

  <div class="preloader-wrapper big active">
    <div class="spinner-layer spinner-blue-only">
      <div class="circle-clipper left">
        <div class="circle"></div>
      </div><div class="gap-patch">
      <div class="circle"></div>
    </div><div class="circle-clipper right">
      <div class="circle"></div>
    </div>
    </div>
  </div>


```




```css
.loader{
    position: absolute;
    top: 40%;
    left:47%;
}

```




### When section comes in we must hide it


# This ain't working  

```html
<!--  Preloader   -->

  <div class="preloader-wrapper big active">
    <div class="spinner-layer spinner-blue-only">
      <div class="circle-clipper left">
        <div class="circle"></div>
      </div><div class="gap-patch">
      <div class="circle"></div>
    </div><div class="circle-clipper right">
      <div class="circle"></div>
    </div>
    </div>
  </div>














  <!--Import jQuery before materialize.js-->
  <script type="text/javascript" src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
  <script type="text/javascript" src="js/materialize.min.js"></script>
  <script>

   // hide sections

    $('.section').hide();

    setTimeout(function () {

      $(document).ready(function () {
        // show sections

        $('.section').fadeIn();

        // Hide preloader
        $('.loader').fadeOut();

        //Init Side nav
        $('.button-collapse').sideNav();



        $('.count').each(function(){
          $(this).prop('Counter',0).animate({
                    Counter:$(this).text()
                  },
                  {
                    duration:1200,
                    easing:'swing',
                    step: function (now) {
                      $(this).text(Math.ceil(now));
                    }
                  });
        });

      });

    },1000)






  </script>
```



**css**

```css
.loader{
    position: absolute;
    top: 40%;
    left:47%;
}
```






#  Display chart recent comments

```html


<!--  Section : visitors  chart-->

  <div class="section section section-visitors blue lighten-4">
    <div class="row">
      <div class="col s12 m6 l8">
        <div class="card-panel">
          <div id="chartContainer" style="height:300px;width:100%;">
          </div>
        </div>


        <div class="col s12 m6 l4">
          <div class="card-panel">
            <div id="chartContainer" style="height:300px;width:100%;">
            </div>
          </div>

      </div>

    </div>
  </div>


  <script src="https://canvasjs.com/assets/script/canvasjs.min.js"></script>


    <script src="js/chart.js"></script>

```




**Chart js**

```js
window.onload = function () {

        var chart = new CanvasJS.Chart("chartContainer", {
            animationEnabled: true,
            theme: "light2",
            title:{
                text: "Daily visitors"
            },
            axisY:{
                includeZero: false
            },
            data: [{
                type: "line",
                dataPoints: [
                    { y: 450 },
                    { y: 414},
                    { y: 520, indexLabel: "highest",markerColor: "red", markerType: "triangle" },
                    { y: 460 },
                    { y: 450 },
                    { y: 500 },
                    { y: 480 },
                    { y: 480 },
                    { y: 410 , indexLabel: "lowest",markerColor: "DarkSlateGrey", markerType: "cross" },
                    { y: 500 },
                    { y: 480 },
                    { y: 510 }
                ]
            }]
        });
        setTimeout(function () {
            chart.render();
        },1000);

    }


```




# Visitors


```html
<!--  Section : visitors  chart-->

  <div class="section section section-visitors blue lighten-4">
    <div class="row">
      <div class="col s12 m6 l8">
        <div class="card-panel">
          <div id="chartContainer" style="height:300px;width:100%;"></div>
        </div>
      </div>

        <div class="col s12 m6 l4">
<!--          Latest comments-->
          <ul class="collection with-header latest-comments">
            <li class="collection-header">Latest Comments</li>
            <li class="collection-item avatar">
              <img src="img/person1.jpg" alt="" class="circle">
              <span class="title">John Levy</span>
              <p class="truncate">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ab, aperiam blanditiis deserunt doloribus facere fugit illum impedit inventore itaque iure molestias provident quaerat reiciendis repudiandae sunt voluptates voluptatibus? Consequatur, sit!</p>

              <a href="#" class="approve green-text">Approve</a>
              <a href="#" class="deny red-text">Deny</a>

            </li>


            <li class="collection-item avatar">
              <img src="img/person2.jpg" alt="" class="circle">
              <span class="title">John Levy</span>
              <p class="truncate">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ab, aperiam blanditiis deserunt doloribus facere fugit illum impedit inventore itaque iure molestias provident quaerat reiciendis repudiandae sunt voluptates voluptatibus? Consequatur, sit!</p>

              <a href="#" class="approve green-text">Approve</a>
              <a href="#" class="deny red-text">Deny</a>
            </li>



            <li class="collection-item avatar">
              <img src="img/person3.jpg" alt="" class="circle">
              <span class="title">John Levy</span>
              <p class="truncate">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ab, aperiam blanditiis deserunt doloribus facere fugit illum impedit inventore itaque iure molestias provident quaerat reiciendis repudiandae sunt voluptates voluptatibus? Consequatur, sit!</p>

              <a href="#" class="approve green-text">Approve</a>
              <a href="#" class="deny red-text">Deny</a>


            </li>

          </ul>
        </div>
      </div>
  </div>
  
```




