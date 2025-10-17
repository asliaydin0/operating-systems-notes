# 🧠 2.2 Çekirdek Yapıları

Çekirdek (Kernel), bir işletim sisteminin **en temel ve kritik** bileşenidir.  
Sistem kaynaklarını yönetir, kullanıcı uygulamalarıyla donanım arasında aracı görevi görür.  
Farklı işletim sistemlerinde çekirdek tasarımı farklılık gösterebilir.  
Bu bölümde çekirdek yapılarının türlerini inceleyeceğiz.

---

## a. Monolitik Yapı
- Tüm işletim sistemi tek bir **büyük çekirdek** halinde çalışır.  
- Tüm servisler çekirdek düzeyinde yer alır.  
- Doğrudan iletişim sayesinde hızlıdır.

**Avantajları:**  
- Yüksek performans  
- Servisler arasında hızlı iletişim

**Dezavantajları:**  
- Hata ayıklaması zordur.  
- Bir hatada tüm sistem çökebilir.

💡 **Örnek:** MS-DOS, Linux çekirdeği, Unix çekirdeği

---

## b. Katmanlı Yapı
- İşletim sistemi **katmanlara ayrılır** (örn. donanım, çekirdek, servisler, kullanıcı arayüzü).  
- Her katman yalnızca bir alt katmanla iletişim kurar.  
- Modüler bir yapı sunar.

**Avantajları:**  
- Bakım ve hata ayıklama kolaylığı  
- Yapılandırılmış bir mimari

**Dezavantajları:**  
- Katmanlar arası geçiş performansı düşürebilir.

💡 **Örnek:** THE sistemi

---

## c. Mikroçekirdek (Microkernel)
- Sadece **temel servisler** çekirdek içinde yer alır.  
- Diğer servisler kullanıcı modunda çalışır.  
- Güvenlik ve esneklik ön plandadır.

**Avantajları:**  
- Daha güvenli ve esnek  
- Hata durumunda sistemin çökmesi daha zor

**Dezavantajları:**  
- Kullanıcı ve çekirdek arasında daha fazla iletişim → performans düşebilir.

💡 **Örnek:** Mach, Minix

---

## d. Modüler Sistemler
- Çekirdek, **yüklenebilir modüller** içerir.  
- Monolitik yapının hızını, mikroçekirdeğin esnekliğiyle birleştirir.  
- Modern işletim sistemlerinde yaygın olarak kullanılır.

**Avantajları:**  
- Yüksek performans + esneklik  
- Sadece ihtiyaç duyulan modüller yüklenir.

**Dezavantajları:**  
- Yönetim karmaşık olabilir.

💡 **Örnek:** Linux çekirdeği

---

## e. Hibrit Çekirdek (Hybrid Kernel)
- Mikroçekirdek ve monolitik çekirdek yapılarını birleştirir.  
- Çekirdeğin bazı kısımları monolitik, bazıları kullanıcı modundadır.  
- Performans ve güvenlik arasında denge sağlar.

**Avantajları:**  
- Yüksek performans + esneklik  
- Sistem çökmesine karşı daha dayanıklı

**Dezavantajları:**  
- Tasarımı karmaşıktır.  
- Geliştirmesi zaman alabilir.

💡 **Örnek:** Windows NT, macOS XNU
