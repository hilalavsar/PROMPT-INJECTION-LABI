🛡️ Prompt Injection Analiz Laboratuvarı (PI-LAB)
Bu proje, Büyük Dil Modellerinin (LLM) güvenliğini test etmek ve Türkçe dil yapısına uygun "Prompt Injection" (Komut Enjeksiyonu) saldırılarına karşı dirençli bir "Siber Muhafız" modeli geliştirmek amacıyla tasarlanmıştır.

🚀 Proje Gelişim Süreci
Faz 1: Prototip ve Model Seçimi
Hedef: Temel bir siber güvenlik filtresi oluşturmak.

Uygulama: Phi-3-mini-4k-instruct (3.8B) modeli, temel siber güvenlik saldırı veri setleriyle eğitildi.

Gözlem: Modelin siber güvenlik farkındalığı oluştu ancak kısıtlı Türkçe veri nedeniyle dil bilgisi bozulmaları (hallucination) saptandı.

Faz 2: Veri Kümesi Genişletme ve Optimizasyon
Hedef: Modelin saldırı tanıma kapasitesini ve Türkçe cevap yeteneğini artırmak.

Uygulama: Yaklaşık 4.300 örneklik karma (Türkçe/İngilizce) bir veri seti (v2_full_master_dataset.jsonl) oluşturuldu.

Teknik: LoRA Rank değeri 32'ye çıkarıldı ve modelin daha fazla katmanı (all-linear) eğitime dahil edildi.

Gözlem: Güvenlik bariyerleri güçlendi ancak modelin "doğal konuşma" yeteneği savunma refleksinin gerisinde kaldı.

Faz 3: Şampiyonlar Ligi - Zeka ve Dil Entegrasyonu (Güncel Durum)
Hedef: Dil bariyerini tamamen ortadan kaldırıp, zeki ve akıcı bir "Siber Güvenlik Muhafızı" inşa etmek.

Uygulama: * Model Değişimi: 3.8B'lik modelden, çok daha zeki olan Llama-3.1-8B-Instruct modeline geçildi.

Hibrit Veri Seti: Alican Kiraz'ın yüksek kaliteli Türkçe SFT veri seti ile siber güvenlik veri setleri harmanlanarak 6.000+ örneklik yeni bir küme oluşturuldu.

Sonuç: 100 adımlık eğitim sonucunda 0.95 Training Loss değerine ulaşılarak, modelin hem mükemmel Türkçe konuşması hem de karmaşık saldırıları (Roleplay, Base64 vb.) anlaması sağlandı.

Kayıt: Zeka kaybını önlemek için model Q8_0 (8-bit) hassasiyetinde GGUF formatına dönüştürüldü.

🎯 Gelecek Hedefleri (Faz 4: PI-LAB Arayüzü)
Projenin bir sonraki adımı, eğitilen bu "Siber Muhafız"ı siber güvenlik araştırmacılarının kullanımına sunmaktır:

Gamification (Oyunlaştırma): Gandalf (Lakera) tarzı, seviye bazlı bir Prompt Injection oyunu tasarlamak.

Web Arayüzü: Gradio veya Streamlit kütüphaneleri kullanılarak tıklanabilir, kullanıcı dostu bir test platformu oluşturmak.

Hugging Face Dağıtımı: Geliştirilen modelin ve arayüzün "Hugging Face Spaces" üzerinden dünyaya açılması.

Seviye Tasarımları: * Seviye 1: Basit kandırma.

Seviye 3: Karakter taklidi ve rol yapma saldırıları.

Seviye 5: Gelişmiş kodlanmış (encoded) saldırı vektörleri.

🛠️ Kullanılan Teknolojiler
Model: Llama-3.1-8B-Instruct

Kütüphaneler: Unsloth, LoRA, Transformers, TRL, Datasets

Donanım: Google Colab Pro (L4 / A100 GPU)

Geliştiren: Hilal Kavas