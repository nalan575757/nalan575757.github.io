# 🔥 Firebase Kurulum Rehberi

## Adım 1: Firebase Projesi Oluşturma

1. **Firebase Console'a gidin**: https://console.firebase.google.com/
2. **"Add project"** (Proje ekle) butonuna tıklayın
3. **Proje adı girin**: Örneğin "yks-net-takip"
4. **Google Analytics'i** istediğiniz gibi yapılandırın (isteğe bağlı)
5. **"Create project"** butonuna tıklayın

## Adım 2: Firestore Database Oluşturma

1. Sol menüden **"Build" > "Firestore Database"** seçin
2. **"Create database"** butonuna tıklayın
3. **Konum seçin**: Europe (eur3) önerilir
4. **Güvenlik kuralları**: "Start in test mode" seçin (geliştirme için)
5. **"Enable"** butonuna tıklayın

⚠️ **ÖNEMLİ**: Test modu 30 gün sonra sona erer. Production için güvenlik kurallarını güncelleyin!

### Production Güvenlik Kuralları (Önerilen):

```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /exams/{document=**} {
      allow read, write: if true; // Herkes okuyup yazabilir
      // Veya daha güvenli:
      // allow read, write: if request.auth != null; // Sadece giriş yapmış kullanıcılar
    }
  }
}
```

## Adım 3: Web Uygulaması Ekleme

1. Firebase Console'da proje genel bakış sayfasında **"Web"** ikonuna (</>)  tıklayın
2. **App nickname** girin: "YKS Net Takip Web"
3. **"Firebase Hosting"** seçeneğini işaretlemeyin (GitHub Pages kullanacağız)
4. **"Register app"** butonuna tıklayın

## Adım 4: Firebase Config Bilgilerini Kopyalama

Şu şekilde bir yapılandırma göreceksiniz:

```javascript
const firebaseConfig = {
  apiKey: "AIzaSyXXXXXXXXXXXXXXXXXXXXXXXXXXXXX",
  authDomain: "yks-net-takip.firebaseapp.com",
  projectId: "yks-net-takip",
  storageBucket: "yks-net-takip.appspot.com",
  messagingSenderId: "123456789012",
  appId: "1:123456789012:web:abcdef1234567890"
};
```

## Adım 5: Config'i index.html'e Ekleme

1. **index.html** dosyasını açın
2. Şu satırları bulun (yaklaşık 17-24. satırlar):

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

3. **Kendi Firebase config bilgilerinizle değiştirin**
4. **Dosyayı kaydedin**

## Adım 6: Test Etme

1. **index.html** dosyasını tarayıcıda açın
2. Bir sınav ekleyin
3. Sayfayı yenileyin - veriler hala orada olmalı
4. Firebase Console > Firestore Database'de verileri görebilirsiniz

## 🎉 Tebrikler!

Firebase entegrasyonu tamamlandı! Artık verileriniz bulutta güvenle saklanıyor.

## 🔐 Güvenlik İpuçları

### Test Modundan Production'a Geçiş:

1. Firebase Console > Firestore Database > Rules
2. Şu kuralları ekleyin:

```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /exams/{examId} {
      // Herkes okuyabilir, herkes yazabilir (basit)
      allow read, write: if true;
      
      // VEYA daha güvenli: Sadece belirli bir kullanıcı
      // allow read, write: if request.auth != null && request.auth.uid == "USER_ID";
    }
  }
}
```

3. **"Publish"** butonuna tıklayın

## 🆘 Sorun Giderme

### "Permission denied" hatası:
- Firestore kurallarını kontrol edin
- Test modunda olduğunuzdan emin olun

### Veriler görünmüyor:
- Tarayıcı konsolunu açın (F12)
- Hata mesajlarını kontrol edin
- Firebase config bilgilerinin doğru olduğundan emin olun

### CORS hatası:
- Firebase otomatik olarak CORS'u yönetir
- Sorun devam ederse tarayıcı önbelleğini temizleyin

## 📚 Ek Kaynaklar

- [Firebase Docs](https://firebase.google.com/docs)
- [Firestore Güvenlik Kuralları](https://firebase.google.com/docs/firestore/security/get-started)
- [Firebase Console](https://console.firebase.google.com/)
