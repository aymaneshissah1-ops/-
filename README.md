# -<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <title>توصيل القنيطرة</title>
  <style>
    /* === General Styles === */
    body {
      font-family: 'Arial', sans-serif;
      background: linear-gradient(to right, #2a9d8f, #e9c46a);
      color: #333;
      text-align: center;
      padding: 50px;
      margin: 0;
    }

    h1 {
      color: #264653;
      font-size: 36px;
      margin-bottom: 10px;
    }

    p {
      font-size: 18px;
      margin-bottom: 20px;
    }

    /* === Form Styles === */
    form {
      background: #fff;
      padding: 30px;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.2);
      display: inline-block;
      min-width: 300px;
    }

    input {
      padding: 12px;
      margin: 10px 0;
      width: 80%;
      border: 1px solid #ccc;
      border-radius: 8px;
      font-size: 16px;
    }

    button {
      padding: 12px 20px;
      font-size: 16px;
      background: #e76f51;
      color: #fff;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    button:hover {
      background: #f4a261;
      transform: scale(1.05);
    }

    /* === Message Styles === */
    #message {
      margin-top: 20px;
      font-weight: bold;
      color: #264653;
    }

    /* === Contact === */
    .contact {
      margin-top: 30px;
      font-size: 20px;
      font-weight: bold;
      color: #e9c46a;
    }
  </style>
</head>
<body>
  <h1>توصيل القنيطرة من صيدلية لباب الدار</h1>
  <p>تواصل معنا مباشرة واطلب الدواء لي بغيتي</p>

  <form id="orderForm">
    <input type="text" placeholder="اسمك" required><br>
    <input type="text" placeholder="عنوانك" required><br>
    <button type="submit">أرسل الطلب</button>
  </form>

  <p id="message"></p>

  <p class="contact">📞 اتصل بنا: 0707662411</p>

  <script>
    const form = document.getElementById('orderForm');
    const message = document.getElementById('message');

    form.addEventListener('submit', (e) => {
      e.preventDefault();

      // Animate message
      message.textContent = 'شكراً! تم إرسال طلبك، سنتواصل معك قريباً.';
      message.style.opacity = 0;
      message.style.transition = "opacity 0.5s";
      setTimeout(() => { message.style.opacity = 1; }, 50);

      // Reset form
      form.reset();
    });
  </script>
</body>
</html>
