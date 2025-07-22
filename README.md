
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>アジャストワンFAQ</title>
  <style>
    body {
      font-family: "Segoe UI", "Helvetica Neue", sans-serif;
      background: linear-gradient(to right, #1f2a3c, #2e3c50);
      color: #f5f5f5;
      margin: 0;
      padding: 40px 20px;
    }

    h2 {
      text-align: center;
      font-size: 28px;
      margin-bottom: 30px;
      color: #ffffff;
      letter-spacing: 1px;
    }

    #searchBox {
      width: 100%;
      max-width: 400px;
      margin: 0 auto 30px;
      padding: 10px 14px;
      border: none;
      border-radius: 6px;
      font-size: 16px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    }

    .faq-toggle {
      background-color: #39495f;
      padding: 14px 16px;
      margin: 12px 0;
      cursor: pointer;
      font-weight: 600;
      border-radius: 6px;
      font-size: 16px;
      transition: background 0.3s;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    }

    .faq-toggle:hover {
      background-color: #465a77;
    }

    .faq-content {
      display: none;
      padding: 16px 20px;
      background-color: #2d394c;
      border-left: 3px solid #00acc1;
      border-radius: 0 0 6px 6px;
      margin-bottom: 10px;
    }

    .faq-content p {
      margin: 0;
    }

    .layer {
      margin-left: 15px;
    }
  </style>
</head>
<body>

  <h2>🔧 アジャストワンFAQ</h2>

  <input type="text" id="searchBox" placeholder="キーワードで検索..." oninput="filterFaq()" />

  <!-- 第1階層 -->
  <div class="faq-toggle" onclick="toggle(this)">オフィスラインについて 🔽</div>
  <div class="faq-content layer">

    <div class="faq-toggle" onclick="toggle(this)">セルフページについて 🔽</div>
    <div class="faq-content layer">

      <div class="faq-toggle" onclick="toggle(this)">セルフページで出来ることは？ 🔽</div>
      <div class="faq-content layer">
        <p><strong>Q:</strong> セルフページで設定できることは？<br>
        <strong>A:</strong> 無条件転送・スケジュール転送・着信拒否（有償）などが設定可能です。<br>
        詳しくは 0120-874-839 へお問い合わせください。</p>
      </div>

      <div class="faq-toggle" onclick="toggle(this)">自社で設定されたい場合 🔽</div>
      <div class="faq-content layer">
        <p><strong>Q:</strong> 自社で設定をされたい場合<br>
        <strong>A:</strong> 一度0120-874-839 へお問い合わせください。</p>
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
      const sections = document.querySelectorAll(".faq-content, .faq-toggle");
      sections.forEach(el => {
        if (el.textContent.toLowerCase().includes(keyword)) {
          el.style.display = "";
        } else if (el.classList.contains("faq-content")) {
          el.style.display = "none";
        }
      });
    }
  </script>

</body>
</html>
