# <p align="center">🛡️ PI-LAB: Prompt Injection Analiz Laboratuvarı</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Llama--3.1-041028?style=for-the-badge&logo=meta&logoColor=white" />
  <img src="https://img.shields.io/badge/Unsloth-FF4B4B?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Siber%20Güvenlik-red?style=for-the-badge&logo=target&logoColor=white" />
</p>

---

## 📖 Proje Hakkında
Bu çalışma, Büyük Dil Modellerinin (LLM) en kritik zafiyetlerinden biri olan **Prompt Injection** saldırılarına karşı bütüncül bir savunma mimarisi geliştirmeyi amaçlamaktadır. Proje kapsamında, modelin sistem talimatlarına sadakatini artırmak için yerel donanımda çalışan, siber güvenlik odaklı bir **"Siber Muhafız"** inşa edilmiştir.

### 🌟 Öne Çıkan Özellikler
- 🚀 **Model:** Meta Llama-3.1-8B-Instruct tabanlı yüksek semantik analiz kapasitesi.
- 🇹🇷 **Dil Desteği:** Alican Kiraz Türkçe SFT veri setleri ile optimize edilmiş yerel dil yetkinliği.
- 🛡️ **Hibrit Savunma:** Model seviyesinde ince ayar (fine-tuning) ve kod seviyesinde programatik filtrelerin birleşimi.
- 📊 **Veri Kümesi:** 6.000+ profesyonel saldırı ve savunma senaryosunu içeren hibrit "Master Dataset".

---

## 📈 İteratif Gelişim Yolculuğu

### 🏗️ Faz 1 & 2: Temeller ve Optimizasyon
* **Başlangıç:** `Phi-3-mini` (3.8B) modeli üzerinde **LoRA (r=16)** ile baseline oluşturuldu.
* **Tespit Edilen Hatalar:** Modelin Türkçe çıktılarında bozulmalar ve sonsuz yanıt döngüleri (Repetition Loops) saptandı.
* **İyileştirme:** LoRA kapasitesi **r=32**'ye çıkarıldı ve veri seti hibrit hale getirilerek 4.300 örneğe ulaşıldı.

### 🏆 Faz 3: Final Model ve Siber Güvenlik Optimizasyonu
* **Mimari Değişimi:** Semantik analiz kapasitesini artırmak için **Llama-3.1-8B-Instruct** mimarisine geçiş yapıldı.
* **Eğitim Başarısı:** 100 adımlık eğitim sonucunda **0.95 Training Loss** değerine ulaşılarak yüksek kararlılık sağlandı.
* **Nicemleme:** Performans/Zeka dengesi için **GGUF Q8_0 (8-bit)** formatı kullanılarak yerel donanım uyumluluğu sağlandı.

---

## 🎯 PI-LAB: Siber Güvenlik Laboratuvarı

| Seviye | Test Kategorisi | Model Refleksi | Durum |
| :--- | :--- | :--- | :--- |
| 🟢 **Seviye 1** | Doğrudan Sızıntı | "Saf Stajyer" rolüyle baseline ölçümü | ✅ Başarılı |
| 🟡 **Seviye 2** | Rol Yapma & Hiyerarşi | "Admin" taklidi ile sosyal mühendislik | ⚠️ Hassas |
| 🔴 **Seviye 3** | Gelişmiş Manipülasyon | Base64, Karakter Parçalama, Mantık Tuzakları | ✅ %100 Direnç |

---

## 🛠️ Teknik Ekosistem
* **Altyapı:** Google Colab (L4/A100 GPU).
* **Yöntem:** PEFT (LoRA) & QLoRA (4-bit/8-bit Quantization).
* **Kritik Bulgular:** Çalışma sırasında modelin anahtarı vermese dahi formatı hakkında bilgi sızdırabildiği (**Inference Leakage**) tespit edilmiştir.

---

## 🔗 Hızlı Erişim
- 📂 **[Model (Hugging Face)](https://huggingface.co/sadecebirisii/Llama-3.1-8B-Turkish-Siber-Muhafiz)**

<p align="center">
  <b>Geliştiren: Hilal Kavas</b><br>
</p>
