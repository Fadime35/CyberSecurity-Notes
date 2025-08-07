1. SOC Analyst nedir ve temel görevleri nelerdir?
   
- SOC Analyst, bir organizasyonun bilgi güvenliğini izleyen, tehditleri tespit eden, analiz eden ve müdahale eden kişidir. Temel görevleri; güvenlik olaylarını izlemek, analiz etmek, raporlamak ve gerektiğinde olay müdahalesi yapmak, ayrıca güvenlik ihlallerini önlemek için proaktif çalışmalardır.
---
2. SIEM nedir? SOC içinde neden önemlidir?
   
- SIEM (Security Information and Event Management), farklı kaynaklardan gelen log ve olayları toplayan, analiz eden ve korele eden bir güvenlik aracıdır. SOC içinde tehditlerin hızlı tespiti ve müdahalesi için kritik öneme sahiptir.
---
3. Firewall nedir? Temel çalışma prensibi nedir?
   
- Firewall, ağ trafiğini belirli kurallara göre filtreleyen ve yetkisiz erişimleri engelleyen güvenlik cihazıdır. İç ağ ile dış ağ arasında bir bariyer görevi görür.
---
4. Intrusion Detection System (IDS) ve Intrusion Prevention System (IPS) arasındaki fark nedir?

- IDS, ağda veya sistemde şüpheli aktiviteleri tespit eder ve uyarı verir; ancak müdahale etmez. IPS ise tespit ettiği tehditleri aktif olarak engeller ve müdahale eder.
---
5. Log nedir ve SOC'da neden önemlidir?

- Log, sistem, uygulama veya cihazların kaydettiği olay kayıtlarıdır. SOC'da saldırıların tespiti, analiz edilmesi ve adli inceleme için vazgeçilmezdir.
---
6. Phishing saldırısı nedir? Nasıl önlenir?

- Phishing, kullanıcıları kandırarak hassas bilgilerini ele geçirme yöntemidir. Önleme için eğitim, e-posta filtreleme ve çok faktörlü kimlik doğrulama kullanılır.
---
7. TCP ve UDP protokolleri arasındaki temel farklar nelerdir?

- TCP bağlantı odaklı, güvenilir veri iletimi sağlar; UDP ise bağlantısızdır, hızlıdır ancak veri kaybı olabilir. SOC analistleri protokol türlerine göre ağ trafiğini inceler.
---
8. Bir siber güvenlik olayı tespit ettiğinizde ilk adımınız ne olur?

- Öncelikle olayı doğrular, etkisini değerlendirir ve izole ederim. Ardından ilgili ekiplere bilgi verip müdahale sürecini başlatırım.
---
9. MITRE ATT&CK framework nedir?

- MITRE ATT&CK, siber saldırı tekniklerini ve saldırgan taktiklerini sınıflandıran kapsamlı bir bilgi tabanıdır. SOC'da saldırı tespiti ve savunma stratejileri geliştirmek için kullanılır.
---
10. SOC'da kullandığınız temel güvenlik araçları nelerdir?

- SIEM, firewall, IDS/IPS, antivirüs, endpoint detection and response (EDR) gibi araçlar günlük işlerimde temel destek sağlar.
---
11. Bir kullanıcı bilgisayarının yavaşladığını ve garip davranışlar sergilediğini bildiriyor. Ne yaparsınız?

Öncelikle cihazı izole ederim. Ardından logları ve süreçleri analiz ederek kötü amaçlı yazılım ya da yetkisiz erişim olup olmadığını araştırırım. Gerekirse EDR araçlarıyla detaylı inceleme yapar ve raporlarım.
---
12. SOC seviyeleri nelerdir? (Tier 1, Tier 2, Tier 3)

Tier 1 (L1): Alarm izleme, temel analiz ve olay yönlendirme

Tier 2 (L2): Derinlemesine analiz, olay doğrulama ve müdahale

Tier 3 (L3): Tehdit avcılığı, zafiyet analizi, gelişmiş olay inceleme
---
13. DNS Spoofing nedir?

DNS spoofing, kullanıcıları sahte bir web sitesine yönlendirerek veri çalmayı amaçlayan bir saldırıdır. Genellikle sahte DNS kayıtlarıyla gerçekleştirilir.
---
14. False Positive ve False Negative nedir? Hangisi daha tehlikelidir?

False Positive: Gerçekte tehdit olmayan olayın tehdit olarak algılanması

False Negative: Gerçek bir tehdidin algılanamaması

False negative daha tehlikelidir çünkü fark edilmeden sisteme zarar verebilir.
---
15. En son hangi güvenlik zafiyetini inceledin?

En son CVE-2024-3094 adlı zafiyeti inceledim. Bu zafiyet, yaygın kullanılan bir kütüphanede uzaktan kod çalıştırmaya izin veriyordu. Potansiyel etkiyi ve düzeltme yöntemlerini araştırdım.

(Not: Bu soruda gerçek bir CVE kullanman seni bilgili gösterir. Yukarıdaki örneği güncelleyebiliriz.)
---
16. Honeypot nedir ve ne amaçla kullanılır?

Honeypot, saldırganları çekmek ve onların tekniklerini analiz etmek için kullanılan tuzak sistemdir. Gerçek sisteme zarar gelmeden tehditleri tanımayı sağlar.
---
17. Olay müdahale sürecini nasıl yönetirsin?

Olay müdahale sürecini 6 adımda yönetirim: Hazırlık, Tespit, Analiz, Müdahale, İyileştirme, Raporlama. Her adımda kayıt tutar, iş birliği yapar ve sistemin güvenliğini yeniden sağlarım.
---
18. Neden SOC alanını seçtin?

Gerçek zamanlı tehditlerle mücadele etmek, sürekli öğrenmek ve sistemleri korumak beni motive ediyor. Bu alan hem teknik hem stratejik düşünme becerilerimi kullanmamı sağlıyor.
---
19. Zafiyet taraması (vulnerability scanning) ile penetrasyon testi arasındaki fark nedir?

Zafiyet taraması otomatik araçlarla sistem açıklarını listeler. Penetrasyon testi ise bu açıkların gerçekten sömürülüp sömürülemeyeceğini manuel ve detaylı şekilde test eder.
---
20. Log korelasyonu nedir ve neden önemlidir?

Log korelasyonu, farklı sistemlerden gelen logları ilişkilendirerek tekil olayları anlamaya yarar. Böylece zincirleme saldırılar veya büyük tehditler daha net görünür.
