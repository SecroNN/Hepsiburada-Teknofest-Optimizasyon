# Hepsiburada Yapay Zeka Destekli Lojistik Anahat Optimizasyonu - MVP Çözümü

Bu repository, Hepsiburada'nın sağladığı veri setini kullanarak 11-17 Mayıs 2026 haftası için operasyonel kısıtlara uygun desi tahminlemesi ve spot araç optimizasyonu yapan algoritmayı içermektedir.

**Operasyonel Kısıtlar ve Mimari:**
* Talep tahmini `Prophet` makine öğrenmesi modeli ile yapılmıştır.
* Teslimat dosyaları, jüri tarafından istenen sütun yapılarına (Tarih, Araç Tipi, Çıkış TM, Varış TM, Atanan Desi, Maliyet vb.) tam uyumlu şekilde üretilmiştir.
* Transfer merkezlerindeki kiralık araçlar rotalara öncelikli atanmış, günlük kira ve km maliyetleri PDF'deki kurala uygun olarak hesaba dahil edilmiştir.
* Spot araç atamalarında jürinin belirlediği "Minimum %10 Doluluk" kuralına sıkı sıkıya uyulmuş; bu kısıtı sağlayamayan küçük hacimli açıklar Rollover (ertesi güne devir) algoritmasıyla planlanmıştır.

### Toplam Sistem Maliyeti
(Sabit Kiralık Araçların "Kira + Km" Maliyetleri ve Optimize Edilmiş Spot Araç Maliyetleri Toplamı)
11-17 MAYIS HAFTALIK TOPLAM SİSTEM MALİYETİ: 9.755.766,35 TL
