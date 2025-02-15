<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>ভ্যালেন্টাইন্স ডে ১০০ জিবি অফার! 💝</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f8f9fa;
      text-align: center;
    }
    header {
      background-color: #ff4081;
      color: white;
      padding: 15px;
      font-size: 1.5em;
    }
    .container {
      max-width: 90%;
      margin: 20px auto;
      padding: 15px;
      background: white;
      box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
      border-radius: 10px;
    }
    .progress-bar {
      width: 100%;
      height: 10px;
      background: #ddd;
      border-radius: 5px;
      margin: 20px 0;
    }
    .progress {
      width: 5%;
      height: 100%;
      background: #4CAF50;
      transition: width 0.3s ease-in-out;
    }
    .countdown {
      font-size: 1.8em;
      color: red;
      font-weight: bold;
    }
    .share-btn {
      background: #007BFF;
      color: white;
      border: none;
      padding: 12px;
      width: 100%;
      border-radius: 5px;
      font-size: 1.2em;
      cursor: pointer;
      margin-top: 10px;
    }
    .share-links a {
      display: block;
      background: #007BFF;
      color: white;
      text-decoration: none;
      padding: 10px;
      border-radius: 5px;
      margin: 5px 0;
    }
  </style>
</head>
<body>

  <header>
    💖 ১০০ জিবি ভ্যালেন্টাইন্স ডে অফার! 💖</header>

  <div class="container">
    <h2>100GB MB আনলক করুন!</h2>
    <p>শুধু ১০০ বার শেয়ার করুন ও MB আনলক করুন!</p>

    <div class="progress-bar">
      <div class="progress" id="progress"></div>
    </div>

    <p id="shareCount">0 / 100 Shares</p>

    <button class="share-btn" id="shareButton">📤 Share Now</button>
    <p class="countdown" id="countdown">10</p>

    <div class="share-links" id="shareLinks">
      <p>Share via:</p>
      <a href="#" id="facebookShare" target="_blank">Facebook</a>
      <a href="#" id="whatsappShare" target="_blank">WhatsApp</a>
      <a href="#" id="telegramShare" target="_blank">Telegram</a>
    </div>
  </div>

  <script>
    let shares = 0;
    const maxShares = 100;
    const progress = document.getElementById("progress");
    const shareButton = document.getElementById("shareButton");
    const shareCount = document.getElementById("shareCount");
    const countdown = document.getElementById("countdown");
    const shareLinks = document.getElementById("shareLinks");

    function updateProgress() {
      let progressPercent = Math.min((shares / maxShares) * 100, 100);
      progress.style.width = progressPercent + "%";
      shareCount.textContent = `${shares} / ${maxShares} Shares`;
      if (shares >= maxShares) {
        shareButton.disabled = true;
        shareButton.textContent = "✅ Goal Achieved!";
      }
    }

    shareButton.addEventListener("click", () => {
      shares++;
      updateProgress();
    });

    const shareUrl = encodeURIComponent(window.location.href);
    const shareText = encodeURIComponent("১০০ জিবি MB আনলক করতে এই ওয়েবসাইটটি ১০০ বার শেয়ার করুন!");

    document.getElementById("facebookShare").href = `https://www.facebook.com/sharer/sharer.php?u=${shareUrl}`;
    document.getElementById("whatsappShare").href = `https://wa.me/?text=${shareText}%20${shareUrl}`;
    document.getElementById("telegramShare").href = `https://t.me/share/url?url=${shareUrl}&text=${shareText}`;
  </script>
</body>
</html>
