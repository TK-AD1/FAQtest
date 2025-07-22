<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>多階層FAQ</title>
  <style>
    body {
      font-family: sans-serif;
      padding: 20px;
    }
    .layer {
      margin-left: 20px;
      margin-top: 10px;
    }
    .faq-toggle {
      background-color: #e0e0e0;
      padding: 8px;
      margin-top: 5px;
      cursor: pointer;
      font-weight: bold;
      border-radius: 4px;
    }
    .faq-content {
      display: none;
      padding: 10px;
      background-color: #f9f9f9;
      border-left: 3px solid #0078D7;
      border-radius: 4px;
    }
  </style>
</head>
<body>

  <h2>多階層 FAQ</h2>

  <!-- 第1階層 -->
  <div class="faq-toggle" onclick="toggle(this)">🔽 ログインについて</div>
  <div class="faq-content layer">
    
    <!-- 第2階層 -->
    <div class="faq-toggle" onclick="toggle(this)">🔽 ID／パスワード関連</div>
    <div class="faq-content layer">
      
      <!-- 第3階層 -->
      <div class="faq-toggle" onclick="toggle(this)">🔽 パスワードを忘れた場合</div>
      <div class="faq-content layer">
        
        <!-- 第4階層 -->
        <p><strong>Q:</strong> 再設定方法は？<br>
           <strong>A:</strong> ログイン画面の「パスワードをお忘れですか？」をクリックして、登録メールアドレスを入力してください。</p>
      </div>

    </div>

    <!-- 他の第2階層 -->
    <div class="faq-toggle" onclick="toggle(this)">🔽 2段階認証の設定</div>
    <div class="faq-content layer">
      <p><strong>Q:</strong> 認証アプリは何を使えばよい？<br>
         <strong>A:</strong> Google AuthenticatorまたはMicrosoft Authenticatorが利用可能です。</p>
    </div>

  </div>

<script>
function toggle(element) {
  const next = element.nextElementSibling;
  const isVisible = next.style.display === "block";
  next.style.display = isVisible ? "none" : "block";
  element.textContent = isVisible
    ? element.textContent.replace("🔼", "🔽")
    : element.textContent.replace("🔽", "🔼");
}
</script>

</body>
</html>
