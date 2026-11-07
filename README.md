# Kabul Kontrol · Windows yayınları

Kabul Kontrol ve Olympos Ekran Tanısı için imzalı güncelleme kanalı ve Windows x64 paketleri.

| Uygulama | Sürüm | İndir |
|---|---|---|
| Kabul Kontrol | 0.7.2 | [ZIP indir](https://github.com/TraxleAdmin/kabul-kontrol-updates/releases/download/v0.7.2/KabulKontrol-Windows-x64-0.7.2.zip) |
| Olympos Ekran Tanısı | 0.2.0 | [ZIP indir](https://github.com/TraxleAdmin/kabul-kontrol-updates/releases/download/v0.2.0-probe/Olympos-Ekran-Tanisi-Windows-x64-0.2.0.zip) |

## İlk kurulum

ZIP’i ayrı bir klasöre tamamen çıkarın. Kabul Kontrol için `KabulKontrol.exe`, tanı aracı için `OlymposEkranTanisi.exe` dosyasını açın. EXE, yanındaki çalışma dosyalarıyla birlikte kullanılmalıdır. Önceki sürümü kapatın; açık çalışmayı kaydedin.

0.5.0 ve üstündeyseniz güncellemeyi uygulama içinden alabilirsiniz. Daha eski sürümlerden ilk geçişte ZIP’i kullanın. Yayınları **Yardım → Güncellemeleri Kontrol Et…** menüsünden kontrol edin. Yeni sürüm bulunduğunda indirin; doğrulama tamamlanınca **Yeniden Aç ve Güncelle** ile uygulayın. İndirme veya yeni sürümün açılması başarısız olursa mevcut kurulum korunur.

## Olympos tanısı

Birden fazla Olympos penceresi varsa tanı aracında doğru pencereyi seçin. Hedef kapanırsa listeyi yenileyin. Tanı raporu tüm ürünlerin veya kaydırma dışındaki satırların okunduğunu kanıtlamaz; uygulama Olympos kaydını değiştirmez.

## Doğrulama kapsamı

Yerel birim testleri, imzalı paket hazırlama, yeni EXE açılışı ve etkin sürüme yönlenme doğrulandı. Gerçek Olympos ve hedef işyeri bilgisayarı ayrıca test gerektirir. Orijinal fotoğraf çifti ve üç Olympos ekranı/dört fatura sayfası için JSON/CSV regresyonları son EXE’de geçti. Son EXE’nin yerel soğuk fotoğraf ve yedi kaynaklı JSON ölçümleri yaklaşık 13–14 saniyedir; 5–6 saniye hedefi karşılanmadı.

Faturalar ve tanı raporları güncelleme hizmetine yüklenmez. Bu depoda yayın açıklaması ve imzalı sürüm bildirimleri bulunur; Windows paketleri Releases bölümündedir. Üçüncü taraf lisansları ZIP’lerde yer alır.

## Otomatik günlük föy

Otomatik föy başlangıçta kapalıdır; numara kaynağı varsayılan Kayıt No’dur. Föy Alanları değişikliğinden sonra Olympos ve fatura kapsam onaylarını yeniden verip Karşılaştır seçin.

**Föy Ayarları** bölümünde çıktı klasörünü seçin ve otomatik kaydı açın. Dosya, Olympos **Kabul Tarihi** ile `YIL/GG.AA.ods` yoluna hazırlanır. FİRMA ADI, İRSALİYE NO, KAYIT NO ve TARİH sütunları kullanılır. TARİH sütunu varsayılan olarak evrak tarihidir; kabul tarihi ayrıca seçilebilir. KAYIT NO için Olympos Kayıt No veya Sistem No açıkça seçilir; bu alanlar birbirinin yerine kullanılmaz.

Varsayılan kayıt yalnız iki kaynağın kapsamı/alanları onaylanmış ve karşılaştırması uyumlu kayıtlarda yapılır. Eksik veya belirsiz kabul tarihi, firma ya da seçilen numara varsa **Föy Alanları** ile kaynak üzerinden doğrulayın ve yeniden onaylayıp karşılaştırın. Aynı günlük dosyada tekrarlanan kayıt eklenmez; çelişen kayıt üzerine yazılmaz. Mevcut dosya değiştirilmeden önce yedek alınır. Föy Excel/LibreOffice’te açıksa kapatıp yeniden karşılaştırın. Başarılı föy kaydı uygulamada ayrıca gösterilir.

Belge numarasının önekindeki I/1 veya O/0 şüphesinde bağımsız alan okuması kullanılır. İki okuma uyuşmazsa numara doğrulanmış sayılmaz; kullanıcı incelemesi gerekir. SH1 gibi geçerli bir önek körlemesine SHI yapılmaz.

## 0.7.1 okuma kontrolleri

Düşük güvenli belge numarası, barkod ve miktar hücreleri hedefli olarak yeniden okunur. Tarihler ilgili etiketin önceliğiyle seçilir; çelişen veya doğrulanamayan değerler bilinmiyor kalır. Geçersiz standart GTIN kontrol rakamı kullanıcı kapsam onayıyla geçerli sayılmaz. Aynı barkod ve birim altındaki farklı ürün adlarının eşit toplamları tek başına uyum kanıtı değildir. İlk OCR güveni ve kanıtı kullanıcı onayından ayrı korunur; güven puanı doğruluk yüzdesi değildir.

593 birim testi ve sağlayıcı/insan onayları simüle edilen 15 yerel Tk senaryosu geçti. Son EXE’de bir işleme ait iki gerçek fotoğrafta önceden belirlenmiş 46 sayı/barkod/tarih alanı doğru okundu. Önceki sürüm de aynı küçük referansta doğruydu; bu kontrol gerileme olmadığını gösterir, genel doğruluk yüzdesini kanıtlamaz. Tam ürün adları ve görünmeyen sayfalar bu ölçüme dahil değildir. Sorun çıkan gerçek belgelerle daha geniş doğrulama gerekir.

## Otomatik föy düzeltmesi

Föy Alanları'nda firma, kabul tarihi ve kayıt bilgileri düzenlenince mevcut ürün eşleştirmeleri korunur. İki kaynağın kapsamını yeniden onaylayıp Karşılaştır'a basın; kayıt uygunsa günlük dosyaya otomatik yazılır. Sistem No seçiliyken yalnız kullanılmayan Kayıt No alanına ait olduğu doğrulanan uyarılar kayıt engeli değildir. Diğer belirsizliklerin giderilmesi gerekir.

Yazma başarısız olursa neden durum satırında kalır; açık karşılaştırmada ayrıca uyarı gösterilir. Başarı mesajında dosyanın tam yolu bulunur: seçilen klasör/YIL/GG.AA.ods. Ayarları kaydettikten sonra yeni karşılaştırma başlatılmalıdır. Otomatik kaydın açık olması tek başına eksik alan/onay kontrollerini geçersiz yapmaz.

Yerel 15 Tk senaryosunda onaylı ürün eşleştirmesi, föy alanı düzenlemesi, iki kaynağın tekrar onaylanması ve gerçek geçici ODS yazımı birlikte doğrulandı. Tekrar kayıt engeli ve yazma hatasından sonra açık tekrar denemesi geçti. Sağlayıcılar ve insan onayları simüle edildi; gerçek işyeri dosyası ve ekranı ayrıca doğrulanmalıdır.

## 0.7.2 Olympos görüntü doğrulaması

İlk okumada Kabul Kontrol artık gizlenmez. İlk okuma ve sonraki doğrulama, Olympos'u öne getirmeden aynı hedef pencere yakalama yöntemiyle çalışır. Windows'un geometrisini doğruladığı etkin iç kayıt penceresinde başlık/çerçeve boyası veri değişikliği sayılmaz. OCR yalnız korunan iş alanını okur; bu alandaki pikseller, kayıt kimliği, yerleşim ve kaydırma konumları korunur. Belirsiz geometri, kaynak popup'ı veya üstteki kayıt penceresinin örtüşmesinde tam görüntünün birebir kontrolü sürer. Genel piksel toleransı kullanılmaz.

Doğrulama başarısız olduğunda uyarı, kaydın kesin değiştiğini iddia etmez. Yerel alan okumasının kimlik kontrolü kabul tarihi, firma, kayıt kimlikleri ve satır/ürün kimliklerini de kapsar. Güncelleme sonrasında mevcut kaydı Olympos'u Oku ile yeniden alın.

623 birim testi ve 15 yerel Tk/föy senaryosu geçti. Gerçek Windows/Pillow testinde tamamen örtülü ve pasif sentetik kaynak üç kez aynı okundu; 12→13 miktar değişimi yakalandı. Bu test gerçek Olympos sağlayıcısının veya işyeri bilgisayarının doğrulandığı anlamına gelmez. İş alanı içindeki seçim, kaydırma veya veri değişiklikleri yeniden okuma gerektirebilir.
