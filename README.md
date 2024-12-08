<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Number Conversion Tool</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            min-height: 100vh;
            background: url(gojo.gif) no-repeat center center fixed;
            background-size: cover;
            display: flex;
            flex-direction: column;
        }

        .content {
            flex: 1;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .container {
            background-color: rgba(238, 130, 238, 0.2);
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            max-width: 800px;
            width: 100%;
            margin: 20px 0;
            display: flex;
            flex-direction: row;
            border: 2px solid white;
        }

        .input-section, .table-section {
            flex: 1;
            margin: 10px;
        }

        input[type="number"] {
            width: calc(100% - 22px);
            padding: 10px;
            margin: 15px 0;
            font-size: 16px;
            border: 1px solid #ced4da;
            border-radius: 4px;
        }

        ul {
            list-style-type: none;
            padding: 0;
        }

        li {
            margin: 10px 0;
            font-size: 18px;
        }

        strong {
            color: #007bff;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
            font-size: 14px;
        }

        table th, table td {
            border: 1px solid #ccc;
            text-align: center;
            padding: 8px;
        }

        table th {
            background-color: #007bff;
            color: white;
        }

        .header {
            width: 100%;
            padding: 20px;
            background-color: #007bff;
            color: #ffffff;
            text-align: center;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }

        footer {
            text-align: center;
            padding: 10px;
            background-color: #007bff;
            color: #fff;
            width: 100%;
            position: relative;
            bottom: 0;
        }

        button {
            padding: 10px 20px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        button:hover {
            background-color: #0056b3;
        }

        .header, .content, footer {
            background: rgba(255, 255, 255, 0.8);
        }

        h1, p {
            color: black;
        }
    </style>
</head>

<body>
    <div class="header">
        <h1>Number Conversion Tool</h1>
        <p>Convert Decimal Numbers into Binary, Octal, and Hexadecimal</p>
    </div>

    <div class="content">
        <div class="container">
            <div class="input-section">
                <h2>Enter a Decimal Number</h2>
                <input type="number" id="numberInput" placeholder="Enter a decimal number" />

                <ul>
                    <li>Binary: <strong id="binaryResult">-</strong></li>
                    <li>Octal: <strong id="octalResult">-</strong></li>
                    <li>Hexadecimal: <strong id="hexResult">-</strong></li>
                </ul>
                <button id="clearBtn">Clear</button>
            </div>

            <div class="table-section">
                <h3>Table of Number Systems</h3>
                <table>
                    <thead>
                        <tr>
                            <th>Decimal</th>
                            <th>Binary</th>
                            <th>Hexadecimal</th>
                            <th>Octal</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr><td>0</td><td>0000</td><td>0</td><td>0</td></tr>
                        <tr><td>1</td><td>0001</td><td>1</td><td>1</td></tr>
                        <tr><td>2</td><td>0010</td><td>2</td><td>2</td></tr>
                        <tr><td>3</td><td>0011</td><td>3</td><td>3</td></tr>
                        <tr><td>4</td><td>0100</td><td>4</td><td>4</td></tr>
                        <tr><td>5</td><td>0101</td><td>5</td><td>5</td></tr>
                        <tr><td>6</td><td>0110</td><td>6</td><td>6</td></tr>
                        <tr><td>7</td><td>0111</td><td>7</td><td>7</td></tr>
                        <tr><td>8</td><td>1000</td><td>8</td><td>10</td></tr>
                        <tr><td>9</td><td>1001</td><td>9</td><td>11</td></tr>
                        <tr><td>10</td><td>1010</td><td>A</td><td>12</td></tr>
                        <tr><td>11</td><td>1011</td><td>B</td><td>13</td></tr>
                        <tr><td>12</td><td>1100</td><td>C</td><td>14</td></tr>
                        <tr><td>13</td><td>1101</td><td>D</td><td>15</td></tr>
                        <tr><td>14</td><td>1110</td><td>E</td><td>16</td></tr>
                        <tr><td>15</td><td>1111</td><td>F</td><td>17</td></tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>

    <footer>
        <p>&copy; 2024 Number Conversion Tool. All rights reserved.</p>
    </footer>

    <script>
        const numberInput = document.getElementById('numberInput');
        const binaryResult = document.getElementById('binaryResult');
        const octalResult = document.getElementById('octalResult');
        const hexResult = document.getElementById('hexResult');
        const clearBtn = document.getElementById('clearBtn');

        numberInput.addEventListener('input', () => {
            const number = parseInt(numberInput.value);

            if (!isNaN(number)) {
                binaryResult.textContent = number.toString(2);
                octalResult.textContent = number.toString(8);
                hexResult.textContent = number.toString(16).toUpperCase();
            } else {
                binaryResult.textContent = '-';
                octalResult.textContent = '-';
                hexResult.textContent = '-';
            }
        });

        clearBtn.addEventListener('click', () => {
            numberInput.value = '';
            binaryResult.textContent = '-';
            octalResult.textContent = '-';
            hexResult.textContent = '-';
        });
    </script>
</body>

</html>
