# 🇹🇷 Nutuk 1. Cilt — Türkçe Doğal Dil İşleme Veri Seti

> “Efendiler, bu nutuklarım, bir devrin hikâyesidir...”  
> — Gazi Mustafa Kemal ATATÜRK, 1927

**Depo:** https://github.com/mehmetaksoy/Nutuk-Turkce-NLP-Dataset

---

## İçindekiler

- [📘 Hakkında](#-hakkında)
- [📖 Kaynak ve Kapsam](#-kaynak-ve-kapsam)
- [📂 Veri Dosyaları](#-veri-dosyaları)
- [🎯 Amaç ve Kullanım Alanları](#-amaç-ve-kullanım-alanları)
- [⚙️ Ön‑İşleme Süreci](#️-ön-işleme-süreci)
- [🧩 Veri Şeması](#-veri-şeması)
- [💡 Örnek Kayıtlar](#-örnek-kayıtlar)
- [🧠 Kalite ve Sınırlılıklar](#-kalite-ve-sınırlılıklar)
- [🗓️ Sürümleme](#️-sürümleme)
- [⚖️ Lisans ve Hukuki Not](#-lisans-ve-hukuki-not)
- [🤝 Katkı ve İletişim](#-katkı-ve-iletişim)
- [📜 Atıf](#-atıf)
- [🙏 Teşekkür](#-teşekkür)

---

## 📘 Hakkında

Bu çalışma, Gazi Mustafa Kemal ATATÜRK’ün **Nutuk** adlı eserinin **1. cildinden (1–334. sayfalar)** özenle işlenmiş, Türkçe doğal dil işleme (NLP), fine‑tuning, embedding eğitimi, dil modeli değerlendirmesi ve benzeri yapay zekâ araştırmaları için hazırlanmış **örnek veri setini** içerir.  
Amaç; bilgisayarların **Türkçeyi daha doğru, doğal ve yabancılaşmamış biçimde** öğrenmesine katkı sunmak, ATATÜRK ’ün dilindeki ifade gücünü modern algoritmaların anlayabileceği biçime kazandırmaktır.

---

## 📖 Kaynak ve Kapsam

- **Ana kaynak:** *Mustafa Kemal ATATÜRK – Nutuk (Orijinal Metin), 1927 baskısı.*  
- **Metin kaynağı:** İnternet Arşivi’nde bulunan orijinal **OCR (Full Text)** sürümünden alınmıştır.  
- **Kapsam:** **1–334. sayfalar** arası içerik (2. cilde geçilen 335. sayfa itibarıyla durdurulmuştur).  
- **OCR bilgisi:** *Tesseract 5, 300 PPI, tur+Latin parametreleri.*

> Not: OCR metni yer yer tarihsel imlâyı yansıtır; temizlik ve düzenleme adımlarında dil birliği gözetilmiştir.

---

## 📂 Veri Dosyaları

```
data/
├── NUTUK_1.txt                      # Temizlenmiş 1. cilt metni (1–334. sayfalar)
└── nutuk_qa_birlesik_revize_final.json  # JSON formatında örnek soru-cevap listesi
```

- **NUTUK_1.txt:** Başlık, paragraf ve cümle yapısı korunarak sadeleştirilmiş metin.  
- **nutuk_qa_birlesik_revize_final.json:** Metin temelli bilgi çıkarımı ve model eğitimi için örnek **soru‑cevap** yapısı. (AI)

---

## 🎯 Amaç ve Kullanım Alanları

Bu veri seti, Türkçe dilinde çalışan doğal dil işleme sistemlerinin **doğallık, anlam derinliği ve tarihsel bağlam** kapasitesini artırmak amacıyla hazırlanmıştır.

**Kullanım alanları:**

- Türkçe dil modellerinin **fine‑tuning** süreçleri  
- **Embedding** tabanlı semantik arama ve anlam haritalama  
- Türkçe **metin anlama**, **özetleme** ve **bağlamsal çıkarım** çalışmaları  
- Yapay zekâ **etik ve kültürel uyum** araştırmaları  
- **Tarihsel metinlerin dijital analizi** ve **dil evrimi** incelemeleri  

> Bu veri seti, sadece teknolojik değil; **kültürel sürekliliği** koruyan bir katkı olarak tasarlanmıştır.

---

## ⚙️ Ön‑İşleme Süreci

**Kaynak Seçimi:** İnternet Arşivi’ndeki OCR sürümünden metin çıkarımı yapıldı.  

**Temizlik:**  

- Satır kırılımları ve paragraf düzeni onarıldı.  
- Sayfa numaraları, dipnotlar ve kesme işaretleri temizlendi.  
- OCR kaynaklı hatalar düzeltildi, dil birliği sağlandı.  

**Yapılandırma:**  

- Metin; cümle, başlık ve paragraf düzeyinde anlam bütünlüğü korunarak düzenlendi.  
- İsteğe bağlı olarak **JSON biçiminde** örnek QA eşleşmeleri oluşturuldu.

> Reprodüksiyon için öneri: Ön‑işleme adımlarını ayrı bir betikte toplayıp *commit hash* ile sürümleyin.

---

## 🧩 Veri Şeması

Aşağıdaki şema, **örnek QA** dosyasındaki kayıt yapısını gösterir:

```jsonc
{
  "id": 1,
  "category": "bilgi",               // ["bilgi","neden-sonuç","amaç","yorum","özet"]
  "question": "…",
  "answer": "…",
  "source_excerpt": "…",
  "page_range": "s.120-121",
  "annotation": "doğrulandı"         // ["doğrulandı","revize edildi","belirsiz"]
}
```

---

## 💡 Örnek Kayıtlar

- **Soru:** Erzurum Kongresi’nin toplanma amacı neydi?  
  **Yanıt:** Vatanın bütünlüğünü korumak ve milletin bağımsızlığını sağlamak; millî bir hükümet esasını kurmak.
- **Soru:** Amasya Tamimi’nin önemi nedir?  
  **Yanıt:** Millî iradenin esas alınacağını ve bağımsızlığın milletin kararıyla korunacağını ilan etmiştir.

> Not: Örnekler, 1. cilt metnindeki tarihsel bağlamdan türetilmiş **temsilî** kayıtlardır.

---

## 🧠 Kalite ve Sınırlılıklar

- OCR kaynaklı **eski imlâ** farkları yer yer korunmuştur.  
- **Noktalama** ve **cümle bütünlüğü** akademik denge gözetilerek yeniden düzenlenmiştir.  
- QA örnekleri **navigasyonel** (ör. “burada/şurada”) değil; **Büyük Dil modelleri ile içerik odaklı** hazırlanmıştır.

---

## 🗓️ Sürümleme

- **v1.0 — 29 Ekim 2025**: İlk kamu yayımlaması (1–334. sayfalar, örnek QA).

---

## ⚖️ Lisans ve Hukuki Not

- **Metin:** *Nutuk (1927)* — Türkiye’de, müellifin vefatından 70 yıl geçtiği için **kamu malıdır. (public domain)**.  
- **Veri (JSON/işlenmiş çıktılar):** **CC BY 4.0**  
- **Kod/Betikler (varsa):** **MIT**

---

## 🤝 Katkı ve İletişim

**Pull Request** ve **Issue**’lara açıktır. Yeni eklemeler, düzeltmeler veya Türkçe NLP projeleriyle entegrasyon önerileri memnuniyetle karşılanır.  

- Depo: https://github.com/mehmetaksoy/Nutuk-Turkce-NLP-Dataset

---

## 📜 Atıf

Bu veri setini akademik/teknik çalışmalarda kullanırken lütfen aşağıdaki atıflardan birini yapınız.

**Türkçe (önerilen):**  

> Mehmet Aksoy, *Nutuk 1. Cilt — Türkçe Doğal Dil İşleme Veri Seti* (sürüm v1.0), GitHub deposu, 29 Ekim 2025. Erişim: https://github.com/mehmetaksoy/Nutuk-Turkce-NLP-Dataset

**IEEE stilinde örnek:**  

> [1] M. Aksoy, “Nutuk 1. Cilt — Türkçe Doğal Dil İşleme Veri Seti (v1.0),” GitHub repository, Oct. 29, 2025. [Online]. Available: https://github.com/mehmetaksoy/Nutuk-Turkce-NLP-Dataset

**APA stilinde örnek:**  

> Aksoy, M. (2025). *Nutuk 1. Cilt — Türkçe Doğal Dil İşleme Veri Seti* (v1.0) [GitHub repository]. https://github.com/mehmetaksoy/Nutuk-Turkce-NLP-Dataset

**BibTeX:**

```bibtex
@misc{nutuk_tr_nlp_v1_2025,
  title        = {Nutuk 1. Cilt --- Türkçe Doğal Dil İşleme Veri Seti},
  author       = {Aksoy, Mehmet},
  year         = {2025},
  howpublished = {\url{https://github.com/mehmetaksoy/Nutuk-Turkce-NLP-Dataset}},
  note         = {Sürüm v1.0, GitHub repository},
}
```

---

## 🙏 Teşekkür

Cumhuriyetimizin 102. yılında, Gazi Mustafa Kemal ATATÜRK ’ün diliyle Türkçeyi teknolojiye armağan ediyorum. Onu ve tüm silah arkadaşlarını **sonsuz saygı, minnet ve özlemle** anıyorum.
