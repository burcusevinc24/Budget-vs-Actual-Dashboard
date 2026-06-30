# 📊 Excel ile Dinamik Bütçe ve Gerçekleşen (Budget vs Actuals) Sapma Analizi Dashboard

Bu proje; planlanan bütçe hedefleri ile yıl içinde gerçekleşen harcamalar arasındaki farkları (**Sapma Analizi / Variance Analysis**) dinamik bir şekilde izlemek, analiz etmek ve raporlamak amacıyla geliştirilmiş interaktif bir Excel modelidir. 


---

## 🚀 Projenin Öne Çıkan Özellikleri & Teknik Yapısı

Panelin arka planında verilerin birbirini otomatik tetiklemesi ve kullanıcı dostu bir deneyim (UI/UX) sunması için şu teknik adımlar uygulanmıştır:

* **Dinamik Ay Seçimi (Data Validation):** Kullanıcı, panel üzerindeki açılır listeden (Dropdown) istediği ayı seçtiğinde tüm bütçe verileri, gerçekleşen harcamalar ve grafikler seçilen aya göre anlık olarak güncellenir.
* **Esnek Bütçe Sorgulama (INDEX & MATCH):** Matris formundaki bütçe tablosundan, seçilen aya ve ilgili harcama kalemine (satır/sütun kesişimine) denk gelen bütçe tutarlarını dinamik olarak çekmek için `INDEX` (İndis) ve `MATCH` (Kaçıncı) fonksiyonları kombinasyon halinde kullanılmıştır.
* **Otomatik Güncellenen Harcama Takibi (SUMIFS):** Harcama günlüğüne yeni veriler veya satırlar eklendikçe, `SUMIFS` (Çoketopla) fonksiyonu sayesinde bu veriler paneldeki ilgili ay ve kategori başlığı altında anlık olarak toplanır.
* **Görsel Sapma Analizi (Variance & Conditional Formatting):** Planlanan bütçe ile gerçekleşen tutar arasındaki farklar (Sapma) hesaplanmış; bütçe aşımlarını ve tasarrufları tek bakışta (scannable) fark edebilmek için `IF` mantığına dayalı **Koşullu Biçimlendirme** (Kırmızı/Yeşil uyarı sistemi) uygulanmıştır.
* **Veri Görselleştirme:** Bütçe ve gerçekleşen tutarların kategorisel karşılaştırmaları için **Sütun Grafikleri**, harcamaların genel dağılımını analiz etmek için ise **Pasta Grafikleri** kullanılarak kararları destekleyici bir görsel dil oluşturulmuştur.

---

## 📁 Dosya ve Sekme Mimarisi

Proje veri bütünlüğünü korumak adına 3 ana sekme (Tab) üzerine kurgulanmıştır:

1. **`Panel (Dashboard)`:** Kullanıcının ayı seçtiği, özet veri tablolarının, sapma analizlerinin ve grafiklerin yer aldığı ana yönetim ekranı.
2. **`Bütçe (Budget)`:** Yıl başında planlanan sabit/hedeflenen bütçe verilerinin yer aldığı yatay matris tablo.
3. **`Gerçekleşen (Actuals)`:** Yıl içinde yapılan harcamaların tarih, kategori ve tutar bazlı alt alta, dikey olarak kaydedildiği dinamik veri günlüğü.

---

## 🛠️ Kullanılan Teknolojiler ve Fonksiyonlar

* **Yazılım/Araç:** Microsoft Excel
* **Fonksiyonlar:** `INDEX` (İndis), `MATCH` (Kaçıncı), `SUMIFS` (Çoketopla), `IF` (Eğer)
* **Özellikler:** Veri Doğrulama (Data Validation), Koşullu Biçimlendirme (Conditional Formatting), Dinamik Grafik Yönetimi

---

💡 *Not: Projenin interaktif çalışmasını test etmek için dosyayı bilgisayarınıza indirip makro veya formülleri etkinleştirmeniz yeterlidir.*
