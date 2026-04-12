# DMX Pro Controller - iOS Uygulaması

## Kurulum

### Gereksinimler
- Node.js 18+
- Xcode 14+
- macOS

### Adımlar

1. **Bağımlılıkları yükleyin:**
```bash
cd dmx-ios-app
npm install
```

2. **iOS platformunu ekleyin (zaten ekli):**
```bash
npx cap add ios
```

3. **Web assets'leri iOS'a kopyalayın:**
```bash
npx cap sync ios
```

4. **iOS projesini Xcode'da açın:**
```bash
npx cap open ios
```

5. **Xcode'da build yapın:**
   - Product > Build (Cmd+B)
   - Veya Product > Run (Cmd+R) ile simulatorde/test cihazında çalıştırın

## Özellikler

- 512 DMX kanal kontrolü
- USB ve WiFi bağlantısı
- 20 submaster
- Kanal kaydetme/yükleme (JSON)
- Profesyonel keypad arayüzü

## Önemli Notlar

1. **WiFi Bağlantısı:** Uygulama, DMX kontrol cihazına WiFi üzerinden bağlanır. `192.168.10.221` varsayılan IP'dir.

2. **USB Bağlantısı:** Chrome/Edge tarayıcılarında WebSerial API kullanır. iOS'ta bu özellik sınırlıdır.

3. **Simülatör vs Gerçek Cihaz:** WiFi bağlantısı hem simülatörde hem gerçek cihazda çalışır.

## Proje Yapısı

```
dmx-ios-app/
├── www/              # Web uygulaması (HTML/CSS/JS)
├── ios/              # iOS native projesi
├── capacitor.config.json
└── package.json
```

## Güncelleme

Web kodunda değişiklik yapıldıktan sonra:
```bash
npx cap sync ios
npx cap open ios
```

## Capacitor Dokümantasyonu

Daha fazla bilgi için: https://capacitorjs.com/docs
