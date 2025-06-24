# wUSDT Website - Ücretsiz Deploy Rehberi

## Seçenek 1: Netlify (Önerilen)

1. GitHub'da yeni repo oluşturun
2. Bu projeyi GitHub'a push edin:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/USERNAME/wusdt-website.git
   git push -u origin main
   ```
3. Netlify.com'a gidin
4. "New site from Git" tıklayın
5. GitHub repo'nuzu seçin
6. Build ayarları otomatik algılanacak (netlify.toml sayesinde)
7. Deploy butonuna tıklayın

**Domain**: Otomatik `random-name.netlify.app` domain alırsınız
**Custom Domain**: Ücretsiz custom domain bağlayabilirsiniz

## Seçenek 2: Vercel

1. GitHub'a push edin (yukarıdaki adımlar)
2. Vercel.com'a gidin
3. "New Project" tıklayın
4. GitHub repo'nuzu seçin
5. Framework otomatik algılanacak (vercel.json sayesinde)
6. Deploy butonuna tıklayın

**Domain**: Otomatik `project-name.vercel.app` domain alırsınız

## Seçenek 3: GitHub Pages

1. GitHub repo oluşturun
2. Settings > Pages
3. Source: "GitHub Actions" seçin
4. Bu workflow dosyasını `.github/workflows/deploy.yml` olarak ekleyin:

\`\`\`yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  build-and-deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
        with:
          node-version: '20'
      - run: npm install
      - run: npm run build
      - uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: \${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./dist
\`\`\`

**Domain**: `username.github.io/repo-name`

## Card.co'da Paylaşım

Deploy tamamlandıktan sonra:

1. Card.co'ya giriş yapın
2. "Create New Card" > "Website" seçin
3. Deploy URL'nizi ekleyin:
   - Netlify: `https://your-site.netlify.app`
   - Vercel: `https://your-project.vercel.app`
   - GitHub Pages: `https://username.github.io/repo-name`
4. Başlık: "Wrapped USDT (Wormhole) - wUSDT"
5. Açıklama: "Cross-chain USDT on Solana. 10B total supply, 2B locked on Jupiter"
6. Logo ekleyin ve publish edin

## Projeniz Hazır!

Bu proje tamamen static olduğu için tüm ücretsiz platformlarda sorunsuz çalışacak.