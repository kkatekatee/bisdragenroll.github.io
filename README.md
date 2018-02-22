<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!--
Design by TEMPLATED
http://templated.co
Released for free under the Creative Commons Attribution License

Name       : Mongoose
Description: A two-column, fixed-width design with dark color scheme.
Version    : 1.0
Released   : 20130920

-->
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title></title>
<meta name="keywords" content="" />
<meta name="description" content="" />
<link href="http://fonts.googleapis.com/css?family=Source+Sans+Pro:200,300,400,600,700,900" rel="stylesheet" />
<link href="default.css" rel="stylesheet" type="text/css" media="all" />
<link href="fonts.css" rel="stylesheet" type="text/css" media="all" />

<!--[if IE 6]><link href="default_ie6.css" rel="stylesheet" type="text/css" /><![endif]-->
<style>
body {font-family: Arial, Helvetica, sans-serif;}
form {border: 3px solid #f1f1f1;}

input[type=text], input[type=password] {
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid #ccc;
    box-sizing: border-box;
}

button {
    background-color: #4CAF50;
    color: white;
    padding: 14px 20px;
    margin: 8px 0;
    border: none;
    cursor: pointer;
    width: 100%;
}

button:hover {
    opacity: 0.8;
}


.container {
    padding: 16px;
}

span.psw {
    float: right;
    padding-top: 16px;
}

/* Change styles for span and cancel button on extra small screens */
@media screen and (max-width: 300px) {
    span.psw {
       display: block;
       float: none;
    }
    .cancelbtn {
       width: 100%;
    }
}
</style>

</head>
<body>
<div id="header-wrapper">
<div id="header" class="container">
	<div id="logo">
		<h1><a href="#"><strong>BIS DRAG ENROLL</strong></a></h1>
	</div>
	<div id="menu">

			<li><a href="index.html" accesskey="5" title="">Log In	</a></li>
		</ul>
	</div>
</div></div>
<div id="page" class="container">
	<div id="content">
		<div class="title">
			<h2>Welcome to our website</h2>
			<span class="byline">Login</span> </div>
<!-- login -->



<form>

  <div class="w3-container w3-half">

    <label for="uname"><b>Username</b></label>
    <input id="uname" type="text" placeholder="Enter Username" name="uname" required>

    <label for="psw"><b>Password</b></label>
    <input id="psw" type="password" placeholder="Enter Password" name="psw" required>

    <button id="signIn" type="submit" onclick="singIn()"><a href="index02.html">Login</a></button>
    <label>
      <input type="checkbox" checked="checked" name="remember"> Remember me
    </label>
  </div>

</form>
	</div>
<!-- End login -->
<!-- Script -->
<script src="https://www.gstatic.com/firebasejs/4.10.0/firebase.js"></script>
<script>
  // Initialize Firebase
  var config = {
    apiKey: "AIzaSyDSetigw0vfCj7c-IlpzYXMh74PN2mByEs",
    authDomain: "my-project-1517970809956.firebaseapp.com",
    databaseURL: "https://my-project-1517970809956.firebaseio.com",
    projectId: "my-project-1517970809956",
    storageBucket: "my-project-1517970809956.appspot.com",
    messagingSenderId: "91235408501"
  };
  firebase.initializeApp(config);
</script>

<script>
function signIn() {
  var username = document.getElementById('uname').value;
  var password = document.getElementById('psw').value;
  firebase.auth().SignInWithUserAndPassword(username, password).catch(function (error){
    var errorCode = error.code;
    var erroreMessage = error.message;
    if (errorCode === 'auth/weak-password'){
      alert('Wrong password');
    } else {
      alert(errorMessage);
    }
    console.log(error);
  });
  alert('logged in')
}
</script>

<!-- End Script -->


	<div id="sidebar">
		<ul class="style1">
			<li class="first">
				<h3>...</h3>
				<p>xxxx</p>
			</li>


	</div>
</div>
<div id="copyright">
	<p>&copy; Untitled. All rights reserved. | Photos by <a href="http://fotogrph.com/">Fotogrph</a> | Design by <a href="http://templated.co" rel="nofollow">TEMPLATED</a>.</p>
</div>
</body>
</html>
