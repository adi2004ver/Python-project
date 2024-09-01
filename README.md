# Python-project webpage
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Order Management</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        h1 {
            text-align: center;
        }
        .logo {
            text-align: center;
            margin-bottom: 20px;
        }
        .logo img {
            width: 150px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-bottom: 20px;
        }
        table, th, td {
            border: 1px solid #ddd;
        }
        th, td {
            padding: 10px;
            text-align: left;
        }
        th {
            background-color: #f2f2f2;
        }
        .total {
            text-align: right;
            margin-top: 20px;
        }
        .total span {
            font-weight: bold;
        }
        button {
            display: block;
            width: 100%;
            padding: 10px;
            font-size: 16px;
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>

    <div class="logo">
        <img src="srm_logo.png" alt="SRM University Logo">
    </div>

    <h1>GREEN CANTEEN</h1>
    <h2>Place Your Order<span style='font-size:50px;'>&#8595;</span></h2>

    <form id="order-form">
        <table>
            <thead>
                <tr>
                    <th>Item</th>
                    <th>Price</th>
                    <th>Quantity</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Sandwich</td>
                    <td>₹50</td>
                    <td><input type="number" id="sandwich-quantity" min="0" value="0"></td>
                </tr>
                <tr>
                    <td>Pasta</td>
                    <td>₹70</td>
                    <td><input type="number" id="pasta-quantity" min="0" value="0"></td>
                </tr>
                <tr>
                    <td>Burger</td>
                    <td>₹80</td>
                    <td><input type="number" id="burger-quantity" min="0" value="0"></td>
                </tr>
                <tr>
                    <td>Fries</td>
                    <td>₹40</td>
                    <td><input type="number" id="fries-quantity" min="0" value="0"></td>
                </tr>
                <tr>
                    <td>Coffee</td>
                    <td>₹30</td>
                    <td><input type="number" id="coffee-quantity" min="0" value="0"></td>
                </tr>
                <tr>
                    <td>Tea</td>
                    <td>₹20</td>
                    <td><input type="number" id="tea-quantity" min="0" value="0"></td>
                </tr>
                <tr>
                    <td>Juice</td>
                    <td>₹35</td>
                    <td><input type="number" id="juice-quantity" min="0" value="0"></td>
                </tr>
            </tbody>
        </table>

        <div class="total">
            <span>Total: ₹<span id="total-amount">0</span></span>
        </div>

        <button type="button" onclick="calculateTotal()">Calculate Total</button>
    </form>

    <script>
        function calculateTotal() {
            var sandwichPrice = 50;
            var pastaPrice = 70;
            var burgerPrice = 80;
            var friesPrice = 40;
            var coffeePrice = 30;
            var teaPrice = 20;
            var juicePrice = 35;

            var sandwichQuantity = document.getElementById('sandwich-quantity').value;
            var pastaQuantity = document.getElementById('pasta-quantity').value;
            var burgerQuantity = document.getElementById('burger-quantity').value;
            var friesQuantity = document.getElementById('fries-quantity').value;
            var coffeeQuantity = document.getElementById('coffee-quantity').value;
            var teaQuantity = document.getElementById('tea-quantity').value;
            var juiceQuantity = document.getElementById('juice-quantity').value;

            var total = (sandwichPrice * sandwichQuantity) +
                        (pastaPrice * pastaQuantity) +
                        (burgerPrice * burgerQuantity) +
                        (friesPrice * friesQuantity) +
                        (coffeePrice * coffeeQuantity) +
                        (teaPrice * teaQuantity) +
                        (juicePrice * juiceQuantity);

            document.getElementById('total-amount').textContent = total;
        }
    </script>

</body>
</html>
