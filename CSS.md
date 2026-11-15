* {
  box-sizing: border-box;
}

body {
  margin: 0;
  padding: 24px;
  font-family: Georgia, "Times New Roman", serif;
  color: #263238;
  background: #f1f0ec;
}

.magazine-layout {
  max-width: 1100px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: minmax(0, 2fr) minmax(240px, 1fr);
  grid-template-rows: auto auto 1fr auto;
  grid-template-areas:
    "header header"
    "nav nav"
    "article sidebar"
    "footer footer";
  gap: 20px;
}

.site-header {
  grid-area: header;
  padding: 26px 30px;
  background: #263f45;
  color: white;
}

.logo {
  color: white;
  font-size: 2rem;
  font-weight: bold;
  text-decoration: none;
}

.site-header p {
  margin: 6px 0 0;
  color: #d0dddd;
}

.site-nav {
  grid-area: nav;
  display: flex;
  flex-wrap: wrap;
  gap: 24px;
  padding: 14px 20px;
  border-bottom: 2px solid #c8d0cd;
  background: white;
}

.site-nav a {
  color: #354b50;
  font-family: Arial, sans-serif;
  font-weight: bold;
  text-decoration: none;
}

.site-nav a:hover {
  color: #aa583d;
}

.main-article {
  grid-area: article;
  min-width: 0;
  padding: 28px;
  background: white;
  line-height: 1.75;
}

.category {
  margin: 0 0 8px;
  color: #aa583d;
  font-family: Arial, sans-serif;
  font-size: 0.75rem;
  font-weight: bold;
  letter-spacing: 0.1em;
}

.main-article h1 {
  margin: 0 0 12px;
  font-size: clamp(2rem, 4vw, 3rem);
  line-height: 1.1;
}

.article-intro {
  color: #526266;
  font-size: 1.15rem;
}

.article-image {
  height: 280px;
  margin: 22px 0;
  border-radius: 8px;
  background:
    linear-gradient(#183b2c22, #183b2c22),
    url("https://images.unsplash.com/photo-1416879595882-3373a0480b5b?auto=format&fit=crop&w=1200&q=80")
    center / cover;
}

.sidebar {
  grid-area: sidebar;
  align-self: start;
  padding: 24px;
  border-top: 5px solid #aa583d;
  background: #fff;
}

.sidebar h2 {
  margin: 0 0 18px;
  font-size: 1.4rem;
}

.sidebar-story {
  padding: 16px 0;
  border-top: 1px solid #e0e3df;
}

.sidebar-story h3 {
  margin: 0;
  font-size: 1.1rem;
  line-height: 1.4;
}

.site-footer {
  grid-area: footer;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  gap: 8px 20px;
  padding: 18px 24px;
  background: #263f45;
  color: white;
  font-family: Arial, sans-serif;
  font-size: 0.9rem;
}

.site-footer p {
  margin: 0;
}

@media (max-width: 700px) {
  body {
    padding: 12px;
  }

  .magazine-layout {
    grid-template-columns: 1fr;
    grid-template-rows: auto;
    grid-template-areas:
      "header"
      "nav"
      "article"
      "sidebar"
      "footer";
    gap: 12px;
  }

  .site-header,
  .main-article {
    padding: 22px;
  }

  .article-image {
    height: 220px;
  }
}