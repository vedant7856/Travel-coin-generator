let generatedLocations = new Set();
let coins = 0;

function generateCoin() {
    const location = document.getElementById('location').value;
    if (location && !generatedLocations.has(location)) {
        generatedLocations.add(location);
        coins++;
        document.getElementById('coins').innerText = Coins: ${coins};
    } else {
        alert('This location already generated a coin or location is empty.');
    }
}

function redeemCoins() {
    if (coins > 0) {
        let qrcodeElement = document.getElementById("qrcode");
        qrcodeElement.innerHTML = ""; // Clear previous QR code, if any
        new QRCode(qrcodeElement, {
            text: "Coins Redeemed",
            width: 128,
            height: 128
        });
        coins = 0;
        document.getElementById('coins').innerText = Coins: ${coins};
    } else {
        alert('No coins to redeem.');
    }
}
