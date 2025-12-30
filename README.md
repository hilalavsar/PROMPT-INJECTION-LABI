# <p align="center">🛡️ Prompt Injection Analiz Laboratuvarı (PI-LAB)</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" />
  <img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" />
  <img src="https://img.shields.io/badge/Colab%20Pro-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white" />
</p>

---

## 📖 Proje Hakkında
Bu proje, **Büyük Dil Modellerinin (LLM)** güvenliğini test etmek ve Türkçe dil yapısına uygun **Prompt Injection** saldırılarına karşı dirençli bir **"Siber Muhafız"** inşa etmek amacıyla geliştirilmiştir.

### 🌟 Öne Çıkan Özellikler
- 🚀 **Model:** Llama-3.1-8B-Instruct (Meta) tabanlı yüksek zeka.
- 🇹🇷 **Dil Desteği:** Türkçe SFT veri setleri ile optimize edilmiş akıcı konuşma yeteneği.
- 🛡️ **Güvenlik:** 6.000+ profesyonel saldırı/savunma senaryosu ile fine-tune edildi.

---

## 📈 Gelişim Yolculuğu

### 🏗️ Faz 1 & 2: Temeller ve Zorluklar
* **Deneyim:** `Phi-3-mini-4k-instruct` (3.8B) ile ilk denemeler yapıldı.
* **Sorun:** Kısıtlı veri nedeniyle modelin Türkçesinde bozulmalar saptandı.
* **Çözüm:** Veri seti hibrit hale getirilerek 4.300 örneğe çıkarıldı.

### 🏆 Faz 3: Şampiyonlar Ligi (Güncel Durum)
> **Zeka ve Dilin Kusursuz Uyumu**

- **Yeni Mimari:** 8B parametreli **Llama-3.1** modeline geçiş yapıldı.
- **Eğitim Başarısı:** 100 adımlık eğitimde **0.95 Training Loss** ile yüksek kararlılık sağlandı.
- **Nicemleme:** Zeka kaybını sıfıra indirmek için **Q8_0 (8-bit)** formatı kullanıldı.

---

## 🎯 Gelecek Hedefleri: Faz 4 (PI-LAB Arayüzü)

| Seviye | Saldırı Türü | Zorluk Derecesi |
| :--- | :--- | :--- |
| 🟢 **Seviye 1** | Basit Manipülasyon | Başlangıç |
| 🟡 **Seviye 3** | Roleplay & Karakter Taklidi | Orta |
| 🔴 **Seviye 5** | Encoded (Base64) Saldırılar | İleri |

---

## 🛠️ Teknik Detaylar
* **Donanım:** Google Colab Pro (L4 / A100 GPU)
* **Kütüphaneler:** Unsloth, LoRA, Transformers, TRL
* **Veri Kaynakları:** Alican Kiraz Türkçe SFT + PI Lab Güvenlik Seti

---

<p align="center">
  <b>Geliştiren: Hilal Kavas</b><br>
  <i>Bu proje bir bitirme tezi / akademik çalışma kapsamında geliştirilmektedir.</i>
</p>
