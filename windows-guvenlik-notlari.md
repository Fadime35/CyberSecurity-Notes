#  Windows İşletim Sistemi

Windows, Microsoft tarafından geliştirilen grafiksel kullanıcı arayüzüne sahip bir işletim sistemidir. Masaüstü bilgisayarlarda en yaygın kullanılan sistemlerden biridir.

---

## Temel Güvenlik Özellikleri

### Windows Defender  
Windows'un yerleşik antivirüs ve kötü amaçlı yazılım koruma aracıdır.  
- Gerçek zamanlı tarama yapar.  
- İnternette indirilen dosyaları analiz eder.  
- Zararlı yazılımları otomatik karantinaya alır.  



### Windows Güvenlik Duvarı (Firewall)  

Windows Güvenlik Duvarı, cihaza gelen ve giden ağ trafiğini kontrol ederek zararlı bağlantılara karşı koruma sağlar. Hem ev kullanıcıları hem de kurumsal sistemler için önemli bir savunma katmanıdır.

#### Ne İşe Yarar?
- Bilgisayara **dışarıdan gelen** izinsiz bağlantıları engeller.
- Bilgisayardan **dışarıya giden** şüpheli trafikleri kontrol eder.
- Uygulama bazlı izinler verilebilir. Örneğin, yalnızca belirli uygulamaların internete çıkmasına izin verilir.
- GUI ile yönetim: `wf.msc`  
- Komut satırı(CLI-Command Line Interface) ile yönetim: `netsh advfirewall` 

**Not:**  Güvenlik duvarı, dış saldırıları engellemek için ilk savunma hattıdır.

---

### UAC – Kullanıcı Hesabı Denetimi  
Sistem üzerinde değişiklik yapılmadan önce kullanıcıdan onay isteyen güvenlik özelliğidir.  

**Not:**  Yüksek izin gerektiren işlemlerde ekran kararıp “izin ver” sorusu çıkar.

---

### BitLocker  
Sabit diskin tamamını şifreleyen güvenlik aracıdır.  
- TPM (Trusted Platform Module) destekliyse daha güvenlidir.  

**Not:** Fiziksel olarak disk ele geçirilse bile veriler okunamaz.


---

## Sık Kullanılan Güvenlik Komutları

| Komut              | Açıklama |
|--------------------|----------|
| `tasklist`         | Çalışan işlemleri listeler. |
| `netstat -ano`     | Açık portları ve PID'leri (işlem kimliği) gösterir.  |
| `whoami`           | Hangi kullanıcı tarafından oturum açıldığını gösterir.  |
| `eventvwr.msc`     | Olay Günlüğü Görüntüleyicisini açar.  |

**Not:** Bu komutlar, temel sistem gözlemi ve analizleri için kullanılır.

---

## Faydalı Güvenlik Araçları

- **Process Explorer**: Gelişmiş görev yöneticisidir. Her işlemin detayını gösterir.  
- **Autoruns**: Windows açılışında hangi uygulamaların otomatik çalıştığını gösterir.  
- **Wireshark**: Ağ trafiğini gerçek zamanlı analiz eder.  
- **Event Viewer**: Sistem loglarını (günlüklerini) görüntüler.  

 **Not:** Bu araçların çoğu, siber güvenlik analistleri tarafından aktif olarak kullanılır.

---

## Neden SOC Analyst için Önemlidir?

Windows sistemler hem bireysel hem de kurumsal ortamlarda en yaygın kullanılan işletim sistemleridir. Bu nedenle siber saldırganlar genellikle Windows sistemleri hedef alır.
SOC (Security Operations Center) analistleri, olay müdahalesi sırasında genellikle Windows sistem günlüklerini (Event Viewer, firewall logları vb.) analiz eder.
Tehdit tespiti, kötü amaçlı yazılım analizi ve sistem güvenliği değerlendirmesi gibi görevlerde Windows'un güvenlik araçlarını kullanma bilgisi kritik önemdedir.

Örneğin; şüpheli bir portun açık olup olmadığını netstat, oturumu açan kullanıcıyı whoami, veya sistem olaylarını eventvwr.msc ile hızlıca tespit edebilirler.

Bu nedenle, SOC analyst’lerin  Windows işletim sistemindeki temel güvenlik unsurlarını iyi bilmesi kritik önem taşır.

---


