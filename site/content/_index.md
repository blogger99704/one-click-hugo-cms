{{ define "main" }}
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>{{ .Site.Title }} - Modern Static CMS</title>
  <meta name="description" content="{{ .Site.Params.description }}">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Inter', sans-serif;
    }
    body {
      background: #f5f6f8;
      color: #333;
      line-height: 1.6;
    }
    header {
      background: #1e1e2f;
      color: #fff;
      padding: 1.5rem 3rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    header h1 {
      font-size: 1.6rem;
      font-weight: 700;
      letter-spacing: 1px;
    }
    nav a {
      color: #fff;
      text-decoration: none;
      margin-left: 1.5rem;
      font-weight: 600;
      transition: 0.3s;
    }
    nav a:hover {
      color: #00bcd4;
    }
    .hero {
      text-align: center;
      padding: 6rem 2rem;
      background: linear-gradient(135deg, #1e1e2f, #2e2e4f);
      color: #fff;
    }
    .hero h2 {
      font-size: 2.8rem;
      margin-bottom: 1rem;
    }
    .hero p {
      font-size: 1.1rem;
      max-width: 700px;
      margin: 0 auto 2.5rem;
    }
    .hero a {
      background: #00bcd4;
      color: #fff;
      padding: 0.9rem 1.8rem;
      border-radius: 8px;
      font-weight: 600;
      text-decoration: none;
      transition: 0.3s;
    }
    .hero a:hover {
      background: #0097a7;
    }
    .features {
      padding: 4rem 2rem;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 2rem;
      max-width: 1100px;
      margin: 0 auto;
    }
    .feature {
      background: #fff;
      padding: 2rem;
      border-radius: 12px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.08);
      text-align: center;
      transition: transform 0.3s;
    }
    .feature:hover {
      transform: translateY(-5px);
    }
    .feature h3 {
      color: #1e1e2f;
      margin-bottom: 1rem;
    }
    .feature p {
      color: #555;
    }
    footer {
      background: #1e1e2f;
      color: #aaa;
      text-align: center;
      padding: 1.5rem;
      font-size: 0.9rem;
      margin-top: 3rem;
    }
  </style>
</head>
<body>
  <header>
    <h1>{{ .Site.Title }}</h1>
    <nav>
      <a href="/">Home</a>
      <a href="/blog/">Blog</a>
      <a href="/docs/">Docs</a>
      <a href="/contact/">Contact</a>
    </nav>
  </header>

  <section class="hero">
    <h2>Build Lightning-Fast Websites with Hugo</h2>
    <p>{{ with .Site.Params.tagline }}{{ . }}{{ else }}Hugo CMS makes content management simple, fast, and flexible for developers and creators.{{ end }}</p>
    <a href="/docs/">Get Started</a>
  </section>

  <section class="features">
    <div class="feature">
      <h3>⚡ Blazing Fast</h3>
      <p>Generate static sites in milliseconds. Perfect for SEO, speed, and scalability.</p>
    </div>
    <div class="feature">
      <h3>🧩 Markdown Based</h3>
      <p>Write content in Markdown and let Hugo handle the structure automatically.</p>
    </div>
    <div class="feature">
      <h3>🛠️ Easy to Customize</h3>
      <p>Flexible themes and layouts for any type of website — from blogs to businesses.</p>
    </div>
  </section>

  <footer>
    <p>© {{ now.Format "2006" }} {{ .Site.Title }}. Built with ❤️ using Hugo.</p>
  </footer>
</body>
</html>
{{ end }}
