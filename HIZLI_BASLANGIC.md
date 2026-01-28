# 🎯 HIZLI BAŞLANGIÇ REHBERİ

## ✅ Tamamlanan Adımlar

1. ✅ Firebase entegreli tek HTML dosyası oluşturuldu (`index.html`)
2. ✅ Git repository başlatıldı
3. ✅ İlk commit yapıldı
4. ✅ Detaylı kurulum rehberleri hazırlandı

## 🔥 ŞİMDİ YAPMANIZ GEREKENLER

### 1. Firebase Kurulumu (5 dakika)

📄 **Detaylı rehber**: `FIREBASE_SETUP.md` dosyasını okuyun

**Hızlı adımlar:**
1. https://console.firebase.google.com/ adresine gidin
2. Yeni proje oluşturun: "yks-net-takip"
3. Firestore Database ekleyin (Test mode)
4. Web uygulaması ekleyin
5. Config bilgilerini kopyalayın
6. `index.html` dosyasının 17-24. satırlarındaki Firebase config'i güncelleyin

```javascript
// index.html içinde bunu bulun ve değiştirin:
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",  // ← Buraya kendi bilgilerinizi yazın
    authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_PROJECT_ID.appspot.com",
    messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
    appId: "YOUR_APP_ID"
};
```

### 2. GitHub Repository Oluşturma (3 dakika)

📄 **Detaylı rehber**: `GITHUB_PAGES_SETUP.md` dosyasını okuyun

**Hızlı adımlar:**
1. https://github.com/new adresine gidin
2. Repository adı: `yks-net-takip`
3. Public seçin
4. "Create repository" tıklayın
5. Açılan sayfadaki komutları KULLANMAYIN (zaten yaptık!)

### 3. GitHub'a Push (2 dakika)

Terminal/PowerShell'de şu komutları çalıştırın:

```bash
# KULLANICI_ADINIZ yerine kendi GitHub kullanıcı adınızı yazın
git remote add origin https://github.com/KULLANICI_ADINIZ/yks-net-takip.git

# Push yap
git push -u origin main
```

**Not**: İlk push'ta GitHub kullanıcı adı ve Personal Access Token isteyecek.

#### Personal Access Token Oluşturma:
1. GitHub > Settings > Developer settings > Personal access tokens > Tokens (classic)
2. "Generate new token (classic)"
3. Note: "YKS App"
4. Expiration: 90 days
5. Scopes: ✅ repo
6. "Generate token" ve kopyalayın

### 4. GitHub Pages Aktifleştirme (1 dakika)

1. GitHub repository > Settings > Pages
2. Source: `main` branch, `/ (root)` folder
3. Save

**5-10 dakika sonra siteniz yayında olacak!**

URL: `https://KULLANICI_ADINIZ.github.io/yks-net-takip/`

## 🎉 TAMAMLANDI!

Artık uygulamanız:
- ✅ Tek HTML dosyası
- ✅ Firebase ile bulut senkronizasyonu
- ✅ GitHub Pages'de canlı
- ✅ Her yerden erişilebilir
- ✅ Mobil uyumlu

## 📱 Kullanım

1. Sitenizi açın
2. Sınav bilgilerini girin
3. Veriler otomatik olarak Firebase'e kaydedilir
4. Başka cihazdan açsanız bile verileriniz orada!

## 🔄 Güncelleme Yapmak

Kod değişikliği yaptığınızda:

```bash
git add .
git commit -m "Açıklama"
git push
```

GitHub Pages otomatik güncellenir!

## 📚 Dosya Yapısı

```
YKS uygulaması/
├── index.html              ← Ana uygulama (TEK DOSYA!)
├── README.md               ← Proje açıklaması
├── FIREBASE_SETUP.md       ← Firebase kurulum rehberi
├── GITHUB_PAGES_SETUP.md   ← GitHub Pages rehberi
├── HIZLI_BASLANGIC.md      ← Bu dosya
└── .gitignore              ← Git ignore kuralları
```

## 🆘 Yardım

- Firebase sorunları → `FIREBASE_SETUP.md` dosyasına bakın
- GitHub Pages sorunları → `GITHUB_PAGES_SETUP.md` dosyasına bakın
- Genel sorular → `README.md` dosyasına bakın

## 🎯 Sıradaki Adımlar

1. ☐ Firebase config'i güncelleyin
2. ☐ GitHub repository oluşturun
3. ☐ Push yapın
4. ☐ GitHub Pages'i aktifleştirin
5. ☐ Uygulamanızı test edin
6. ☐ Arkadaşlarınızla paylaşın!

---

**Başarılar! Sorularınız için issue açabilirsiniz.** 🚀
