# Cumhuriyetin İzinde: Bayrak Avcısı 🇹🇷✈️

**29 Ekim Cumhuriyet Bayramı** temalı, 6. sınıf (Ortaokul) düzeyi başta olmak üzere tüm yaş gruplarına (Okul Öncesi, İlkokul, Ortaokul, Lise) uyarlanabilir 2D yatay ilerlemeli uçak ve bayrak toplama oyunu.

---

## 1. Bilgisayarda Nasıl Açılır ve Oynanır?

Oyun **tamamen çevrimdışı (internetsiz)** çalışacak şekilde tek bir `index.html` dosyası içinde geliştirilmiştir. Harici görsel, ses dosyası veya sunucu kurulumu gerektirmez.

1. Klasör içindeki **`index.html`** dosyasına çift tıklayın (Google Chrome, Microsoft Edge, Mozilla Firefox veya Safari ile doğrudan açılır).
2. Açılış ekranında varsayılan olarak **Ortaokul (6. Sınıf)** modu seçilidir. İsterseniz **Yaş Grubu / Zorluk Seçimi** menüsünden farklı bir kademe seçebilirsiniz.
3. **🚀 Oyuna Başla** butonuna tıklayarak 1. seviyeden uçuşa başlayabilirsiniz.

### Kontroller
- **Bilgisayar (Klavye):**
  - **Ok Tuşları** veya **W, A, S, D**: Uçağı yukarı, aşağı, sola ve sağa hareket ettirir.
  - **P** veya **Esc**: Oyunu duraklatır / devam ettirir.
- **Dokunmatik Ekran (Tablet / Akıllı Tahta / Mobil):**
  - Ekranın sol alt köşesindeki **büyük yön tuşlarını (▲ ▼ ◀ ▶)** kullanabilir veya uçağı ekran üzerinde **parmağınızla sürükleyerek** yönlendirebilirsiniz.

---

## 2. Seviyeler ve 6. Sınıf Eğitsel İçeriği

Her seviyede hedef **10 Türk bayrağı** toplamaktır (her bayrak **+10 puan** kazandırır). Oyuncu **3 can (❤️❤️❤️)** ile başlar; kayalara ve sıcak hava balonlarına çarpmaktan kaçınır.

1. **İstanbul'un Gökyüzü (Kolay):** Boğaz ve Galata Kulesi silüeti eşliğinde başlangıç uçuşu.
2. **Anadolu'nun Rüzgârı (Orta):** Kapadokya Peri Bacaları ve sıcak hava balonları arasında manevra.
3. **Cumhuriyet Yolunda (Zor):** Başkent Ankara ve Anıtkabir silüeti üzerinde Cumhuriyet rotası.
4. **Geleceğe Uçuş (İleri):** Yıldızlı Cumhuriyet gecesinde final uçuşu.

- Her seviye sonunda **6. Sınıf Sosyal Bilgiler / Cumhuriyet Tarihi Bilgi Notu** ve etkileşimli **6. Sınıf Mini Sorusu** yer alır.
- Dört seviyeyi tamamlayan oyuncu **“Cumhuriyetin Genç Kahramanı”** unvanını kazanır.

---

## 3. SCORM 1.2 Paketi ve EBA Uyumluluğu

Klasörde hem doğrudan açılabilen `index.html` hem de LMS / içerik yönetim sistemleri için hazırlanmış SCORM 1.2 dosyaları yer alır:

- **`index.html`**: Gömülü SCORM 1.2 API adaptörü içerir (`LMSInitialize`, `LMSSetValue`, `LMSCommit`, `LMSFinish`). SCORM API bulunmadığında (normal tarayıcıda açıldığında) hiçbir hata vermeden çalışır.
- **`imsmanifest.xml`**: SCORM 1.2 standart manifest dosyası.
- **`cumhuriyetin_izinde_bayrak_avcisi_scorm12.zip`**: `index.html` ve `imsmanifest.xml` dosyalarını kök dizinde barındıran hazır SCORM 1.2 ZIP paketi.
- **Tamamlanma Bildirimi:** Oyun yalnızca açıldığı için tamamlandı sayılmaz; seviye ilerlemelerinde puan (`cmi.core.score.raw`) ve konum (`cmi.core.lesson_location`) güncellenir, 4. seviye tamamlandığında `cmi.core.lesson_status = "completed"` bildirilir.

---

## 4. Test Kontrol Listesi Sonucu

Gerçek Google Chrome tarayıcı çalıştırmasıyla (Headless Chrome & CDP Otomasyon Testi) tüm maddeler doğrulanmıştır:

- [x] Açılış ekranı yükleniyor.
- [x] Oyuna Başla çalışıyor.
- [x] Nasıl Oynanır ekranı açılıyor ve geri dönüş çalışıyor.
- [x] Seviye seçimi çalışıyor.
- [x] Klavye kontrolleri uçağı hareket ettiriyor.
- [x] Dokunmatik kontroller çalışıyor.
- [x] Uçak oyun alanının dışına çıkmıyor.
- [x] Bayraklar toplanıyor ve puan doğru artıyor (+10 puan).
- [x] Engellerle çarpışma algılanıyor.
- [x] Her çarpışma yalnızca bir can eksiltiyor (kısa süreli koruma kalkanı devreye giriyor).
- [x] Can sıfırlanınca oyun bitiyor.
- [x] Duraklatma ve devam ettirme çalışıyor.
- [x] Yeniden başlatma tüm değerleri sıfırlıyor.
- [x] On bayrakla seviye tamamlanıyor.
- [x] Sonraki seviye açılıyor.
- [x] Dört seviye tamamlanınca final ekranı ve “Cumhuriyetin Genç Kahramanı” unvanı gösteriliyor.
- [x] Ses açma/kapatma çalışıyor (Web Audio API).
- [x] Farklı ekran boyutlarında arayüz bozulmuyor.
- [x] Tarayıcı konsolunda kritik hata bulunmuyor (`0` hata).
- [x] Oyun internet bağlantısı olmadan açılıyor.
