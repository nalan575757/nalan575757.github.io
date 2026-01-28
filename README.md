# 🎓 YKS (TYT) Net Takip Sistemi

Modern, responsive ve Firebase entegreli YKS TYT sınav performans takip uygulaması.

## ✨ Özellikler

- 📝 **Sınav Kayıt Formu** - Tarih, ad ve 4 ders için doğru/yanlış girişi
- 🧮 **Otomatik Net Hesaplama** - Her ders için anlık net hesaplama (Doğru - Yanlış/4)
- 📊 **İstatistikler** - En yüksek ve ortalama net gösterimi
- 📈 **Grafik Görselleştirme** - Recharts ile net gelişim grafiği
- 🗂️ **Sınav Geçmişi** - Tüm sınavların detaylı tablosu
- ☁️ **Firebase Entegrasyonu** - Bulut tabanlı veri senkronizasyonu
- 💾 **Çift Yedekleme** - Firebase + localStorage
- 📱 **Responsive Tasarım** - Mobil ve masaüstü uyumlu
- 🇹🇷 **Türkçe Arayüz** - Tamamen Türkçe

## 🚀 Canlı Demo

**[YKS Net Takip - GitHub Pages](https://KULLANICI_ADINIZ.github.io/yks-net-takip/)**

## 🔧 Firebase Kurulumu

1. [Firebase Console](https://console.firebase.google.com/) adresine gidin
2. Yeni bir proje oluşturun
3. **Firestore Database** ekleyin (Test modunda başlatın)
4. **Web uygulaması** ekleyin ve yapılandırma bilgilerini alın
5. `index.html` dosyasındaki Firebase config kısmını kendi bilgilerinizle değiştirin:

```javascript
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",
    authDomain: "YOUR_PROJECT_ID.firebaseapp.com",
    projectId: "YOUR_PROJECT_ID",
    storageBucket: "YOUR_PROJECT_ID.appspot.com",
    messagingSenderId: "YOUR_MESSAGING_SENDER_ID",
    appId: "YOUR_APP_ID"
};
```

## 📦 GitHub Pages'de Yayınlama

### Adım 1: GitHub Repository Oluşturma

```bash
git init
git add .
git commit -m "İlk commit: YKS Net Takip Sistemi"
git branch -M main
git remote add origin https://github.com/KULLANICI_ADINIZ/yks-net-takip.git
git push -u origin main
```

### Adım 2: GitHub Pages Aktifleştirme

1. GitHub repository'nizde **Settings** > **Pages** bölümüne gidin
2. **Source** olarak `main` branch'i seçin
3. **Root** klasörünü seçin
4. **Save** butonuna tıklayın
5. Birkaç dakika içinde siteniz yayında olacak!

## 💻 Yerel Kullanım

Sunucu gerektirmez! Sadece `index.html` dosyasını tarayıcınızda açın:

```bash
# Dosyayı doğrudan açın
start index.html

# Veya basit bir HTTP sunucusu ile
python -m http.server 8000
# Sonra http://localhost:8000 adresine gidin
```

## 🛠️ Teknolojiler

- **React 18** - UI framework
- **Tailwind CSS** - Styling (CDN)
- **Recharts** - Chart visualization
- **Firebase Firestore** - Cloud database
- **localStorage** - Offline backup

## 📱 Kullanım

1. **Sınav Ekle**: Tarih, ad ve doğru/yanlış sayılarını girin
2. **Net Hesaplama**: Otomatik olarak her ders için net hesaplanır
3. **Kaydet**: Veriler Firebase'e ve localStorage'a kaydedilir
4. **Takip Et**: Grafik ve tabloda gelişiminizi görün
5. **Sil**: İstenmeyen sınavları silin

## 🔒 Güvenlik

- Veriler Firebase Firestore'da güvenle saklanır
- localStorage ile offline yedekleme
- HTTPS üzerinden güvenli iletişim

## 📄 Lisans

MIT License - Özgürce kullanabilir ve değiştirebilirsiniz.

## 🤝 Katkıda Bulunma

Pull request'ler memnuniyetle karşılanır!

## 📧 İletişim

Sorularınız için issue açabilirsiniz.

---

**Başarılar! YKS çalışmalarınızda kolaylıklar dilerim!** 🎯📚
