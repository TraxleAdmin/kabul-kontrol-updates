# Kabul Kontrol · Windows yayınları

Kabul Kontrol ve Olympos Ekran Tanısı için imzalı güncelleme kanalı ve Windows x64 paketleri.

| Uygulama | Sürüm | İndir |
|---|---|---|
| Kabul Kontrol | 0.6.0 | [ZIP indir](https://github.com/TraxleAdmin/kabul-kontrol-updates/releases/download/v0.6.0/KabulKontrol-Windows-x64-0.6.0.zip) |
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
