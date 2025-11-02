# 🇹🇷 Nutuk 1. Cilt — Türkçe Doğal Dil İşleme Veri Seti (600-QA) V2.0

> "Efendiler, bu nutuklarım, bir devrin hikâyesidir..."
> — Gazi Mustafa Kemal ATATÜRK, 1927

**Depo:** https://github.com/mehmetaksoy/Nutuk-Turkce-NLP-Dataset

[![Veri Kalitesi](https://img.shields.io/badge/veri_kalitesi-100%25-brightgreen)]()
[![Soru Sayısı](https://img.shields.io/badge/sorular-600-blue)]()
[![Kategori](https://img.shields.io/badge/kategoriler-41-orange)]()
[![Lisans](https://img.shields.io/badge/lisans-CC_BY_4.0-green)]()

---

## İçindekiler

- [📘 Hakkında](#-hakkında)
- [✨ Yeni Özellikler (v2.0)](#-yeni-özellikler-v20)
- [📖 Kaynak ve Kapsam](#-kaynak-ve-kapsam)
- [📂 Veri Dosyaları](#-veri-dosyaları)
- [📊 Kaynak Metin İstatistikleri (NUTUK_1.txt)](#-kaynak-metin-i̇statistikleri-nutuk_1txt)
- [🎯 Amaç ve Kullanım Alanları](#-amaç-ve-kullanım-alanları)
- [⚙️ Ön‑İşleme Süreci](#️-ön-işleme-süreci)
- [🧩 Veri Şeması](#-veri-şeması)
- [📊 Veri Seti İstatistikleri](#-veri-seti-i̇statistikleri)
- [💡 Örnek Kayıtlar](#-örnek-kayıtlar)
- [✅ Kalite Güvencesi](#-kalite-güvencesi)
- [🧠 Kalite ve Sınırlılıklar](#-kalite-ve-sınırlılıklar)
- [🗓️ Sürümleme](#️-sürümleme)
- [⚖️ Lisans ve Hukuki Not](#-lisans-ve-hukuki-not)
- [🤝 Katkı ve İletişim](#-katkı-ve-iletişim)
- [📜 Atıf](#-atıf)
- [🙏 Teşekkür](#-teşekkür)

---

## 📘 Hakkında

Bu çalışma, Gazi Mustafa Kemal ATATÜRK'ün **Nutuk** adlı eserinin **1. cildinden** özenle işlenmiş, Türkçe doğal dil işleme (NLP), fine‑tuning, embedding eğitimi, RAG (Retrieval-Augmented Generation), soru-cevap sistemleri ve benzeri yapay zekâ araştırmaları için hazırlanmış **%100 doğrulukla verifikasyondan geçmiş veri setini** içerir.

**600 soru-cevap çifti**, kaynak metinle karakter düzeyinde doğrulanmış, 41 farklı kategoride yapılandırılmış ve her kayıt için detaylı metadata sağlanmıştır.

Amaç; bilgisayarların **Türkçeyi daha doğru, doğal ve yabancılaşmamış biçimde** öğrenmesine katkı sunmak, ATATÜRK'ün dilindeki ifade gücünü modern algoritmaların anlayabileceği biçime kazandırmaktır.

---

## ✨ Yeni Özellikler (v2.0)

### 🎯 %100 Veri Doğruluğu

- ✅ Tüm 600 soru kaynak metinle satır satır doğrulandı
- ✅ chunk_id referansları tam doğru (TEXT_LINE_XXXX formatı)
- ✅ Unicode karakterler kaynak metinle normalize edildi
- ✅ Hiç tekrar eden soru yok
- ✅ Hiç boş alan yok

### 📊 Zengin Metadata

- **10 alan** ile detaylı bilgi: id, category, question, answer, chunk_id, support_scope, support_excerpt, audit_status, support_method, match_detail
- **41 kategori** ile çok boyutlu sınıflandırma
- **Kaynak metin referansları** her soru için satır düzeyinde

### 🔍 Profesyonel Yapılandırma

- **577 soru (%96.2):** Direct/exact_quote (doğrudan alıntı)
- **23 soru (%3.8):** Contextual/text_match (bağlamsal)
- Tüm sorular "verified" ve "content_verified" durumunda

---

## 📖 Kaynak ve Kapsam

- **Ana kaynak:** *Mustafa Kemal ATATÜRK – Nutuk (Orijinal Metin), 1927 baskısı.*
- **Metin kaynağı:** İnternet Arşivi'nde bulunan orijinal **OCR (Full Text)** sürümünden alınmıştır.
- **Kapsam:** **1–334. sayfalar** arası içerik (2. cilde geçilen 335. sayfa itibarıyla durdurulmuştur).
- **OCR bilgisi:** *Tesseract 5, 300 PPI, tur+Latin parametreleri.*

> Not: OCR metni yer yer tarihsel imlâyı yansıtır; temizlik ve düzenleme adımlarında dil birliği gözetilmiştir.

---

## 📂 Veri Dosyaları

```
/
├── NUTUK_1.txt                              # Temizlenmiş 1. cilt metni (2,914 satır, 802 KB)
├── nutuk_qa_birlesik_revize_final.json      # 600 soru-cevap veri seti (959 KB)
├── .gitignore                               # Git yapılandırması
└── README.md                                # Bu dosya
```

- **NUTUK_1.txt:** Başlık, paragraf ve cümle yapısı korunarak sadeleştirilmiş kaynak metin.
- **nutuk_600_sorular_DUZELTILMIS.json:** Kaynak metinle %100 doğrulanmış, 41 kategoride **soru‑cevap** veri seti.

---

## 📊 Kaynak Metin İstatistikleri (NUTUK_1.txt)

Veri setinin temelini oluşturan kaynak metin **NUTUK_1.txt**, Gazi Mustafa Kemal ATATÜRK'ün 1927 yılında verdiği nutukun 1. cildinin dijitalleştirilmiş tam metnidir.

### 📈 Temel Metrikler

| Metrik                 | Değer                           |
| ---------------------- | ------------------------------- |
| 📦 **Dosya Boyutu**     | 821,455 byte (802.2 KB)         |
| 📄 **Toplam Satır**     | 2,914 satır                     |
| 📝 **Dolu Satır**       | 2,912 satır                     |
| 🔤 **Karakter Sayısı**  | 763,136 karakter (boşluk dahil) |
| 📖 **Kelime Sayısı**    | 97,294 kelime                   |
| 🎯 **Benzersiz Kelime** | 23,587 benzersiz kelime         |
| 📋 **Cümle Sayısı**     | 6,542 cümle                     |

### 📚 Dil İstatistikleri

- **Ortalama Kelime/Cümle:** 14.9 kelime
- **Ortalama Kelime Uzunluğu:** 6.8 karakter
- **Type-Token Ratio (TTR):** 24.24% (leksikal çeşitlilik)

### 🔝 En Sık Kullanılan Kelimeler

| Sıra | Kelime | Frekans | Yüzde |
| ---- | ------ | ------- | ----- |
| 1    | ve     | 4,499   | %4.62 |
| 2    | bir    | 1,765   | %1.81 |
| 3    | bu     | 964     | %0.99 |
| 4    | Bu     | 534     | %0.55 |
| 5    | ile    | 461     | %0.47 |
| 6    | olan   | 450     | %0.46 |
| 7    | için   | 441     | %0.45 |
| 8    | de     | 438     | %0.45 |
| 9    | Paşa   | 406     | %0.42 |
| 10   | milli  | 396     | %0.41 |

### 📅 Tarihsel İçerik

- **Yıl Referansları:** 461 toplam (14 benzersiz yıl)
- **En Çok Geçen Yıllar:** 1919 (296 kez), 1920 (120 kez), 1927 (23 kez)
- **Tarih Formatı:** 305 adet (Gün Ay formatında)

> Bu metrikler, kaynak metnin **97 bin kelimelik zengin bir corpus** olduğunu ve 23 bin benzersiz kelime ile Türkçe NLP çalışmaları için yüksek leksikal çeşitliliğe sahip olduğunu göstermektedir.

---

## 🎯 Amaç ve Kullanım Alanları

Bu veri seti, Türkçe dilinde çalışan doğal dil işleme sistemlerinin **doğallık, anlam derinliği ve tarihsel bağlam** kapasitesini artırmak amacıyla hazırlanmıştır.

**Kullanım alanları:**

- 🤖 **LLM Fine-tuning:** Türkçe dil modellerinin özelleştirilmesi
- 🔍 **RAG Sistemleri:** Retrieval-Augmented Generation uygulamaları
- 📊 **Embedding Eğitimi:** Semantik arama ve vektör veritabanları
- 💬 **Soru-Cevap Sistemleri:** Q&A bot geliştirme
- 📖 **Metin Anlama:** Reading comprehension ve bilgi çıkarımı
- 🎓 **Akademik Araştırma:** NLP, tarih, dilbilim çalışmaları
- 🌐 **Çok-dilli Modeller:** Türkçe destekli uluslararası sistemler
- 📚 **Tarihsel Metin Analizi:** Dijital beşeri bilimler

> Bu veri seti, sadece teknolojik değil; **kültürel sürekliliği** koruyan bir katkı olarak tasarlanmıştır.

---

## ⚙️ Ön‑İşleme Süreci

### 1️⃣ Kaynak Seçimi

İnternet Arşivi'ndeki [Nutuk orijinal OCR sürümünden](https://archive.org/details/mustafa-kemal-ataturk-nutuk-orijinal-metin) metin çıkarımı yapıldı.

### 2️⃣ Temizlik

- Satır kırılımları ve paragraf düzeni onarıldı.
- Sayfa numaraları, dipnotlar ve kesme işaretleri temizlendi.
- OCR kaynaklı hatalar düzeltildi, dil birliği sağlandı.

### 3️⃣ Yapılandırma

- Metin; cümle, başlık ve paragraf düzeyinde anlam bütünlüğü korunarak düzenlendi.
- 2,914 satıra bölünerek TEXT_LINE_XXXX formatında indexlendi.

### 4️⃣ QA Üretimi

- 600 soru-cevap çifti oluşturuldu
- 41 farklı kategoride sınıflandırıldı
- Soru-cevap çiftleri ve kategoriler otomatik üretilip, manuel olarak doğrulandı

### 5️⃣ Doğrulama (%100 Accuracy)

- **Aşama 1:** chunk_id satır kaymaları düzeltildi
- **Aşama 2:** Unicode apostrophe normalizasyonu
- **Aşama 3:** Başlık-içerik hizalaması
- **Aşama 4:** Editorial içerik temizleme
- **Aşama 5:** Tırnak işareti standartlaştırma
- **Sonuç:** 600/600 soru kaynak metinle %100 eşleşme

---

## 🧩 Veri Şeması

Her kayıt aşağıdaki **10 alanı** içerir:

```jsonc
{
  "id": 1,                                    // Benzersiz soru numarası (1-600)
  "category": "Bilgi",                        // Soru kategorisi (41 farklı kategori)
  "question": "Mustafa Kemal Paşa'nın Samsun'a çıkış tarihi nedir?",
  "answer": "Mustafa Kemal Paşa 1919 senesi Mayıs'ının 19. günü Samsun'a çıkmıştır.",
  "chunk_id": "TEXT_LINE_0285",               // Kaynak metnin satır referansı
  "support_scope": "direct",                  // "direct" veya "contextual"
  "support_excerpt": "1919 senesi Mayıs'ının 19. günü Samsun'a çıktım.",
  "audit_status": "verified",                 // Doğrulama durumu
  "support_method": "exact_quote",            // "exact_quote" veya "text_match"
  "match_detail": "content_verified"          // Eşleşme detayı
}
```

### Alan Açıklamaları

| Alan              | Tip     | Açıklama                                                 |
| ----------------- | ------- | -------------------------------------------------------- |
| `id`              | integer | 1-600 arası benzersiz soru kimliği                       |
| `category`        | string  | 41 kategoriden biri (detay aşağıda)                      |
| `question`        | string  | Soru metni (33-292 karakter)                             |
| `answer`          | string  | Cevap metni (35-1,310 karakter)                          |
| `chunk_id`        | string  | Kaynak metin satır referansı (TEXT_LINE_0001 formatında) |
| `support_scope`   | string  | "direct" (doğrudan alıntı) veya "contextual" (bağlamsal) |
| `support_excerpt` | string  | Kaynak metinden ilgili bölüm (37-3,027 karakter)         |
| `audit_status`    | string  | "verified" (tüm kayıtlar doğrulanmış)                    |
| `support_method`  | string  | "exact_quote" veya "text_match"                          |
| `match_detail`    | string  | "content_verified" (içerik doğrulanmış)                  |

---

## 📊 Veri Seti İstatistikleri

### Genel Bilgiler

- **Toplam Soru:** 600
- **Kategori Sayısı:** 41
- **Benzersiz chunk_id:** 301 farklı satır
- **Doğruluk Oranı:** %100

### Kategori Dağılımı (Top 10)

| Kategori                    | Soru Sayısı |
| --------------------------- | ----------- |
| Halkla İlişkiler            | 27          |
| Bilgi                       | 20          |
| Neden-sonuç                 | 20          |
| Amaç                        | 20          |
| Yorum/Anlam çıkarımı        | 20          |
| Özet/Genel bilgi            | 20          |
| Askeri Strateji             | 20          |
| Milli Mücadele Stratejileri | 20          |
| sosyal_değişim              | 20          |
| ideolojik_dönüşüm           | 20          |

<details>
<summary>📋 Tüm Kategoriler (41 adet)</summary>


- Amaç (20)
- Askeri Strateji (20)
- Askeri Örgütlenme (10)
- Askerî Organizasyon (10)
- Bilgi (20)
- Devrim Süreci (15)
- Diplomatik İlişkiler (10)
- Felsefi Yaklaşımlar (16)
- Gelecek Vizyonu (17)
- Halk Katılımı (10)
- Halkla İlişkiler (27)
- Hukukî Meseleler (10)
- Kavramsal Analiz (10)
- Kriz Yönetimi (10)
- Kurumsal Gelişim (10)
- Liderlik Felsefesi (15)
- Liderlik ve Karar Alma (10)
- Milli Mücadele Stratejileri (20)
- Neden-sonuç (20)
- Sivas Kongresi (10)
- Siyasi Analiz (10)
- Siyasi Mücadele (10)
- Tarih Perspektifi (17)
- Tarihsel Analiz (10)
- Teşkilatlanma (10)
- Uluslararası İlişkiler (10)
- Yorum/Anlam çıkarımı (20)
- devrimci_perspektif (13)
- ideolojik_dönüşüm (20)
- liderlik_ozellikleri (12)
- milliyetçilik (20)
- modernleşme_vizyonu (20)
- siyasi_strateji (20)
- sosyal_değişim (20)
- stratejik_ongoru (13)
- tarihsel_degerlendirme (12)
- Örgütsel Yapılanma (17)
- Özet/Genel bilgi (20)
- İdarî Reformlar (10)
- İletişim Stratejileri (16)
- İstanbul Hükümeti İlişkileri (10)

</details>

### Support Scope Dağılımı

| Tip                      | Soru Sayısı | Yüzde |
| ------------------------ | ----------- | ----- |
| direct (doğrudan alıntı) | 577         | %96.2 |
| contextual (bağlamsal)   | 23          | %3.8  |

### Uzunluk İstatistikleri

| Alan    | Min  | Max   | Ortalama     |
| ------- | ---- | ----- | ------------ |
| Soru    | 33   | 292   | 121 karakter |
| Cevap   | 35   | 1,310 | 532 karakter |
| Excerpt | 37   | 3,027 | 587 karakter |

---

## 💡 Örnek Kayıtlar

### Örnek 1: Bilgi Kategorisi

```json
{
  "id": 9,
  "category": "Bilgi",
  "question": "Erzurum Kongresi kaç gün devam etti?",
  "answer": "Erzurum Kongresi 14 gün devam etti.",
  "chunk_id": "TEXT_LINE_0684",
  "support_scope": "direct",
  "support_excerpt": "Efendiler, Erzurum Kongresi 14 gün devam etti. Mesaisinin neticesi, tespit ettiği nizamname ve bu nizamname muhteviyatını ilan eden beyanname! içinde yer alanlardan ibarettir.",
  "audit_status": "verified",
  "support_method": "exact_quote",
  "match_detail": "content_verified"
}
```

### Örnek 2: Amaç Kategorisi

```json
{
  "id": 41,
  "category": "Amaç",
  "question": "Mustafa Kemal'in Samsun'a çıkışının temel amacı neydi?",
  "answer": "Mustafa Kemal'in Samsun'a çıkışının temel amacı, genel vaziyet ve manzarayı değerlendirerek milli kurtuluş hareketini başlatmak ve organize etmekti.",
  "chunk_id": "TEXT_LINE_0285",
  "support_scope": "direct",
  "support_excerpt": "1919 senesi Mayıs'ının 19. günü Samsun'a çıktım. Genel vaziyet ve manzara:",
  "audit_status": "verified",
  "support_method": "exact_quote",
  "match_detail": "content_verified"
}
```

### Örnek 3: Neden-Sonuç Kategorisi

```json
{
  "id": 26,
  "category": "Neden-sonuç",
  "question": "Mustafa Kemal neden Tokat'ta telgrafhaneyi kontrol altına aldırdı?",
  "answer": "Mustafa Kemal ulaştığının Sivas'a ve hiçbir tarafa bildirilmemesini temin etmek için Tokat'ta telgrafhaneyi kontrol altına aldırdı.",
  "chunk_id": "TEXT_LINE_0512",
  "support_scope": "direct",
  "support_excerpt": "Tokat'a varır varmaz telgrafhaneyi kontrol altına aldırarak benim ulaştığımın Sivas'a ve hiçbir tarafa bildirilmemesini temin ettim.",
  "audit_status": "verified",
  "support_method": "exact_quote",
  "match_detail": "content_verified"
}
```

---

## ✅ Kalite Güvencesi

### Doğrulama Süreci

Tüm 600 soru aşağıdaki kalite kontrol adımlarından geçirilmiştir:

#### ✅ Teknik Doğrulama

- **JSON Format:** Geçerli JSON yapısı, syntax hatası yok
- **ID Kontrolü:** 1-600 arası tüm ID'ler mevcut, tekrar yok, sıralı
- **Alan Eksiksizliği:** Her kayıtta 10 alan tam ve dolu
- **chunk_id Format:** TEXT_LINE_XXXX formatı %100 tutarlı

#### ✅ İçerik Doğrulama

- **Kaynak Eşleşme:** Her support_excerpt kaynak metinde mevcut
- **Satır Referansı:** chunk_id doğru satırı işaret ediyor
- **Unicode Uyumu:** Karakterler kaynak metinle normalize
- **Scope-Method Tutarlılığı:** direct→exact_quote, contextual→text_match

#### ✅ Kalite Metrikleri

- **Tekrar Eden Soru:** 0/600 (✅ Yok)
- **Boş Alan:** 0/6000 (✅ Yok)
- **chunk_id Doğruluğu:** 600/600 (%100 ✅)
- **Kaynak Eşleşme:** 600/600 (%100 ✅)
- **Metadata Tutarlılığı:** 600/600 (%100 ✅)

### Düzeltme İstatistikleri

Toplam **29 benzersiz soru** düzeltildi (bazı sorular birden fazla düzeltme aldı):

| Düzeltme Türü           | Soru Sayısı |
| ----------------------- | ----------- |
| chunk_id satır kayması  | 12          |
| Unicode apostrophe      | 7           |
| Başlık hizalama         | 2           |
| Editorial içerik        | 1           |
| Tırnak standartlaştırma | 3           |

**Sonuç:** %100 veri doğruluğu garantisi

---

## 🧠 Kalite ve Sınırlılıklar

### ✅ Güçlü Yönler

- ✅ **%100 Doğruluk:** Her kayıt kaynak metinle doğrulanmış
- ✅ **Zengin Metadata:** 10 farklı alan ile detaylı bilgi
- ✅ **Çok Kategorili:** 41 farklı perspektif
- ✅ **Kaynak Referanslı:** Satır düzeyinde izlenebilirlik
- ✅ **Unicode Normalized:** Karakter standardizasyonu yapılmış

### ⚠️ Sınırlılıklar

- OCR kaynaklı **eski imlâ** farkları yer yer korunmuştur
- **Navigasyonel** sorular yok (ör. "burada/şurada ne diyor?")
- Sadece **1. cilt** kapsamlı (sayfa 1-334)
- **Tarihsel bağlam** gerektirir (1919-1927 dönemi)

### 📝 Kullanım Önerileri

- RAG sistemlerinde chunk_id ile doğrudan kaynak erişimi
- Fine-tuning'de category bazlı filtreleme
- Embedding eğitiminde support_scope gözetimi
- Soru-cevap sistemlerinde exact_quote önceliği

---

## 🗓️ Sürümleme

### v2.0 — 2 Kasım 2024 🎉

- ✅ **%100 Doğruluk** garantisi ile yeniden yayımlandı
- ✅ 600 soru kaynak metinle satır satır doğrulandı
- ✅ Unicode karakterler normalize edildi
- ✅ chunk_id referansları düzeltildi
- ✅ 41 kategoriye genişletildi
- ✅ 10 alan ile zengin metadata
- ✅ Profesyonel veri şeması
- 📄 Dosya adı: `nutuk_600_sorular_DUZELTILMIS.json`

### v1.0 — 29 Ekim 2024

- İlk kamu yayımlaması (1–334. sayfalar, örnek QA)
- 📄 Dosya adı: `nutuk_qa_birlesik_revize_final.json`

---

## ⚖️ Lisans ve Hukuki Not

### Metin Lisansı

**Nutuk (1927)** — Türkiye'de, müellifin vefatından 70 yıl geçtiği için **kamu malıdır (public domain)**.

### Veri Seti Lisansı

**JSON/İşlenmiş Çıktılar:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

### Kod Lisansı

**Betikler (varsa):** MIT License

### Kullanım Şartları

- ✅ Akademik ve ticari kullanım serbest
- ✅ Değiştirme ve dağıtma izni var
- ⚠️ Atıf zorunlu (aşağıdaki bölüme bakın)
- ⚠️ Lisans metnini koruyun

---

## 🤝 Katkı ve İletişim

**Pull Request** ve **Issue**'lara açıktır. Yeni eklemeler, düzeltmeler veya Türkçe NLP projeleriyle entegrasyon önerileri memnuniyetle karşılanır.

### Katkı Alanları

- 🐛 Hata bildirimi
- 💡 Yeni kategori önerileri
- 📝 Ek soru-cevap çiftleri
- 🔧 Veri kalitesi iyileştirmeleri
- 📚 Dokümantasyon güncellemeleri
- 🌐 Çoklu dil desteği

### İletişim

- **GitHub Issues:** [Yeni Issue Aç](https://github.com/mehmetaksoy/Nutuk-Turkce-NLP-Dataset/issues)
- **Pull Requests:** [PR Gönder](https://github.com/mehmetaksoy/Nutuk-Turkce-NLP-Dataset/pulls)
- **Depo:** https://github.com/mehmetaksoy/Nutuk-Turkce-NLP-Dataset

---

## 📜 Atıf

Bu veri setini akademik/teknik çalışmalarda kullanırken lütfen aşağıdaki atıflardan birini yapınız.

### Türkçe (önerilen)

> Mehmet Aksoy, *Nutuk 1. Cilt — Türkçe Doğal Dil İşleme Veri Seti* (sürüm v2.0), GitHub deposu, 2 Kasım 2024. Erişim: https://github.com/mehmetaksoy/Nutuk-Turkce-NLP-Dataset

### IEEE Stili

> [1] M. Aksoy, "Nutuk 1. Cilt — Türkçe Doğal Dil İşleme Veri Seti (v2.0)," GitHub repository, Nov. 2, 2024. [Online]. Available: https://github.com/mehmetaksoy/Nutuk-Turkce-NLP-Dataset

### APA Stili

> Aksoy, M. (2024). *Nutuk 1. Cilt — Türkçe Doğal Dil İşleme Veri Seti* (v2.0) [GitHub repository]. https://github.com/mehmetaksoy/Nutuk-Turkce-NLP-Dataset

### BibTeX

```bibtex
@misc{nutuk_tr_nlp_v2_2024,
  title        = {Nutuk 1. Cilt --- Türkçe Doğal Dil İşleme Veri Seti},
  author       = {Aksoy, Mehmet},
  year         = {2024},
  month        = {11},
  howpublished = {\url{https://github.com/mehmetaksoy/Nutuk-Turkce-NLP-Dataset}},
  note         = {Sürüm v2.0, GitHub repository, %100 doğrulukla verifikasyondan geçmiş 600 soru-cevap veri seti},
  version      = {2.0}
}
```

---

## 🙏 Teşekkür

Cumhuriyetimizin kuruluşunun 101. yılında, Gazi Mustafa Kemal ATATÜRK'ün diliyle Türkçeyi teknolojiye armağan ediyorum. Onu ve tüm silah arkadaşlarını **sonsuz saygı, minnet ve özlemle** anıyorum.

Bu veri setinin %100 doğruluğa ulaşması için yapılan kapsamlı doğrulama çalışması, ATATÜRK'ün "Hayatta en hakiki mürşit ilimdir" sözüne bir saygı duruşudur.

---

**🇹🇷 Ne mutlu Türküm diyene!**

---

<div align="center">


**Veri Seti Metrikleri**

![Sorular](https://img.shields.io/badge/Sorular-600-blue?style=for-the-badge)
![Kategoriler](https://img.shields.io/badge/Kategoriler-41-orange?style=for-the-badge)
![Doğruluk](https://img.shields.io/badge/Doğruluk-100%25-brightgreen?style=for-the-badge)
![Lisans](https://img.shields.io/badge/Lisans-CC_BY_4.0-green?style=for-the-badge)

</div>
