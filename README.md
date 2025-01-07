<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Facebook Login Page (Educational)</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f0f2f5;
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
    }
    .login-container {
      background: #fff;
      width: 400px;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      text-align: center;
    }
    .login-container h1 {
      color: #1877f2;
      font-size: 24px;
      margin-bottom: 10px;
    }
    .login-container p {
      font-size: 14px;
      color: #606770;
      margin-bottom: 20px;
    }
    .login-container input {
      width: 100%;
      padding: 10px;
      margin-bottom: 15px;
      border: 1px solid #ddd;
      border-radius: 5px;
      font-size: 16px;
    }
    .login-container button {
      background-color: #1877f2;
      color: #fff;
      font-size: 16px;
      border: none;
      padding: 10px;
      width: 100%;
      border-radius: 5px;
      cursor: pointer;
    }
    .login-container button:hover {
      background-color: #165cba;
    }
  </style>
</head>
<body>
  <div class="login-container">
    <h1>Facebook</h1>
    <p>Log in to see your friends and updates.</p>
    <form onsubmit="handleLogin(event)">
      <input type="text" id="email" placeholder="Email or Phone Number" required />
      <input type="password" id="password" placeholder="Password" required />
      <button type="submit">Log In</button>
    </form>
  </div>

  <script>
    function handleLogin(event) {
      event.preventDefault();
      const email = document.getElementById('email').value;
      const password = document.getElementById('password').value;

      // حفظ البيانات في Local Storage
      localStorage.setItem('savedEmail', email);
      localStorage.setItem('savedPassword', password);

      // تأكيد الحفظ
      alert('Login data has been saved locally.');

      // مسح الحقول بعد الحفظ
      document.getElementById('email').value = '';
      document.getElementById('password').value = '';
    }

    // عرض البيانات المحفوظة في وحدة التحكم (Console)
    console.log('Saved Email:', localStorage.getItem('savedEmail'));
    console.log('Saved Password:', localStorage.getItem('savedPassword'));
  </script>
</body>
</html>
