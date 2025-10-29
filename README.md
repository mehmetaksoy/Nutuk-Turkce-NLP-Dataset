# 🇹🇷 Nutuk 1. Cilt — Türkçe Doğal Dil İşleme Veri Seti

> “Efendiler, bu nutuklarım, bir devrin hikâyesidir...”  
> — *Gazi Mustafa Kemal ATATÜRK, 1927*

---

## 📘 Hakkında

Bu çalışma, **Gazi Mustafa Kemal ATATÜRK’ün Nutuk adlı eseri**nin 1. cildinden (1–334. sayfalar) özenle işlenmiş,  
**Türkçe doğal dil işleme (NLP)**, **fine-tuning**, **embedding eğitimi**, **dil modeli değerlendirmesi** ve benzeri yapay zekâ araştırmaları için hazırlanmış **örnek veri setini** içerir.  

Amaç; bilgisayarların **Türkçeyi daha doğru, doğal ve yabancılaşmamış biçimde** öğrenmesine katkı sunmak,  
Atatürk’ün dilindeki ifade gücünü modern algoritmaların anlayabileceği biçime kazandırmaktır.  

---

## 📚 İçindekiler
- [Kaynak ve Kapsam](#kaynak-ve-kapsam)
- [Veri Dosyaları](#veri-dosyaları)
- [Amaç ve Kullanım Alanları](#amaç-ve-kullanım-alanları)
- [Ön-İşleme Süreci](#ön-i̇şleme-süreci)
- [Veri Şeması](#veri-şeması)
- [Örnek Kayıtlar](#örnek-kayıtlar)
- [Kalite ve Sınırlılıklar](#kalite-ve-sınırlılıklar)
- [Sürümleme](#sürümleme)
- [Lisans ve Hukuki Not](#lisans-ve-hukuki-not)
- [Katkı ve İletişim](#katkı-ve-iletişim)
- [Atıf](#atıf)
- [Teşekkür](#teşekkür)

---

## 📖 Kaynak ve Kapsam

- **Ana kaynak:** *Mustafa Kemal ATATÜRK – Nutuk (Orijinal Metin)*, 1927 baskısı.  
  1. cilt metni, İnternet Arşivi’nde bulunan orijinal OCR (Full Text) sürümünden alınmıştır.  
- **Kapsam:** 1–334. sayfalar arası içerik (2. cilde geçilen 335. sayfa itibarıyla durdurulmuştur).  
- **OCR bilgisi:** Tesseract 5, 300 PPI, `tur+Latin` parametreleri.  

---

## 📂 Veri Dosyaları
```
data/
├── NUTUK_1.txt                         # Temizlenmiş 1. cilt metni (1–334 sayfalar)
└── nutuk_qa_birlesik_revize_final.json # JSON formatında örnek soru-cevap listesi
```
- `NUTUK_1.txt`: Başlık, paragraf ve cümle yapısı korunarak sadeleştirilmiş metin.  
- `nutuk_qa_birlesik_revize_final.json`: Metin temelli bilgi çıkarımı ve model eğitimi için örnek soru‑cevap yapısı.  

---

## 🎯 Amaç ve Kullanım Alanları

Bu veri seti, Türkçe dilinde çalışan doğal dil işleme sistemlerinin **doğallık, anlam derinliği ve tarihsel bağlam** kapasitesini artırmak amacıyla hazırlanmıştır.  

**Kullanım Alanları:**
- Türkçe dil modellerinin **fine‑tuning** süreçleri  
- **Embedding tabanlı** semantik arama ve anlam haritalama  
- **Türkçe metin anlama**, özetleme ve bağlamsal çıkarım çalışmaları  
- **Yapay zekâ etik ve kültürel uyum** araştırmaları  
- **Tarihsel metinlerin dijital analizi** ve dil evrimi incelemeleri  

Bu veri seti, sadece teknolojik değil; **kültürel sürekliliği koruyan** bir katkı olarak tasarlanmıştır.  

---

## ⚙️ Ön‑İşleme Süreci

1. **Kaynak Seçimi:** İnternet Arşivi’ndeki OCR sürümünden metin çıkarımı yapıldı.  
2. **Temizlik:**  
   - Satır kırılımları ve paragraf düzeni onarıldı.  
   - Sayfa numaraları, dipnotlar ve kesme işaretleri temizlendi.  
   - OCR kaynaklı hatalar düzeltildi, dil birliği sağlandı.  
3. **Yapılandırma:**  
   - Metin; cümle, başlık ve paragraf düzeyinde anlam bütünlüğü korunarak düzenlendi.  
   - İsteğe bağlı olarak JSON biçiminde örnek QA eşleşmeleri oluşturuldu.  

---

## 🧩 Veri Şeması

```json
{
  "id": 1,
  "category": "bilgi",
  "question": "…",
  "answer": "…",
  "source_excerpt": "…",
  "page_range": "s.120-121",
  "annotation": "doğrulandı"
}
```

---

## 💡 Örnek Kayıtlar

- **Soru:** Erzurum Kongresi’nin toplanma amacı neydi?  
  **Yanıt:** Vatanın bütünlüğünü korumak ve milletin bağımsızlığını sağlamak; milli bir hükümet esasını kurmak.  

- **Soru:** Amasya Tamimi’nin önemi nedir?  
  **Yanıt:** Milli iradenin esas alınacağını ve bağımsızlığın milletin kararıyla korunacağını ilan etmiştir.  

---

## 🧠 Kalite ve Sınırlılıklar

- OCR kaynaklı eski imlâ farkları yer yer korunmuştur.  
- Noktalama ve cümle bütünlüğü akademik denge gözetilerek yeniden düzenlenmiştir.  

---

## 🗓️ Sürümleme
- **V.1 (29 Ekim 2025)**  

---

## ⚖️ Lisans ve Hukuki Not

- **Metin:** Nutuk (1927) — ATATÜRK ’ün vefatından 70 yıl geçtiği için **kamu malıdır**.  
- **Veri:** CC BY 4.0  
- **Kod:** MIT  
---

## 🤝 Katkı ve İletişim

Pull Request ve Issue’lara açıktır.  
Yeni eklemeler, düzeltmeler veya Türkçe NLP projeleriyle entegrasyon önerileri memnuniyetle karşılanır.

---

## 📜 Atıf

> **Nutuk 1. Cilt — Türkçe Doğal Dil İşleme Veri Seti (v1.0)**, 29 Ekim 2025.  
> Kaynak metin ve örnek veri yapısı; GitHub deposu.

---

## Teşekkür

Cumhuriyetimizin **102. yılında**,  
**Gazi Mustafa Kemal ATATÜRK ’ün diliyle Türkçeyi teknolojiye armağan ediyorum.**  
Onu ve tüm silah arkadaşlarını sonsuz saygı, minnet ve özlemle anıyorum.  
