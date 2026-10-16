# CUMHURİYETİN İZİNDE: BAYRAK AVCISI
## Antigravity için oyun geliştirme görev dosyası

> **Amaç:** Bu dosyadaki gereksinimleri izleyerek gerçek, oynanabilir bir 29 Ekim Cumhuriyet Bayramı uçak oyunu geliştir. Yalnızca tasarım görseli veya prototip ekranı üretme.

## 1. Antigravity için çalışma talimatı

1. Önce çalışma klasöründeki mevcut dosyaları incele. Mevcut bir proje varsa dosyaları gelişigüzel silme veya üzerine yazma.
2. Oyunu çalışır hâle getir; ardından tarayıcıda açıp test et.
3. Hataları tespit edip düzeltmeden işi tamamlanmış sayma.
4. Bir özellik çalışmıyorsa çalışıyormuş gibi gösterme. Sorunu gider veya sınırlamayı açıkça belirt.
5. Kodda `TODO`, boş işlev, sahte buton veya yalnızca görsel olarak var olan kontrol bırakma.
6. Harici görsel ve ağ bağlantısı zorunlu olmasın. Oyun çevrimdışı çalışabilsin.

## 2. Proje özeti

- **Oyun adı:** Cumhuriyetin İzinde: Bayrak Avcısı
- **Tür:** 2D, yatay ilerlemeli uçak toplama ve engellerden kaçma oyunu
- **Tema:** 29 Ekim Cumhuriyet Bayramı
- **Hedef kitle:** Okul öncesi, ilkokul, ortaokul ve lise
- **Dil:** Türkçe
- **Platform:** Windows bilgisayar, tablet, akıllı tahta ve mobil tarayıcı
- **Önerilen teknoloji:** HTML5, CSS3 ve saf JavaScript; oyun mantığı için Canvas kullanılabilir.
- **Teslim hedefi:** Öncelikle tek başına açılabilen `index.html`; gerekirse düzenli kaynak dosyaları ve sonradan SCORM 1.2 paketlemesine uygun yapı.

## 3. Oyun fikri

Oyuncu, Türk bayrağı motifli kırmızı-beyaz bir uçakla gökyüzünde ilerler. Uçuş rotasında beliren Türk bayraklarını toplar, kayalardan ve sıcak hava balonlarından kaçınır. Her bayrak puan kazandırır. Engellere çarpınca can kaybeder. Hedefe ulaşınca seviye tamamlanır.

Oyuncu dört seviyeyi tamamladığında **“Cumhuriyetin Genç Kahramanı”** unvanını kazanır.

## 4. Görsel tasarım

- Canlı, kaliteli, çocuklara uygun çizgi film estetiği kullan.
- Gökyüzü, bulutlar, dağlar ve Türkiye'yi çağrıştıran manzaralar oluştur.
- Uçak kırmızı-beyaz renkte ve Türk bayrağı motifli olsun.
- Toplanabilir nesneler açıkça tanınabilen Türk bayrakları olsun.
- Engeller kayalar ve sıcak hava balonları gibi kolay ayırt edilebilen nesneler olsun.
- Arayüzde kırmızı, beyaz ve mavi tonlarından yararlan.
- Görsel dosyalar bulunamazsa Canvas/CSS ile özgün çizimler üret; oyunu çalıştırmak için internetten dosya indirmeye bağımlı olma.
- Atatürk ve Cumhuriyet temsillerini saygılı ve tarihsel olarak doğru kullan. Tarihî kişileri yanlış bilgiyle ilişkilendirme.
- Metinler Türkçe karakterleri doğru göstermeli: ç, ğ, ı, İ, ö, ş, ü.

## 5. Açılış ekranı

Açılış ekranında şunlar bulunsun:

- “CUMHURİYETİN İZİNDE” başlığı ve “BAYRAK AVCISI” alt başlığı
- Uçak, bayraklar ve bulutlarla kısa bir giriş animasyonu
- **Oyuna Başla**
- **Nasıl Oynanır?**
- **Seviye Seçimi**
- **Ses: Açık/Kapalı**
- **Yaş Grubu / Zorluk Seçimi**

Butonların tamamı çalışmalı. “Oyuna Başla” gerçek oyun ekranını açmalı. “Nasıl Oynanır?” kontrol açıklamalarını göstermeli. “Seviye Seçimi” seviye ekranına götürmeli.

## 6. Kontroller

### Bilgisayar
- Ok tuşları veya WASD ile uçağı yukarı, aşağı, sağa ve sola hareket ettir.
- `P` veya `Esc` ile oyunu duraklat/devam ettir.
- Uçak oyun alanının dışına çıkamasın.

### Dokunmatik ekran
- Ekranda yeterince büyük yön kontrolleri veya güvenilir dokunmatik sürükleme kontrolü sun.
- Kontroller oyun alanını kapatmasın.
- Dokunma hareketleri sayfa kaydırma yerine oyun kontrolünü çalıştırsın.
- Hem dikey hem yatay ekran boyutlarında arayüz kullanılabilir olsun.

Kontroller akıcı, duyarlı ve kolay öğrenilebilir olmalı.

## 7. Oyun mekaniği

- Oyun yatay ilerlemeli olsun; arka plan ve nesneler uçuş hissi verecek şekilde hareket etsin.
- Uçak oyuncu tarafından kontrol edilsin.
- Türk bayrakları farklı yüksekliklerde ve erişilebilir konumlarda belirsin.
- Uçak bayrağa değdiğinde bayrak kaybolsun, sayaç artsın ve puan eklensin.
- Kayalar ve sıcak hava balonları çarpışma engeli olarak çalışsın.
- Çarpışma algılama yalnızca görsel yakınlığa değil, gerçek oyun nesnelerinin konumlarına dayansın.
- Engelle çarpışma bir can eksiltsin; aynı çarpışma için birden fazla can eksilmesini önle.
- Çarpışma sonrası kısa bir hasar koruması veya geri bildirim ekle.
- Can sıfır olduğunda oyun dursun ve “Oyun Bitti” ekranı açılsın.
- Puan, kalan can, toplanan bayrak sayısı ve hedef oyun sırasında güncellensin.
- Duraklatma oyunun zamanını ve nesnelerin hareketini gerçekten durdursun.
- Yeniden başlatma puanı, canı, bayrakları, hızları ve nesne durumlarını doğru biçimde sıfırlasın.
- Oyuncuyu kaçınılmaz çarpışmaya zorlayan nesne düzenleri üretme.
- Oyun zamanla zorlaşsın; ancak seçilen yaş grubuna uygun sınırlar içinde kalsın.
- Puan veya bayrak toplama, aynı nesne için tekrar tekrar tetiklenemesin.

## 8. Seviyeler

Dört seviye oluştur:

1. **İstanbul'un Gökyüzü** — Kolay
2. **Anadolu'nun Rüzgârı** — Orta
3. **Cumhuriyet Yolunda** — Zor
4. **Geleceğe Uçuş** — İleri

Her seviyede:
- Farklı arka plan veya manzara kullan.
- Engel yoğunluğunu ve uçuş hızını kademeli olarak artır.
- Seviye hedefini ekranda göster.
- Hedef **10 Türk bayrağı** olsun.
- On bayrak toplanınca oyun akışı durup “Seviye Tamamlandı” ekranı açılsın.
- Sonraki seviyeye geçiş ve ana menüye dönüş seçenekleri çalışsın.
- Dördüncü seviye tamamlandığında final ekranı gösterilsin.

Seviye seçimi ekranında seviye adı, zorluk ve ilerleme bilgisi görünsün. Henüz açılmamış seviyeler varsa kilitli görünsün; kilit açma mantığı tutarlı çalışsın.

## 9. Puan, can ve ödül sistemi

- Her toplanan Türk bayrağı **10 puan** kazandırsın.
- Oyuncu **3 canla** başlasın.
- Her geçerli çarpışma bir can düşürsün.
- Seviye tamamlandığında yıldızlı başarı geri bildirimi göster.
- Final ekranında toplam puanı, toplanan bayrakları ve tamamlanan seviyeleri göster.
- Dört seviyeyi bitiren oyuncuya **“Cumhuriyetin Genç Kahramanı”** unvanını ver.
- Puanlar, sayaçlar ve can göstergeleri gerçek oyun durumuna bağlı olsun; yalnızca dekoratif olmasın.

## 10. Yaş grubu uyarlaması

Oyuncu yaş grubu seçebilsin:

- **Okul öncesi:** Yavaş hareket, büyük bayraklar, seyrek engeller, basit yönergeler.
- **İlkokul:** Kolay kontrol, dengeli hız, belirgin geri bildirim.
- **Ortaokul:** Daha çeşitli engeller ve orta düzey hız.
- **Lise:** Daha yüksek hız, daha karmaşık ama adil güzergâhlar.

Seçim oyun davranışını gerçekten değiştirsin. Yaş grubu değişince hız, engel sıklığı ve mümkünse bayrak görünürlüğü güncellensin.

## 11. Ses, erişilebilirlik ve kullanıcı deneyimi

- Ses açma/kapatma seçeneği çalışsın.
- Harici ses dosyaları olmadan kısa efektler gerekiyorsa Web Audio API kullan.
- Ses kapalı seçeneği tüm oyun efektlerini sustursun.
- Doğru geri bildirimleri yalnızca renkle ifade etme; metin ve simgeler de kullan.
- Metinleri okunaklı, kontrastı yeterli tut.
- Butonlar klavye ve dokunmatik kullanım için erişilebilir olsun.
- Hareketi azaltmaya yönelik bir seçenek ekle veya yoğun animasyonları sınırlı tut.
- Şiddet unsurları kullanma; çarpışma, hasar ve oyun sonu çocuklara uygun, yumuşak geri bildirimlerle sunulsun.

## 12. Ekranlar ve gezinme

Şu ekranları uygula:

1. Açılış ekranı
2. Nasıl oynanır?
3. Yaş grubu/zorluk seçimi
4. Seviye seçimi
5. Aktif oyun
6. Duraklatma
7. Seviye tamamlandı
8. Oyun bitti
9. Bütün seviyeler tamamlandı

Her ekranda uygun geri dönüş ve devam butonları bulunsun. Ekranlar arası geçişler doğru çalışsın. Oyuncu oyun sırasında yanlışlıkla menüye düşmesin.

## 13. EBA ve SCORM hazırlığı

- Oyun temel işlevleri için internet bağlantısı istemesin.
- Oyun tek `index.html` dosyası olarak çalışabilecek şekilde tasarlansın; çok dosyalı yapı seçilirse tüm gerekli dosyalar teslim edilsin.
- Kod yapısı SCORM 1.2 entegrasyonuna uygun olsun.
- SCORM API bulunmadığında oyun normal tarayıcıda hata vermeden çalışsın.
- SCORM entegrasyonu eklenirse tamamlanma durumu yalnızca oyun açıldığı için değil, tanımlanmış tamamlanma koşulları gerçekleştiğinde bildirilsin.
- SCORM entegrasyonunu test etmeden EBA'da kesin çalışacağı iddiasında bulunma.
- SCORM paketi istenirse doğru `imsmanifest.xml` dosyasını ve gerekli paket yapısını ayrıca hazırla.

## 14. Test kontrol listesi

Teslimden önce aşağıdakilerin her birini gerçek tarayıcı çalıştırmasıyla test et:

- [ ] Açılış ekranı yükleniyor.
- [ ] Oyuna Başla çalışıyor.
- [ ] Nasıl Oynanır ekranı açılıyor ve geri dönüş çalışıyor.
- [ ] Seviye seçimi çalışıyor.
- [ ] Klavye kontrolleri uçağı hareket ettiriyor.
- [ ] Dokunmatik kontroller çalışıyor.
- [ ] Uçak oyun alanının dışına çıkmıyor.
- [ ] Bayraklar toplanıyor ve puan doğru artıyor.
- [ ] Engellerle çarpışma algılanıyor.
- [ ] Her çarpışma yalnızca bir can eksiltiyor.
- [ ] Can sıfırlanınca oyun bitiyor.
- [ ] Duraklatma ve devam ettirme çalışıyor.
- [ ] Yeniden başlatma tüm değerleri sıfırlıyor.
- [ ] On bayrakla seviye tamamlanıyor.
- [ ] Sonraki seviye açılıyor.
- [ ] Dört seviye tamamlanınca final ekranı gösteriliyor.
- [ ] Ses açma/kapatma çalışıyor.
- [ ] Farklı ekran boyutlarında arayüz bozulmuyor.
- [ ] Tarayıcı konsolunda kritik hata bulunmuyor.
- [ ] Oyun internet bağlantısı olmadan açılıyor.

## 15. Teslim edilecekler

1. Çalışan oyun dosyası (`index.html` veya gerekli tüm kaynak dosyaları).
2. Oyunu bilgisayarda nasıl açacağını açıklayan kısa `README.md`.
3. Test kontrol listesinin sonucu; başarısız test varsa açıkça belirt.
4. SCORM 1.2 paketi oluşturulduysa ZIP paketi ve paketleme açıklaması.

**Öncelik sırası:** Önce temel oynanışı eksiksiz kur; ardından seviye sistemi, yaş grubu uyarlaması, sesler ve görsel iyileştirmeleri ekle. Son aşamada tüm kontrolleri test et ve hataları düzelt.
