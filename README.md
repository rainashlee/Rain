<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Number Conversion</title>
    <style>
        body{ font-family: Arial, sans-serif;}
        .container {margin: 20px;}  </style></head><body>
    <div class="container">
        <h1>Number Conversion Tool</h1>
        <h2>Number System Results</h2>
        <input type="number" id="numberInput" placeholder="Enter a decimal number" />
        <ul>   <li>Binary: <strong id="binaryResult">-</strong></li>
            <li>Octal: <strong id="octalResult">-</strong></li>
            <li>Hexadecimal: <strong id="hexResult">-</strong></li>
        </ul>
    </div>
 <script>
        const numberInput = document.getElementById('numberInput');
        const binaryResult = document.getElementById('binaryResult');
        const octalResult = document.getElementById('octalResult');
        const hexResult = document.getElementById('hexResult');numberInput.addEventListener('input', () => { const number = parseInt(numberInput.value);
 if (!isNaN(number)) {
                binaryResult.textContent = number.toString(2);
            octalResult.textContent = number.toString(8);
             hexResult.textContent = number.toString(16).toUpperCase();
            } else {
            
   binaryResult.textContent = '-';
                octalResult.textContent = '-';
                hexResult.textContent = '-';   } }) </script>
</body>
</html>
