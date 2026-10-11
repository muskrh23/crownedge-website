<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CrownEdge | Trading Platform</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #071426;
      color: #ffffff;
    }

    header {
      background: #020914;
      padding: 22px 18px;
      border-bottom: 1px solid #c9a64c;
    }

    .logo {
      color: #e9c568;
      font-size: 25px;
      font-weight: bold;
      letter-spacing: 2px;
    }

    .tagline {
      color: #bdc8d8;
      font-size: 11px;
      margin-top: 6px;
    }

    nav {
      margin-top: 20px;
      display: flex;
      gap: 18px;
      flex-wrap: wrap;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-size: 14px;
    }

    .hero {
      text-align: center;
      padding: 75px 20px;
    }

    .hero h1 {
      font-size: 38px;
      line-height: 1.15;
      margin-bottom: 18px;
    }

    .hero p {
      color: #bdc8d8;
      line-height: 1.7;
      max-width: 500px;
      margin: 0 auto 28px;
    }

    .button {
      display: inline-block;
      background: #e9c568;
      color: #071426;
      text-decoration: none;
      font-weight: bold;
      padding: 14px 24px;
      border-radius: 5px;
    }

    section {
      padding: 35px 22px;
      text-align: center;
    }

    section h2 {
      color: #e9c568;
    }

    section p {
      color: #bdc8d8;
      line-height: 1.7;
    }

    footer {
      text-align: center;
      padding: 25px 15px;
      background: #020914;
      color: #bdc8d8;
      font-size: 12px;
    }
  </style>
</head>
<body>

<script type="module">
  import { createClient } from 'https://esm.sh/@supabase/supabase-js@2';

  const SUPABASE_URL = 'https://zaqfcgqxpbsdevocfiom.supabase.co';
  const SUPABASE_PUBLISHABLE_KEY = 'sb_publishable_K16tkWqfwGVCUCY3nMZ2VQ_m07Viwunp';

  window.supabaseClient = createClient(
    SUPABASE_URL,
    SUPABASE_PUBLISHABLE_KEY
  );
</script>

  <header>
    <div class="logo">CROWNEDGE</div>
    <div class="tagline">
      INSTITUTIONAL GRADE TRADING PLATFORM
    </div>

    <nav>
      <a href="#home">Home</a>
      <a href="#about">About</a>
      <a href="#services">Services</a>
      <a href="#contact">Contact</a>
    </nav>
  </header>

  <main>
    <div class="hero" id="home">
      <h1>Trade With Confidence</h1>

      <p>
        Discover market insights, explore trading
        resources, and learn about our platform.
      </p>

      <a class="button" href="#services">
        Explore Our Services
      </a>
    </div>

    <section id="about">
      <h2>About CrownEdge</h2>
      <p>
        Learn about our company, our approach to
        financial markets, our fees, and the risks
        involved in trading.
      </p>
    </section>
<script type="module">
import { createClient } from 'https://esm.sh/@supabase/supabase-js@2';
const supabase = window.supabaseClient;
const emailInput = document.getElementById('email');
const passwordInput = document.getElementById('password');
const message = document.getElementById('accountMessage');
document.getElementById('signupBtn').addEventListener('click', async () => {
  const email = emailInput.value.trim();
  const password = passwordInput.value;
  if (!email || password.length < 6) {
    message.textContent = 'Enter a valid email and a password of at least 6 characters.';
    return;
  }
  message.textContent = 'Creating account...';
  const { error } = await supabase.auth.signUp({
    email,
    password
  });
  message.textContent = error
    ? error.message
    : 'Signup submitted. Check your email to confirm your account.';
});
document.getElementById('loginBtn').addEventListener('click', async () => {
  const email = emailInput.value.trim();
  const password = passwordInput.value;
  if (!email || !password) {
    message.textContent = 'Enter your email and password.';
    return;
  }
  message.textContent = 'Logging in...';
  const { data, error } = await supabase.auth.signInWithPassword({
    email,
    password
  });
  message.textContent = error
    ? error.message
    : 'You are logged in successfully.';
});
</script>
    <section id="services">
      <h2>Our Services</h2>
      <p>
        Explore platform information, market
        education, and customer support.
      </p>
    </section>

    <section id="contact">
      <h2>Contact Us</h2>
      <p>
        Have a question? Contact our support team
        for information about our services.
      </p>
    </section>
  <section id="account" style="max-width:420px;margin:30px auto;padding:24px;background:#102033;color:white;border:1px solid #bdc8d8;border-radius:12px;">
  <h2 style="color:#d4af37;text-align:center;">CrownEdge Account</h2>
  <form id="accountForm">
    <label for="email">Email address</label>
    <input id="email" type="email" required placeholder="Enter your email" style="box-sizing:border-box;width:100%;padding:12px;margin:8px 0 16px;">
    <label for="password">Password</label>
    <input id="password" type="password" required minlength="6" placeholder="At least 6 characters" style="box-sizing:border-box;width:100%;padding:12px;margin:8px 0 16px;">
    <button type="button" id="signupBtn" style="padding:12px;background:#d4af37;color:#111;border:0;border-radius:6px;">Sign Up</button>
    <button type="button" id="loginBtn" style="padding:12px;background:#fff;color:#111;border:0;border-radius:6px;">Log In</button>
    <p id="accountMessage" role="status"></p>
  </form>
</section>
  </main>

  <footer>
    © 2026 CrownEdge. All rights reserved.
    <p>Trading involves risk, including possible loss of capital.</p>
  </footer>
<!-- Smartsupp Live Chat script -->
<script type="text/javascript">
var _smartsupp = _smartsupp || {};
_smartsupp.key = '42c33928b557d4639b43f0117fc940a3a7c3043b';
window.smartsupp||(function(d) {
  var s,c,o=smartsupp=function(){ o._.push(arguments)};o._=[];
  s=d.getElementsByTagName('script')[0];c=d.createElement('script');
  c.type='text/javascript';c.charset='utf-8';c.async=true;
  c.src='https://www.smartsuppchat.com/loader.js?';s.parentNode.insertBefore(c,s);
})(document);
</script>
<noscript>Powered by <a href="https://www.smartsupp.com" target="_blank">Smartsupp</a></noscript>

</body>
</html>
