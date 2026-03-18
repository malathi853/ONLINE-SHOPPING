# ONLINE-SHOPPING
About online shopping website
<!DOCTYPE html><html>
<head>
<title>Online Shopping</title>
<style>
body {font-family: Arial; margin:0;}
.nav {background:#333; padding:10px; color:white;}
.nav button {margin:5px;}
.page {display:none; padding:20px;}
.active {display:block;}
input {margin:5px; padding:5px;}
.product {border:1px solid #ccc; padding:10px; margin:10px; display:inline-block;}
</style>
</head>
<body><div class="nav">
<button onclick="showPage('welcome')">Home</button>
<button onclick="showPage('login')">Login</button>
<button onclick="showPage('products')">Products</button>
<button onclick="showPage('payment')">Payment</button>
<button onclick="showPage('feedback')">Feedback</button>
</div><!-- Welcome Page --><div id="welcome" class="page active">
<h2>Welcome to Online Shopping</h2>
<p>Shop your favorite items easily!</p>
</div><!-- Login Page --><div id="login" class="page">
<h2>Login</h2>
<input type="text" id="username" placeholder="Username"><br>
<input type="password" id="password" placeholder="Password"><br>
<button onclick="login()">Login</button>
<p id="loginMsg"></p>
</div><!-- Products Page --><div id="products" class="page">
<h2>Clothing</h2>
<div class="product">Saree</div>
<div class="product">Choli</div>
<div class="product">Lehenga</div>
<div class="product">Jean</div>
<div class="product">Crop Tops</div><h2>Accessories</h2>
<div class="product">Mobile</div>
<div class="product">Bluetooth</div>
<div class="product">AirPods</div>
<div class="product">Laptop</div>
</div><!-- Payment Page --><div id="payment" class="page">
<h2>Payment</h2>
<input type="text" placeholder="Card Number"><br>
<input type="text" placeholder="Expiry Date"><br>
<input type="text" placeholder="CVV"><br>
<button onclick="pay()">Pay Now</button>
<p id="payMsg"></p>
</div><!-- Feedback Page --><div id="feedback" class="page">
<h2>Feedback</h2>
<textarea placeholder="Enter your feedback"></textarea><br>
<button onclick="thankyou()">Submit</button>
<p id="thankMsg"></p>
</div><script>
function showPage(pageId) {
  let pages = document.getElementsByClassName('page');
  for (let i = 0; i < pages.length; i++) {
    pages[i].classList.remove('active');
  }
  document.getElementById(pageId).classList.add('active');
}

function login() {
  let user = document.getElementById('username').value;
  let pass = document.getElementById('password').value;
  if(user && pass) {
    document.getElementById('loginMsg').innerText = "Login Successful";
  } else {
    document.getElementById('loginMsg').innerText = "Enter details";
  }
}

function pay() {
  document.getElementById('payMsg').innerText = "Payment Successful";
}

function thankyou() {
  document.getElementById('thankMsg').innerText = "Thank you for your feedback!";
}
</script></body>
</html>
