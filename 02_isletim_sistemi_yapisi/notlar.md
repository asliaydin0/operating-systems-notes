# İşletim Sistemi Yapısı 🧠

Bu bölümde işletim sisteminin **nasıl organize edildiği**, **nasıl çalıştığı** ve **tasarım prensipleri** ele alınacaktır.

---

## 1. İşletim Sistemi Yapısı

İşletim sistemleri karmaşık yapılardır. Bu nedenle belirli bir **yapısal model** üzerinden tasarlanır:

### a. Monolitik Yapı
- Tüm işletim sistemi **tek bir büyük çekirdek** halinde çalışır.  
- Tüm servisler çekirdek düzeyinde yer alır.  
- **Avantajı:** Hızlıdır (doğrudan iletişim).  
- **Dezavantajı:** Hata ayıklaması zordur.

> 💡 Örnek: MS-DOS, Linux çekirdeği, Unix çekirdeği.

### b. Katmanlı Yapı
- İşletim sistemi **katmanlara ayrılır** (örn. donanım, çekirdek, servisler, kullanıcı arayüzü).  
- Katmanlar yalnızca **bir alt katmanla** iletişim kurar.  
- **Avantajı:** Modülerlik, bakım kolaylığı.  
- **Dezavantajı:** Katmanlar arası geçişler performansı düşürebilir.

> 💡 Örnek: THE sistemi.

### c. Mikroçekirdek (Microkernel)
- Minimum çekirdek: sadece temel servisler (işlem iletişimi, bellek yönetimi, zamanlayıcı).  
- Diğer servisler kullanıcı modunda çalışır.  
- **Avantajı:** Daha güvenli ve esnek yapı.  
- **Dezavantajı:** Çekirdek ile kullanıcı servisleri arasında daha fazla iletişim.

> 💡 Örnek: Mach, Minix.

### d. Hibrit Çekirdek (Hybrid Kernel)

- Monolitik ve mikroçekirdek mimarilerinin birleşimidir.
- Çekirdekte temel servisler bulunur, ancak bazı servisler kullanıcı modunda çalışabilir.
- **Avantajı:** Hem performans hem de esneklik sunar.
- **Dezavantajı:** Tasarımı karmaşıktır.

### e. Modüler Sistemler
- Çekirdek, **yüklenebilir modüller** içerir.  
- Monolitik sistemin hızını, mikroçekirdeğin esnekliğiyle birleştirir.  
- Modern işletim sistemleri bu yapıyı kullanır.

> 💡 Örnek: Linux çekirdeği.

---

## 2. İşletim Sistemi İşleyişi

Bir bilgisayar açıldığında işletim sistemi **bir dizi aşamadan geçerek** devreye girer:

1. **Bootloader (Önyükleyici):**  
   - Donanım testlerini yapar (POST).  
   - İşletim sisteminin çekirdeğini RAM’e yükler.

2. **Kernel (Çekirdek) Başlatma:**  
   - Temel donanım sürücüleri yüklenir.  
   - Sistem çağrıları etkinleşir.  
   - İşlem yöneticisi devreye girer.

3. **Servislerin Başlatılması:**  
   - G/Ç yöneticisi, dosya sistemi yöneticisi, bellek yöneticisi çalışır.

4. **Kullanıcı Oturumu:**  
   - Komut satırı veya GUI üzerinden sistem kullanıma açılır.

> 🧭 Çekirdek, sistemin kalbidir. İşleyişin merkezinde CPU, bellek ve G/Ç birimleriyle sürekli etkileşim vardır.

---

## 3. İşletim Sistemi Tasarım ve Gerçekleştirimi

Bir işletim sistemi geliştirilirken şu adımlar izlenir:

- **Hedef Belirleme:** Performans, güvenlik, taşınabilirlik, kullanıcı kolaylığı.  
- **Mimari Seçimi:** Monolitik, mikroçekirdek, modüler vb.  
- **Arabirim Belirleme:** Sistem çağrıları, API, kullanıcı arayüzü.  
- **Gerçekleştirme:** C, C++ gibi dillerle çekirdek kodu yazılır.  
- **Test & Geliştirme:** Hata ayıklama ve iyileştirme.

> 📌 Tasarım ve gerçekleştirim aşaması, işletim sisteminin ne kadar **kararlı** ve **verimli** olacağını belirler.

---

## 4. Sanal Makineler

Sanal makine (VM), fiziksel bir bilgisayarın **yazılımsal bir kopyasıdır**. İşletim sistemleri bu yapıyı destekler.

- **Ana Sistem (Host):** Gerçek donanım üzerinde çalışan sistem.  
- **Konuk Sistem (Guest):** Ana sistem üzerinde sanal ortamda çalışan OS.

### Avantajları:
- Deneme / geliştirme ortamı sağlar  
- Güvenli test yapılabilir  
- Birden fazla OS aynı anda çalıştırılabilir

### Türleri:
- **Tam Sanallaştırma:** Donanım tamamen sanallaştırılır.  
- **Yarı Sanallaştırma:** Bazı donanım bileşenleri ana sistemle paylaşılır.

> 💡 Örnek: VirtualBox, VMware, Hyper-V

---

## 📌 Özet
- İşletim sistemi farklı yapılarda tasarlanabilir (monolitik, mikroçekirdek, modüler).  
- İşleyiş, önyükleyici (bootloader) → çekirdek → servisler → kullanıcı oturumu şeklindedir.  
- Tasarım süreci hedeflere ve mimariye göre şekillenir.  
- Sanal makineler, işletim sistemlerinin esnekliğini artırır.
