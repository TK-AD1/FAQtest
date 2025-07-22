
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>アジャストワンFAQ</title>
  <style>
    body {
      margin: 0;
      font-family: "Segoe UI", "Helvetica Neue", sans-serif;
      background: linear-gradient(135deg, #0e1624, #1b2a45);
      color: #f0f4f8;
      padding: 0 20px 50px;
    }

    header {
      text-align: center;
      padding: 30px 20px 10px;
    }

    header img {
      max-width: 180px;
      height: auto;
    }

    h2 {
      font-size: 28px;
      margin-top: 10px;
      color: #ffffff;
      letter-spacing: 1px;
    }

    #searchBox {
      display: block;
      width: 100%;
      max-width: 400px;
      margin: 30px auto 20px;
      padding: 10px 14px;
      border-radius: 8px;
      font-size: 16px;
      border: none;
      background-color: #eaeef2;
      color: #333;
    }

    .faq-toggle {
      background-color: #212c42;
      margin: 15px 0;
      padding: 14px 18px;
      font-weight: 600;
      font-size: 17px;
      border-radius: 10px;
      cursor: pointer;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 3px 8px rgba(0,0,0,0.3);
      transition: background 0.3s;
    }

    .faq-toggle:hover {
      background-color: #2a3958;
    }

    .faq-content {
      display: none;
      padding: 18px;
      margin-top: -10px;
      background-color: #2f3e59;
      border-left: 4px solid #00bcd4;
      border-radius: 0 0 10px 10px;
      animation: fadeIn 0.4s ease-in;
    }

    .faq-content p {
      margin: 0;
    }

    .layer {
      margin-left: 15px;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-5px); }
      to   { opacity: 1; transform: translateY(0); }
    }
  </style>
</head>
<body>

  <header>
    <img src="your-logo.png" alt="AdjustOne Logo" />
    <h2>アジャストワンFAQ</h2>
  </header>

  <input type="text" id="searchBox" placeholder="🔍 キーワードで検索" oninput="filterFaq()" />

  <div class="faq-toggle" onclick="toggle(this)">オフィスラインについて 🔽</div>
  <div class="faq-content layer">

    <div class="faq-toggle" onclick="toggle(this)">セルフページについて 🔽</div>
    <div class="faq-content layer">

      <div class="faq-toggle" onclick="toggle(this)">セルフページで出来ることは？ 🔽</div>
      <div class="faq-content layer">
        <p><strong>Q:</strong> セルフページで設定できることは？<br>
        <strong>A:</strong> 無条件転送・スケジュール転送・着信拒否（有償）などが可能です。<br>
        詳しくは 0120-874-839 へお問い合わせください。</p>
      </div>

      <div class="faq-toggle" onclick="toggle(this)">自社で設定されたい場合 🔽</div>
      <div class="faq-content layer">
        <p><strong>Q:</strong> 自社で設定したい場合<br>
        <strong>A:</strong> 一度 0120-874-839 までお問い合わせください。</p>
      </div>

    </div>

    <div class="faq-toggle" onclick="toggle(this)">カスコンについて 🔽</div>
    <div class="faq-content layer">
      <div class="faq-toggle" onclick="toggle(this)">利用可能な機能 🔽</div>
      <div class="faq-content layer">
        <p><strong>Q:</strong> 設定できる機能は？<br>
        <strong>A:</strong> ファーストスケジュール・着信先変更などが利用可能です。</p>
      </div>
    </div>

  </div>

  <script>
    function toggle(element) {
      const content = element.nextElementSibling;
      const isVisible = content.style.display === "block";
      content.style.display = isVisible ? "none" : "block";
      element.textContent = isVisible
        ? element.textContent.replace("🔼", "🔽")
        : element.textContent.replace("🔽", "🔼");
    }

    function filterFaq() {
      const keyword = document.getElementById("searchBox").value.toLowerCase();
      const sections = document.querySelectorAll(".faq-toggle, .faq-content");
      sections.forEach(el => {
        el.style.display = el.textContent.toLowerCase().includes(keyword) ? "" : "none";
      });
    }
  </script>

</body>
</html>
