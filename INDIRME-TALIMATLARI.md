# wUSDT Website - İndirme ve Kurulum Talimatları

## 📁 Dosyaları İndirme

### Yöntem 1: Tek tek indirme
1. Replit Files panelinde `wusdt-export` klasörünü açın
2. Her dosyaya sağ tıklayıp "Download" seçin

### Yöntem 2: GitHub'a yükleme (Önerilen)
```bash
# Terminal'de çalıştırın:
git init
git add .
git commit -m "wUSDT website"
git branch -M main
git remote add origin https://github.com/KULLANICI_ADINIZ/wusdt-website.git
git push -u origin main
```

## 💻 Bilgisayarınızda Çalıştırma

1. Dosyaları bilgisayarınıza indirin/klonlayın
2. Terminal açın ve proje klasörüne gidin
3. Bağımlılıkları yükleyin:
   ```bash
   npm install
   ```
4. Development server başlatın:
   ```bash
   npm run dev
   ```
5. Tarayıcıda `http://localhost:5173` adresini açın

## 🚀 Ücretsiz Deploy (Netlify)

1. Dosyaları GitHub'a yükleyin
2. [Netlify.com](https://netlify.com)'a gidin
3. "New site from Git" tıklayın
4. GitHub repo'nuzu seçin
5. Otomatik deploy başlayacak (netlify.toml dosyası sayesinde)

**Sonuç:** `https://site-adiniz.netlify.app` adresinde siteniz yayında olacak

## 📱 Card.co'da Paylaşım

Deploy tamamlandıktan sonra:
1. Card.co'ya giriş yapın
2. "Create New Card" → "Website" seçin
3. Deploy URL'nizi ekleyin
4. Başlık: "Wrapped USDT (Wormhole) - wUSDT"
5. Açıklama: "Cross-chain USDT on Solana. 10B total supply, 2B locked on Jupiter"
6. Logo ekleyin ve publish edin

## 📋 Proje İçeriği

- ✅ Ana sayfa (token bilgileri, sosyal medya)
- ✅ Whitepaper sayfası (tokenomics, roadmap)
- ✅ Responsive tasarım
- ✅ Tether yeşil tema
- ✅ Deploy konfigürasyonu

## 🔗 Önemli Linkler

- **Contract:** 57GajvDHazpCCCCpKgiHppJJf5cjwHWancCZZLPoeFMj
- **Owner:** HJdkDSZpCPxG38t4DdPN5FNxByCfXRhGvvgd3cvNa7Ud
- **Twitter:** https://x.com/wrappedwusdt
- **Telegram:** https://t.me/wrappedusdt
- **Email:** ericwillines@gmail.com

## ❓ Sorun mu yaşıyorsunuz?

- Node.js 18+ gereklidir
- npm install sorunları yaşarsanız: `npm cache clean --force`
- Port 5173 kullanılıyorsa başka port otomatik seçilecek