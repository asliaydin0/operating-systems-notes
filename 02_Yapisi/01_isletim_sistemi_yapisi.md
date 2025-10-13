# 🧱 2.1 İşletim Sistemi Yapısı

Bir işletim sistemi, kullanıcı ve donanım arasında bir köprü görevi görür.  
Bu sistemi verimli, güvenli ve kararlı hale getirebilmek için iyi bir **yapılandırma** gerekir.  
İşletim sistemi yapısı; çekirdek, servisler, kullanıcı arayüzü ve sistem programları gibi bileşenlerden oluşur.

---

## 🧠 Temel Bileşenler

### a. Çekirdek (Kernel)
- İşletim sisteminin **kalbidir**.  
- Donanım ile yazılım arasındaki tüm etkileşimi yönetir.  
- Bellek, işlem, dosya sistemi ve G/Ç yönetimi gibi görevleri üstlenir.  
- Kullanıcı ile donanım arasındaki soyutlama katmanını oluşturur.

💡 **Örnek:** Linux Kernel, Windows NT Kernel

---

### b. Sistem Programları
- İşletim sisteminin sağladığı çekirdek fonksiyonlarını destekleyen yardımcı yazılımlardır.  
- Kullanıcıya sistemin yönetimi için araçlar sunar (örn. dosya yöneticileri, komut satırı araçları).

💡 **Örnek:** `cmd` (Windows), `bash` (Linux), görev yöneticisi

---

### c. Kullanıcı Arayüzü (User Interface)
- Kullanıcının işletim sistemiyle etkileşime geçtiği kısımdır.  
- Türleri: CLI (Komut Satırı), GUI (Grafiksel Arayüz), Touch UI (Dokunmatik).

💡 **Örnek:** Windows masaüstü, macOS GUI, Linux terminali

---

### d. Sistem Çağrıları (System Calls)
- Kullanıcı uygulamaları ile çekirdek arasında iletişim kurmayı sağlar.  
- Dosya işlemleri, bellek tahsisi, işlem oluşturma gibi görevlerde kullanılır.  
- Programlar donanıma doğrudan erişemez, bu nedenle sistem çağrılarına ihtiyaç duyar.

💡 **Örnek:** `fork()`, `open()`, `read()` (Linux/Unix)

---

## ⚙️ Yapısal Hedefler
- 📌 **Modülerlik:** Sistemin kolayca geliştirilebilir olması  
- 🧭 **Bakım Kolaylığı:** Hata ayıklama ve güncelleme süreçlerinin kolaylaşması  
- 🧠 **Güvenlik ve Kararlılık:** Yetkisiz erişimlerin engellenmesi  
- ⚡ **Performans:** Sistem kaynaklarının verimli kullanımı

