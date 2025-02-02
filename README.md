# Shopping-Website-project
It is a watches shopping website made by using HTML,CSS,Javascript

->login.html

<html>
<head>
<title>Login Form</title>
<style>
button
{
background-color: #4CAF50;
border: none;
color: white;
padding: 15px 32px;
text-align: center;
text-decoration: none;
display: inline-block;
font-size: 16px;
}
.form-container {
display: flex;
flex-direction: column;
align-items: center;
justify-content: center;
height: 100vh;
}

input[type="email"], input[type="password"], input[type="tel"] {
padding: 12px 20px;

margin: 8px 0;
box-sizing: border-box;
border: none;
border-bottom: 2px solid #ccc;
width: 100%;
}

input[type="submit"] {
background-color: #4CAF50;
color: white;
padding: 14px 20px;
margin: 8px 0;
border: none;
border-radius: 4px;
cursor: pointer;
width: 100%;
}

input[type="submit"]:hover {
background-color: #45a049;
}
.invalid {
border: 2px solid red;
}
p
{
font-size:40px;
color:blue;
}
</style>
</head>
<body bgcolor=aquamarine>
<div class="form-container">
<p>Login Form</p>
<form id="loginForm" onsubmit="return validateForm()" method="post"
action="mainpg.html">
<label for="email">Email</label>
<input type="email" id="email" name="email" placeholder="Enter email">
<label for="password">Password</label>
<input type="password" id="password" name="password" placeholder="Enter
password">
<label for="phone">Phone Number</label>
<input type="tel" id="phone" name="phone" placeholder="Enter phone number">
<button onclick="mainpg.html">Submit</button>

</form>
</div>
<script>
function validateForm() {
var email = document.forms["loginForm"]["email"].value;
var password = document.forms["loginForm"]["password"].value;
var phone = document.forms["loginForm"]["phone"].value;

// Check if email, password, and phone are empty
if (email == "" || password == "" || phone == "") {
alert("Please fill in all fields.");
return false;
}
// Check email syntax
var emailRegex = /^\S+@\S+\.\S+$/;
if (!emailRegex.test(email)) {
alert("Please enter a valid email address.");
document.getElementById("email").classList.add("invalid");
return false;
}
// Check phone number syntax
var phoneRegex = /^\d{10}$/;
if (!phoneRegex.test(phone)) {
alert("Please enter a valid phone number.");
document.getElementById("phone").classList.add("invalid");
return false;
}
// Check password syntax
var passwordRegex =
/^(?=.*\d)(?=.*[a-z])(?=.*[A-Z])(?=.*[!@#$%^&*])[0-9a-zA-Z!@#$%^&*]{8,}$/;
if (!passwordRegex.test(password)) {
alert("Password must be at least 8 characters long and contain at least one special
character,one uppercase letter, one lowercase letter, and one number.");
document.getElementById("password").classList.add("invalid");
return false;
}
return true;

}
</script>

</body>
</html>


->mainpg.html

<html>
<head>
<title>
Home Page</title>
<style>
b
{
color:aquamarine;
}
a
{
font-size:25px;
color:red;
}
pre
{
font-size:25px;
color:brown;
}
p
{
font-size:50px;
text-align:center;
background-color:blue;
color:yellow;
}
u
{
color:red;
}
</style>
</head>
<body bgcolor=yellow>

<nav><pre>
<a href="home.html">Home</a> <a href="address.html">Shipping Address</a> <a
href="Payment.html">Payment</a>
</pre>
</nav>
<p><b>Almedo Watches Shopping Website!</b></p>

<a href="home.html">Go To shop!</a>
<br>
<img align="middle" class="BuyNow" src="C:\Users\a\Downloads\buynow.jpg" width="700"
height="300" >

<pre>
<u>Almedo Watches Online Shopping Store</u>
Contact Details:
Mobile No:8895246212
E-mail:<a href="mailto:almedowatches@gmail.com">almedowatches@gmail.com</a>
</pre>
</body>
</html>

->home.html

<html>
<head>
<title>
Home Page</title>
<style>
button
{
background-color: #4CAF50; /* Green */
border: none;
color: white;
padding: 15px 32px;
text-align: center;
text-decoration: none;
display: inline-block;
font-size: 16px;
}
h2
{
color:brown;
font-size:30px;
}
h1
{
color:blue;
font-size:30px;
}
pre
{
text-align:left;

}
table
{
background-color:aquamarine;
}
b
{
background-color:linen;
color:red;
font-size:40px;
margin-left:200px;
}
img
{
display: block;
margin-left: auto;
margin-right: auto;
height:250px;
width:250px;
}
a
{
font-size:40px;
}
h2
{
text-align:center;
color:purple;
}
</style>
</head>
<body bgcolor="yellow">
<pre>
<a href="mainpg.html">Main Page</a>
</pre>
<h1><b><u><p>Welcome to the Online Almedo Watches Shopping Store</u></b></p>
<h2><i><u><p>Select your watch</u></i></p></h2>
</h1>
<br>
<table border="3" bordercolor=blue cellpadding="5" cellspacing="5" style="width:100%">
<th>
<pre>
<h1>Company:Noise
Model:Grey Noise Smart-Watch
Price:5600/-

</h1>
</pre>
<img
src="https://assets.myntassets.com/h_200,w_200,c_fill,g_auto/h_1440,q_100,w_1080/v1/as
sets/images/12514718/2020/11/2/aa8fdeda-eb6d-4f4e-8b22-23917b9479721604304380593
-Garmin-Venu-Light-SandRose-Gold-5651604304379738-1.jpg">
<a href="address.html" id="test" class="btn btn-info" role="button">Buy Now</a>
</th>
<th>
<pre>
<h1>
Company:Titan Raga
Model:Raga Viva Analog Dial
Women's watch
Price:3505/-
</h1>
</pre>
<img src="https://m.media-amazon.com/images/I/61KmHWU3MrL._AC_UL320_.jpg">
<span><a href="address.html" id="test" class="btn btn-info" role="button">Buy
Now</a></span>
</th>
<th>
<h1>
<pre>
Company:Titan Rado
Model:Titan Analog Black Dial
Men's Watch
Price:5495/-
</pre>
</h1>
<img src="https://m.media-amazon.com/images/I/41Eae2BvcsL.jpg">
<a href="address.html" id="test" class="btn btn-info" role="button">Buy Now</a>
<style>
#test
{
color:white;
background-color:green;
text-decoration: none;
font-weight:normal;
}
</style>
</pre>
</th>
<br>
</html>

->address.html

<html>
<head>
<title>
Shipping address</title>
<style>
h1
{
color:yellow;
background-color:blue;
margin-left:100px;
margin-right:100px;
text-align:center;
}
h3
{
color:purple;
}
a
{
font-size:30px;
color:red;
}
</style>
</head>
<body bgcolor=cyan>
<a href="mainpg.html">Go to Main page</a>
<form onsubmit="return validateForm()">
<h1>Shipping Address</h1>
<pre>
<h3><label for="name">Name:</label><input type="text" id="name" name="name"
required><br><br>
<label for="address">Address:</label><input type="text" id="address" name="address"
required><br><br>
<label for="city">City:</label><input type="text" id="city" name="city" required><br><br>
<label for="state">State:</label><input type="text" id="state" name="state"
required><br><br>
<label for="pin">Pin Code:</label><input type="text" id="pin" name="pin" required
pattern="[0-9]{6}" title="Please
enter a valid 6-digit pin code"></h3>
</pre><p>Proceed for payment!</p>
<a href="Payment.html" id="test" class="btn btn-info" role="button"><span>Submit</span>
</a>
<style>
label
{
font-size:20px;
}

p
{
font-size:25px;
}
#test
{
color:white;
background-color:green;
text-decoration: none;
font-weight:normal;
}
span
{
font-weight:15px;
}
</body>
</html>

->payment.html

<html>
<head><title>Payment</title>
<style>
h1
{
color:yellow;
background-color:blue;
margin-left:100px;
margin-right:100px;
text-align:center;
}
h3
{
color:purple;
}
</style>
</head>
<body bgcolor=cyan>
<h1>Payment Details</h1>
<h3><label for="card">Card Number:</label>
<input type="text" id="card" name="card" required pattern="[0-9]{16}"
title="Please enter a valid 16-digit card number"><br><br>
<label for="expiration">Expiration Date:</label>
<input type="text" id="expiration" name="expiration" required pattern="(0[1-
9]|1[0-2])\/([0-9]{4}|[0-9]{2})" title="Please enter a valid expiration date in the

format MM/YYYY"><br><br>
<label for="cvv">CVV:</label>
<input type="text" id="cvv" name="cvv" required pattern="[0-9]{3}" title="Please
enter a valid 3-digit CVV code"></h3><br><br>
<button onclick="alertify()">Submit</button>
</form>
<script>
function alertify()
{
alert("Thanks for shopping,visit again!");
}
function validateForm() {
let pin = document.getElementById("pin");
let card = document.getElementById("card");
let expiration = document.getElementById("expiration");
let cvv = document.getElementById("cvv");
let valid = true;
if (!zip.checkValidity()) {
valid = false;
alert("Please enter a valid 5-digit zip code.");
}
if (!card.checkValidity()) {
valid = false;
alert("Please enter a valid 16-digit card number.");
}
if (!expiration.checkValidity()) {
valid = false;
alert("Please enter a valid expiration date in the format MM/YYYY.");
}
if (!cvv.checkValidity()) {
valid = false;
alert("Please enter a valid 3-digit CVV code.");
}
return valid;
}
</script>
</body>
</html>
