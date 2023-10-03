# MoTicV2
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ticket Purchase Platform</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
        }

        .container {
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        h1 {
            text-align: center;
            color: #333;
        }

        .ticket {
            border: 1px solid #ccc;
            padding: 10px;
            margin: 10px 0;
            background-color: #f9f9f9;
            border-radius: 5px;
        }

        #total {
            font-weight: bold;
        }

        button {
            display: block;
            margin: 20px auto;
            padding: 10px 20px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Ticket Purchase Platform</h1>
        <div class="ticket">
            <h2>Concert Ticket</h2>
            <p>Price: $50</p>
            <label for="quantity">Quantity:</label>
            <input type="number" id="quantity" value="1" min="1">
            <p>Total: $<span id="total">50</span></p>
        </div>
        <button id="purchaseButton">Purchase Tickets</button>
    </div>

    <script>
        // JavaScript to calculate the total price based on the quantity selected
        const quantityInput = document.getElementById('quantity');
        const totalSpan = document.getElementById('total');
        const pricePerTicket = 50;

        quantityInput.addEventListener('input', () => {
            const quantity = parseInt(quantityInput.value);
            const total = quantity * pricePerTicket;
            totalSpan.textContent = total;
        });

        // JavaScript to handle the purchase button click (dummy function)
        const purchaseButton = document.getElementById('purchaseButton');
        purchaseButton.addEventListener('click', () => {
            const quantity = parseInt(quantityInput.value);
            const total = quantity * pricePerTicket;
            alert(`You have purchased ${quantity} ticket(s) for a total of $${total}.`);
        });
    </script>
</body>
</html>
