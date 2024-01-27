<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>Shopping Cart</title>
		<link rel="stylesheet" href="style.css" />
	</head>
	<body>
		<div class="app">
			<header>
				<h1>Shopping Cart</h1>
			</header>
			<main>
				<div class="product-list">
					<div class="product">
						<img src="apple.jpg" alt="Apple" />
						<section>
							<p>Apple - $1.50</p>
							<button
								onclick="addToCart('Apple', 1, 1.5)"
								id="apple-cart"
							>
								Add to Cart
							</button>
						</section>
						<p id="apple-count" class="qty">0</p>
					</div>
					<div class="product">
						<img src="banana.jpg" alt="Banana" />
						<section>
							<p>Banana - $0.75</p>
							<button
								onclick="addToCart('Banana', 1, 0.75)"
								id="banana-cart"
							>
								Add to Cart
							</button>
						</section>
						<p id="banana-count" class="qty">0</p>
					</div>
				</div>
				<div class="cart">
					<h2>Your Cart</h2>
					<button
						onclick="applyDiscount('FruitLover')"
						id="discount-btn"
					>
						Apply Discount
					</button>
					<p id="discount-message"></p>
					<button onclick="calculateTotal()" id="checkout">
						Checkout Total
					</button>
					<p id="total-price"></p>
				</div>
			</main>
		</div>
		<script src="utils.js"></script>
		<script src="script.js"></script>
	</body>
</html>

//script.js
let cart = [];
let discountCode;

function addToCart(item, quantity, price) {
	const existingItem = cart.find((cartItem) => cartItem.item === item);
	if (existingItem) {
		existingItem.quantity += quantity;
	} else {
		cart.push({ item, quantity, price });
	}
	document.getElementById(`${item.toLowerCase()}-count`).textContent =
		existingItem ? existingItem.quantity : quantity;
	console.log(`${item} added to cart.`);
}

function applyDiscount(code) {
	// Bug: discountCode should be a number, but it's being stored as a string.
	discountCode = code === "FruitLover" ? 0.1 : 0;

	document.getElementById("discount-message").textContent =
		discountCode === "10"
			? `Discount Applied! ${discountCode}% OFF`
			: "Invalid Discount Code";
	console.log(`Discount code applied: ${code}`);
}

function calculateTotal() {
	let total = 0;
	for (let i = 0; i < cart.length; i++) {
		total += cart[i].quantity * cart[i].price;
	}
	if (discountCode) {
		total = calculateDiscount(total, discountCode);
	}
	document.getElementById(
		"total-price"
	).textContent = `Total: ${formatCurrency(total)}`;
	console.log(`Total: ${formatCurrency(total)}`);
}

//utils.js
function calculateDiscount(price, discount) {
	return price - price * discount;
}

function formatCurrency(amount) {
	return `$${parseFloat(amount).toFixed(2)}`;
}
