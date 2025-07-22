
<html lang="ja">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>FAQ - OfficeLine</title>
  <style>
    body {
      margin: 0;
      font-family: "Helvetica Neue", "Segoe UI", sans-serif;
      background: linear-gradient(to right, #eef1f5, #f6f8fc);
      color: #2c3e50;
      line-height: 1.7;
      padding: 40px;
    }

    h2 {
      text-align: center;
      font-size: 28px;
      color: #0053b3;
      margin-bottom: 40px;
      letter-spacing: 0.5px;
    }

    .faq-toggle {
      background: #ffffffcc;
      backdrop-filter: blur(5px);
      padding: 16px 20px;
      margin: 12px 0;
      font-weight: 600;
      border-radius: 10px;
      cursor: pointer;
      box-shadow: 0 4px 10px rgba(0,0,0,0.05);
      display: flex;
      justify-content: space-between;
      align-items: center;
      transition: all 0.2s ease;
    }

    .faq-toggle:hover {
      background-color: #e9ecf3;
      transform: scale(1.01);
    }

    .faq-content {
      overflow: hidden;
      max-height: 0;
      opacity: 0;
      padding: 0 20px;
      background-color: #fff;
      border-left: 4px solid #0078D7;
      border-radius: 0 0 10px 10px;
      box-shadow: inset 0 0 3px rgba(0,0,0,0.05);
      transition: all 0.4s ease;
    }

    .faq-content.active {
      max-height: 500px;
      opacity: 1;
      padding: 20px;
    }

    .layer {
      margin-left: 15px;
    }

    p {
      margin: 0 0 10px;
    }

    strong {
      color: #333;
    }
  </style>
</head>
<body>

  <h2>📘 オフィスライン社内FAQ</h2>

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

      <div class="faq-toggle" onclick="toggle(this)">自社で設定したい場合 🔽</div>
      <div class="faq-content layer">
        <p><strong>Q:</strong> 管理者が直接設定できますか？<br>
        <strong>A:</strong> 管理者アカウントから可能です。サポートセンターへ事前連絡してください。</p>
      </div>
    </div>

    <div class="faq-toggle" onclick="toggle(this)">カスコンについて 🔽</div>
    <div class="faq-content layer">
      <div class="faq-toggle" onclick="toggle(this)">利用可能な機能 🔽</div>
      <div class="faq-content layer">
        <p><strong>Q:</strong> 設定できる機能は？<br>
        <strong>A:</strong> ファーストスケジュール・時間帯別転送・着信グループ設定などが利用可能です。</p>
      </div>
    </div>

  </div>

<script>
function toggle(element) {
  const content = element.nextElementSibling;
  content.classList.toggle("active");
  element.textContent = element.textContent.includes("🔽")
    ? element.textContent.replace("🔽", "🔼")
    : element.textContent.replace("🔼", "🔽");
}
</script>

</body>
</html>
