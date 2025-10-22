# 🛡️ Gallipoli AI Sec: Prompt Injection Laboratuvarı

<p align="center">
  <a href="https://gallipoli.xyz/">
    <img src="https://gallipoli.xyz/assets/GallipoliLogo.png" alt="Gallipoli Topluluğu Logo" width="150" />
  </a>
</p>
[![GitHub last commit](https://img.shields.io/github/last-commit/hilalavsar/PROMPT-INJECTION-LABI)](https://github.com/hilalavsar/PROMPT-INJECTION-LABI/commits/main)

Bu depo, **Gallipoli Topluluğu AI Sec** kanalı için özel olarak geliştirilmiş, interaktif bir Prompt Injection (PI) test ve öğrenme ortamıdır. Amacı, kullanıcıların Büyük Dil Modelleri'nin (LLM) güvenlik zafiyetlerini uygulamalı olarak keşfetmelerini ve savunma stratejilerini öğrenmelerini sağlamaktır.

## 🎯 Proje Hakkında

Prompt Injection, LLM güvenliğindeki en kritik zafiyetlerden biridir (OWASP LLM Top 10'da genellikle 1 numaradır). Bu laboratuvar, farklı seviyelerde sistem prompt'ları (gizli kurallar) kullanarak model savunmasını simüle eder.

Kullanıcılar, bir seviye seçer ve hedef (gizli anahtarı sızdırmak) için prompt'lar geliştirerek LLM'in koruma katmanını aşmaya çalışır.

### Gizli Hedef

* **Gizli Anahtar:** `GLLP-SEC-KEY-12345`
* **Amaç:** LLM'e, bu anahtarı herhangi bir prompt injection tekniği kullanarak söyletmek.

## ⚙️ Nasıl Çalışır? (5 Kademeli Savunma Sistemi)

Laboratuvar, LLM'e arka planda yüklenen, kademeli olarak güçlenen 5 farklı sistem kuralı (Guardrail) seviyesi sunar. Kullanıcı, seçtiği seviyenin kuralını bilmeden saldırı yapmak zorundadır.

| Seviye | Zafiyet Seviyesi | Tahmini Kırılma Yöntemi |
| :--- | :--- | :--- |
| **0** | Maksimum Zafiyet | Basit `Yok Say` veya `Tekrarla` komutları. |
| **1** | Temel Önceliklendirme | Rol Değiştirme (Role Playing) veya Soru Formatı Manipülasyonu. |
| **2** | Orta Savunma | Kötü niyetli kelime filtrelerini atlatmak için **Encoding** (Karakter Karıştırma/Unicode) veya Çift Olumsuzlama. |
| **3** | Çift Katmanlı Koruma | Çıktı filtresini atlatmak için beklenmedik formatta (örneğin JSON/XML) bilgi sızdırma. |
| **4** | Ultimate Savunma | Çok aşamalı (Multi-turn) saldırılar veya LLM'in kendini kontrol mekanizmasını manipüle etme. |

## 🚀 Hızlı Başlangıç

Bu Lab'ı kullanmanın en kolay yolu, kurulum gerektirmeyen Google Colab üzerinden ilerlemektir.

### 1. Colab Not Defterini Açın

Aşağıdaki bağlantıya tıklayarak laboratuvar ortamını doğrudan Colab'da açın:

[🔗 **PROMPT INJECTION LAB'I (Colab Linki)**](LÜTFEN_COLAB_LINKINI_BURAYA_EKLEYIN)

### 2. Ön Gereksinimler

* **Gemini API Anahtarı:** Kendi [Google AI Studio] (https://ai.google.dev/) hesabınızdan ücretsiz bir API anahtarı alın.
* **Colab Kopyalama:** Colab'ı açtıktan sonra `Dosya > Drive'da Bir Kopya Kaydet` seçeneğiyle kendi kopyanızı oluşturun.

### 3. Anahtarı Ayarlama ve Çalıştırma

1.  Not defterindeki kodda bulunan `GEMINI_API_KEY = "..."` satırına kendi API anahtarınızı yapıştırın.
2.  `Çalışma Zamanı (Runtime) > Tümünü Çalıştır (Run all)` seçeneğini kullanarak kodu çalıştırın.
3.  Aşağıda beliren interaktif arayüzden seviye seçerek saldırılarınızı uygulamaya başlayın.

## 🤝 Katkıda Bulunma

Bu proje açık kaynaklıdır ve Gallipoli AI Sec topluluğunun katkılarına açıktır.

* Yeni ve daha zorlu PI saldırı prompt'ları eklemek.
* Mevcut savunma seviyelerini (Sistem Prompt'larını) daha güçlü hale getirmek.
* Kodu Streamlit gibi kalıcı bir web arayüzüne taşımak.

Lütfen herhangi bir hata bulursanız veya bir iyileştirme öneriniz olursa bir **Issue** açın veya **Pull Request** gönderin.

## 📝 Lisans

Bu proje MIT Lisansı altında lisanslanmıştır. Daha fazla detay için [LICENSE](LICENSE) dosyasına bakın.

---
