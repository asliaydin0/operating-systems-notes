# 🧭 İşlem Yönetimi (Process Management)

## 📌 Temel Kavramlar
- **İşlem (Process):** Çalışmakta olan bir programın bellekteki halidir.  
- **Program ≠ İşlem:** Program pasif bir varlıkken işlem aktif bir yürütme birimidir.

## ⚙️ İşlem Durumları
- **Yeni (New)** → oluşturuluyor  
- **Hazır (Ready)** → yürütülmeyi bekliyor  
- **Çalışıyor (Running)** → CPU tarafından yürütülüyor  
- **Bekliyor (Waiting)** → G/Ç veya olay bekliyor  
- **Sonlandı (Terminated)** → işlem tamamlandı

## 🧠 İşlem Kontrol Bloğu (PCB)
- İşlem kimliği (PID)  
- Program sayacı  
- CPU kayıtları  
- Bellek bilgisi  
- Durum bilgisi

## 🔄 Zamanlayıcı (Scheduler)
- İşlemler arasında CPU zamanını paylaştırır.  
- Türleri:
  - Uzun vadeli (long-term)
  - Kısa vadeli (short-term)
  - Orta vadeli (medium-term)

## 🤝 İşlem İletişimi (IPC)
- İşlemler arasında veri alışverişi sağlar.  
- Yöntemler:
  - Paylaşılan bellek
  - Mesaj geçirme

---

✅ **Özet:**  
İşlem yönetimi, işletim sisteminin CPU kaynaklarını adil ve verimli kullanmasını sağlar. İşlemler durum değiştirerek yürütülür ve zamanlayıcı bu süreci kontrol eder.

