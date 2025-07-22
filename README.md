
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>アジャストワンFAQ</title>
  <style>
    body {
      margin: 0;
      font-family: "Segoe UI", "Helvetica Neue", sans-serif;
      background: linear-gradient(to right, #101923, #1a2738);
      color: #1c1c1c;
      padding: 0 20px 50px;
    }

    header {
      text-align: center;
      padding: 40px 20px 10px;
    }

    header img {
      max-width: 220px;
      height: auto;
    }

    h2 {
      font-size: 28px;
      margin-top: 10px;
      color: #f0f4f8;
      letter-spacing: 1px;
    }

    #searchBox {
      display: block;
      width: 100%;
      max-width: 400px;
      margin: 30px auto 30px;
      padding: 12px 16px;
      border-radius: 10px;
      font-size: 16px;
      border: none;
      background-color: #ffffff;
      color: #333;
      box-shadow: 0 3px 8px rgba(0,0,0,0.2);
    }

    .faq-toggle {
      background-color: #ffffff;
      margin: 15px auto;
      padding: 18px 20px;
      font-weight: 600;
      font-size: 17px;
      border-radius: 12px;
      cursor: pointer;
      max-width: 800px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      transition: transform 0.2s ease;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .faq-toggle:hover {
      transform: scale(1.02);
      background-color: #f1f3f5;
    }

    .faq-content {
      display: none;
      padding: 20px;
      background-color: #f9f9fb;
      border-left: 4px solid #00acc1;
      border-radius: 0 0 12px 12px;
      max-width: 760px;
      margin: -10px auto 30px;
      box-shadow: inset 0 0 4px rgba(0,0,0,0.04);
      animation: fadeIn 0.3s ease;
    }

    .faq-content p {
      margin: 0;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(-5px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .layer {
      margin-left: 20px;
    }

    @media screen and (max-width: 600px) {
      .faq-toggle, .faq-content {
        padding: 16px;
      }

      #searchBox {
        width: 90%;
      }
    }
  </style>
</head>
<body>

  <header>
    <img src="logo.png" alt="アジャストワンロゴ" />
    <h2>アジャストワンFAQ</h2>
  </header>

  <input type="text" id="searchBox" placeholder="🔍 キーワードで検索" oninput="filterFaq()" />

  <!-- FAQ構造開始 -->
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
  <!-- FAQ構造終了 -->

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
