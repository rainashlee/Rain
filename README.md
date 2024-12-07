<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Number Conversion</title>
</head>
<body>
    <div class="container" id="contentWrapper">
        <h1>Number Conversion Tool</h1>
        <h2>Number System Results</h2>
        <input type="number" id="numberInput" placeholder="Enter a decimal number" />
        <ul>
            <li>Binary: <strong id="binaryResult">-</strong></li>
            <li>Octal: <strong id="octalResult">-</strong></li>
            <li>Hexadecimal: <strong id="hexResult">-</strong></li>
        </ul>
    </div> 
    <script>
        const wrapperinput =document.getElementById('contentWraper');
        const numberInput = document.getElementById('numberInput');
        const binaryResult = document.getElementById('binaryResult');
        const octalResult = document.getElementById('octalResult');
        const hexResult = document.getElementById('hexResult');
     
numberInput.addEventListener('input', () => {
                const number = parseInt(numberInput.value);
if (!isNaN(number))     { 
       binaryResult.textContent = number.toString(2);
       octalResult.textContent =number.toString(8);
       hexResult.textContent = number.toString(16).toUpperCase();
           } else {
  binaryResult.textContent = '-';    octalResult.textContent = '-';
  hexResult.textContent = '-';       
                }
            });
        });
    </script>
</body>
</html>
<nav>
            <ul>
                <li><a href="F1.html">Home</a></li>
                <li><a href="#types">Types of Number Systems</a></li>
                <li><a href="#conversions">Conversions</a></li>
                <li><a href="#resources">Resources</a></li>
            </ul>
        </nav>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Navigation Bar Example</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        .navbar {
            overflow: hidden;
            background-color: #333;
        }
        .navbar a {
            float: left;
            display: block;
            color: #f2f2f2;
            text-align: center;
            padding: 14px 20px;
            text-decoration: none;
        }
        .navbar a:hover {
            background-color: #ddd;
            color: black;
        }
        @media screen and (max-width: 600px) {
            .navbar a {
                float: none;
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="navbar">
        <a href="#home">Home</a>
        <a href="#services">Services</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
    </div>

<div id="home" style="padding:20px 20px;">
        <h2>Home Section</h2>
        <p>Welcome to the home page.</p>
    </div>
    <div id="services" style="padding:20px 20px;">
        <h2>Services Section</h2>
        <p>Here are our services.</p>
    </div>
    <div id="about" style="padding:20px 20px;">
        <h2>About Section</h2>
        <p>Learn more about us.</p>
    </div>
    <div id="contact" style="padding:20px 20px;">
        <h2>Contact Section</h2>
        <p>Contact us here.</p>
    </div>
</body>
</html>

 
