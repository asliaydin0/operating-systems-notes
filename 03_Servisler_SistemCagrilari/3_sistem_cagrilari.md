# ⚡ 3.3 Sistem Çağrıları (System Calls)

Uygulama programları donanım kaynaklarına **doğrudan erişemez**.  
Bunun yerine, işletim sisteminin çekirdeği ile iletişim kurmak için **sistem çağrıları** kullanılır.  
Sistem çağrıları, kullanıcı modu ile çekirdek modu arasındaki geçişi güvenli bir şekilde sağlar.

---

## 🧠 Sistem Çağrılarının Özellikleri
- Uygulama → Sistem çağrısı → Çekirdek → Donanım  
- Kontrollü ve güvenli bir erişim sağlar.  
- Her işletim sisteminde sistem çağrılarının isimleri farklı olabilir ama işlevleri benzerdir.

💡 **Örnek:** Bir dosya açmak için `open()` çağrısı yapılır, çekirdek dosya sistemine erişir.

---

## 🧰 Sistem Çağrısı Kategorileri

### a. Proses Kontrolü (Process Control)
- Program başlatma, durdurma, bekleme, sinyal gönderme.  
💡 `fork()`, `exec()`, `exit()`, `wait()`

---

### b. Dosya Yönetimi (File Management)
- Dosya oluşturma, okuma, yazma, silme, kapatma.  
💡 `open()`, `read()`, `write()`, `close()`

---

### c. Aygıt Yönetimi (Device Management)
- Cihazlara erişim, okuma/yazma, kontrol.  
💡 `ioctl()`, `read()`, `write()`

---

### d. Bilgi Bakımı (Information Maintenance)
- Sistem zamanı, kullanıcı bilgisi, dosya öznitelikleri.  
💡 `getpid()`, `getuid()`, `time()`

---

### e. İletişim (Communication)
- Süreçler arası iletişim (IPC), ağ haberleşmesi.  
💡 `pipe()`, `shmget()`, `send()`, `recv()`

---

### f. Koruma (Protection)
- Erişim hakları, yetkilendirme.  
💡 `chmod()`, `umask()`, `setuid()`

---

## 🧭 Sistem Çağrısı Süreci
1. Kullanıcı programı bir işlem başlatır.  
2. Program uygun sistem çağrısını yapar.  
3. CPU, kullanıcı modundan çekirdek moduna geçer.  
4. Çekirdek çağrıyı işler.  
5. Sonuç kullanıcı programına geri döner.

---

## 📌 Kısaca ;
- Sistem çağrıları, uygulamaların çekirdek üzerinden donanıma **güvenli** erişimini sağlar.  
- Temel kategoriler: **Proses kontrolü, dosya yönetimi, aygıt yönetimi, bilgi bakımı, iletişim, koruma**.  
- Tüm modern işletim sistemlerinde sistem çağrıları mevcuttur ancak isimleri ve uygulama biçimleri farklılık gösterebilir.
