# FAQtest
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>FAQ一覧</title>
  <style>
    body {
      font-family: sans-serif;
      line-height: 1.6;
      padding: 20px;
    }
    .faq-category {
      margin-bottom: 20px;
    }
    .faq-header {
      background-color: #f0f0f0;
      cursor: pointer;
      padding: 10px;
      font-weight: bold;
      border: 1px solid #ccc;
      border-radius: 6px;
    }
    .faq-content {
      display: none;
      padding: 10px;
      border-left: 3px solid #0078D7;
      margin-top: 5px;
      background-color: #fafafa;
      border-radius: 4px;
    }
  </style>
</head>
<body>

  <h2>よくあるご質問（FAQ）</h2>

  <div class="faq-category">
    <div class="faq-header" onclick="toggleFaq(this)">🔽 ログインについて</div>
    <div class="faq-content">
      <p><strong>Q:</strong> パスワードを忘れた場合は？<br>
         <strong>A:</strong> 「パスワードをお忘れですか？」から再設定できます。</p>
    </div>
  </div>

  <div class="faq-category">
    <div class="faq-header" onclick="toggleFaq(this)">🔽 支払い方法について</div>
    <div class="faq-content">
      <p><strong>Q:</strong> 支払方法の変更は？<br>
         <strong>A:</strong> マイページから変更できます。次回請求に反映されます。</p>
    </div>
  </div>

  <div class="faq-category">
    <div class="faq-header" onclick="toggleFaq(this)">🔽 アカウント設定について</div>
    <div class="faq-content">
      <p><strong>Q:</strong> 登録メールアドレスは変更できる？<br>
         <strong>A:</strong> アカウント設定で変更可能です。本人確認が必要です。</p>
    </div>
  </div>

  <script>
    function toggleFaq(header) {
      const content = header.nextElementSibling;
      const isVisible = content.style.display === "block";
      content.style.display = isVisible ? "none" : "block";
      header.textContent = isVisible
        ? header.textContent.replace("🔼", "🔽")
        : header.textContent.replace("🔽", "🔼");
    }
  </script>

</body>
</html>
