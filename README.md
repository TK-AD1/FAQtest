<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>多階層FAQ</title>
  <style>
    body {
      font-family: sans-serif;
      padding: 20px;
      line-height: 1.6;
      font-size: 16px;
    }
    .layer {
      margin-left: 20px;
      margin-top: 10px;
    }
    .faq-toggle {
      background-color: #e0e0e0;
      padding: 12px;
      margin-top: 5px;
      cursor: pointer;
      font-weight: bold;
      border-radius: 4px;
      font-size: 16px;
    }
    .faq-content {
      display: none;
      padding: 12px;
      background-color: #f9f9f9;
      border-left: 3px solid #0078D7;
      border-radius: 4px;
      font-size: 15px;
    }
  </style>
</head>
<body>

  <h2>多階層 FAQ</h2>

  <!-- 第1階層 -->
  <div class="faq-toggle" onclick="toggle(this)">🔽 オフィスラインについて</div>
  <div class="faq-content layer">
    
    <!-- 第2階層：セルフページ -->
    <div class="faq-toggle" onclick="toggle(this)">🔽 セルフページについて</div>
    <div class="faq-content layer">

      <!-- 第3階層 -->
      <div class="faq-toggle" onclick="toggle(this)">🔽 セルフページで出来ることは？</div>
      <div class="faq-content layer">
        <p><strong>Q:</strong> セルフページで設定出来ることは？<br>
           <strong>A:</strong> 無条件転送やスケジュール転送が設定可能です。<br>
           着信拒否（有償）も設定可能です。<br>
           詳細は 0120-874-839 へお問合せください。</p>
      </div>

      <div class="faq-toggle" onclick="toggle(this)">🔽 自社で設定したい場合</div>
      <div class="faq-content layer">
        <p><strong>Q:</strong> 自社で設定することは可能か？<br>
           <strong>A:</strong>  一度オフィスラインサポートセンター 0120-874-839 へお問合せください。</p>
      </div>

    </div>

    <!-- 第2階層：カスコン -->
    <div class="faq-toggle" onclick="toggle(this)">🔽 カスコンについて</div>
    <div class="faq-content layer">
      <div class="faq-toggle" onclick="toggle(this)">🔽 利用可能な機能</div>
      <div class="faq-content layer">
        <p><strong>Q:</strong> 設定できる機能は？<br>
           <strong>A:</strong> ファーストスケジュール機能、時間帯別転送、着信グループ設定などが可能です。</p>
      </div>
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
