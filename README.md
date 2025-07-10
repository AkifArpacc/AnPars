# 📦 AnPars - Python Yardımcı Araçlar Kütüphanesi

**AnPars**, Python projelerinde sıkça ihtiyaç duyulan dosya işlemleri, metin temizleme, ağ bağlantı kontrolleri ve akıllı veri tipi dönüşümleri gibi işlemleri kolaylaştıran modüler bir yardımcı araç kütüphanesidir.

---

## 📁 Modüller ve Özellikleri

### ✅ `fs.py` - Dosya ve Klasör Yardımcıları

- `klasor_agaci(yol, derinlik=2)`  
  Belirtilen klasör yolunu ağaç yapısında string olarak gösterir.

- `otomatik_dosya_ismi_uret(dizin, dosya_adi)`  
  Aynı isimde dosya varsa otomatik olarak `(1)`, `(2)` gibi adlandırma yapar.

- `dosya_yedekle(dosya_yolu, yedek_klasor="yedekler")`  
  Dosyayı çakışma olmadan yedek klasörüne kopyalar.

- `dosya_boyutu_okunabilir(dosya_yolu)`  
  Dosya boyutunu okunabilir biçimde döner (örneğin `14.25 KB`).

---

### 🌐 `net.py` - Ağ ve İnternet Kontrolleri

- `internet_var_mi()`  
  İnternet bağlantısının olup olmadığını kontrol eder.

- `basit_get_istegi(url)`  
  Belirtilen URL’ye GET isteği atar, HTML içeriğini döner.

- `ip_adresi_al(hostname)`  
  Verilen hostname’in IP adresini alır.

- `port_acik_mi(host, port)`  
  TCP bağlantısıyla port açık mı kontrol eder.

- `url_gecerli_mi(url)`  
  URL biçimsel olarak geçerli mi kontrol eder.

- `ping_baglantisi_kontrol(host, port=80)`  
  TCP ping ile ağ bağlantısı kontrolü yapar.

---

### 🧠 `smart.py` - Akıllı Veri Dönüşümü

- `akilli_donusum(veri)`  
  String türündeki veriyi otomatik olarak Python türlerine çevirir. (int, float, bool, tarih, json, vs.)

- `veri_tipi_bilgisi(veri)`  
  Verinin tipi hakkında bilgi verir (`"int"`, `"bool"`, `"json"`, vs.).

---

### 🔤 `str.py` - Metin İşleme Araçları

Tüm fonksiyonlar ayrıca `StrUtils` sınıfı içinde de tanımlıdır:

- `turkce_karakter_cevir(metin)`  
  Türkçe karakterleri İngilizce karşılıklarına çevirir.

- `metin_temizle(metin)`  
  Boşluk ve özel karakterleri temizler.

- `slugify(metin)`  
  URL dostu hale getirir (`"Merhaba Dünya"` → `"merhaba-dunya"`).

- `kelime_say(metin)`  
  Kelime sayısını döner.

- `sesli_harf_say(metin)`  
  Türkçe sesli harf sayısını döner.

- `sessiz_harf_say(metin)`  
  Türkçe sessiz harf sayısını döner.

---

## 🧪 Testler

Tüm modüller için `tests/` klasörü altında `unittest` temelli test dosyaları yazılmıştır:

```bash
python -m unittest discover tests
