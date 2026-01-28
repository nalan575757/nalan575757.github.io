# 🚀 GitHub Pages Yayınlama Rehberi

## Ön Gereksinimler

- ✅ GitHub hesabı
- ✅ Git kurulu olmalı
- ✅ Firebase kurulumu tamamlanmış olmalı

## Adım 1: Git Repository Oluşturma

### Terminal/PowerShell'de:

```bash
# Git'i başlat
git init

# Tüm dosyaları ekle
git add .

# İlk commit
git commit -m "İlk commit: YKS Net Takip Sistemi"

# Ana branch'i main olarak ayarla
git branch -M main
```

## Adım 2: GitHub'da Repository Oluşturma

1. **GitHub'a gidin**: https://github.com
2. **Sağ üstteki "+" işaretine** tıklayın
3. **"New repository"** seçin
4. **Repository adı**: `yks-net-takip` (veya istediğiniz ad)
5. **Public** seçin (GitHub Pages için gerekli)
6. **"Create repository without README"** - Zaten README'miz var
7. **"Create repository"** butonuna tıklayın

## Adım 3: Local Repository'yi GitHub'a Bağlama

GitHub'da oluşturduğunuz repository sayfasında gösterilen komutları kullanın:

```bash
# Remote ekle (KULLANICI_ADINIZ'ı kendi kullanıcı adınızla değiştirin)
git remote add origin https://github.com/KULLANICI_ADINIZ/yks-net-takip.git

# Push yap
git push -u origin main
```

### 🔐 GitHub Authentication:

İlk push'ta kimlik doğrulama isteyecek:
- **Username**: GitHub kullanıcı adınız
- **Password**: Personal Access Token (PAT) kullanın

#### Personal Access Token Oluşturma:
1. GitHub > Settings > Developer settings > Personal access tokens > Tokens (classic)
2. "Generate new token" > "Generate new token (classic)"
3. Note: "YKS App Deployment"
4. Expiration: 90 days (veya istediğiniz süre)
5. Scopes: `repo` seçeneğini işaretleyin
6. "Generate token" butonuna tıklayın
7. **Token'ı kopyalayın** (bir daha göremezsiniz!)

## Adım 4: GitHub Pages'i Aktifleştirme

1. **GitHub repository sayfanızda** "Settings" sekmesine gidin
2. Sol menüden **"Pages"** seçin
3. **Source** bölümünde:
   - Branch: `main` seçin
   - Folder: `/ (root)` seçin
4. **"Save"** butonuna tıklayın

## Adım 5: Yayın URL'ini Alma

Birkaç dakika sonra sayfanın üstünde şu mesajı göreceksiniz:

```
✅ Your site is live at https://KULLANICI_ADINIZ.github.io/yks-net-takip/
```

## 🎉 Tebrikler!

Uygulamanız artık canlı! URL'yi paylaşabilirsiniz.

## 📝 Güncelleme Yapmak

Kod değişikliği yaptığınızda:

```bash
# Değişiklikleri ekle
git add .

# Commit yap
git commit -m "Açıklama: Ne değiştirdiniz"

# GitHub'a gönder
git push
```

GitHub Pages otomatik olarak güncellenecek (1-2 dakika sürebilir).

## 🔧 Özel Domain Kullanma (İsteğe Bağlı)

Kendi domain'inizi kullanmak isterseniz:

1. **Domain sağlayıcınızda** (GoDaddy, Namecheap, vb.) DNS ayarlarına gidin
2. **CNAME kaydı** ekleyin:
   - Host: `www` veya `@`
   - Value: `KULLANICI_ADINIZ.github.io`
3. **GitHub Pages ayarlarında** "Custom domain" bölümüne domain'inizi girin
4. **"Enforce HTTPS"** seçeneğini aktifleştirin

## 🐛 Sorun Giderme

### Sayfa 404 hatası veriyor:
- GitHub Pages'in aktif olduğundan emin olun
- `index.html` dosyasının root dizinde olduğunu kontrol edin
- 5-10 dakika bekleyin (ilk deployment biraz zaman alabilir)

### Firebase çalışmıyor:
- `index.html` içindeki Firebase config'in doğru olduğundan emin olun
- Tarayıcı konsolunu kontrol edin (F12)
- Firebase kurallarının doğru ayarlandığından emin olun

### Git push hatası:
- Personal Access Token kullandığınızdan emin olun
- Token'ın `repo` yetkisine sahip olduğunu kontrol edin

### Değişiklikler görünmüyor:
- Tarayıcı önbelleğini temizleyin (Ctrl + Shift + R)
- GitHub Actions sekmesinde deployment durumunu kontrol edin

## 📱 Mobil Erişim

Uygulamanız responsive olduğu için mobil cihazlardan da mükemmel çalışır!

URL'yi telefonunuzda açın ve:
- **iOS**: Safari'de "Paylaş" > "Ana Ekrana Ekle"
- **Android**: Chrome'da "Menü" > "Ana ekrana ekle"

## 🔒 Güvenlik Notları

- ✅ HTTPS otomatik aktif (GitHub Pages sayesinde)
- ✅ Firebase config bilgileri public olabilir (normal)
- ✅ Firestore güvenlik kurallarını production için güncelleyin
- ⚠️ API anahtarları client-side'da görünür (bu normal ve güvenli)

## 📊 Analytics Ekleme (İsteğe Bağlı)

Google Analytics eklemek için `index.html` içine:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

## 🎯 Sonraki Adımlar

1. ✅ Firebase kurulumunu tamamlayın
2. ✅ GitHub'a push yapın
3. ✅ GitHub Pages'i aktifleştirin
4. ✅ URL'yi test edin
5. ✅ Arkadaşlarınızla paylaşın!

## 📚 Faydalı Linkler

- [GitHub Pages Docs](https://docs.github.com/en/pages)
- [Git Basics](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics)
- [Markdown Guide](https://www.markdownguide.org/)

---

**Başarılar!** 🚀
