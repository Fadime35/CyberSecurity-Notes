# OSI ve TCP/IP Modeli 

## OSI (Open Systems Interconnection) Modeli

OSI modeli, ağ iletişimini 7 katmanda tanımlar. Her katman, belirli bir işlevi yerine getirir.

| Katman No | Katman Adı            | Görevi                                                                 |
|-----------|------------------------|------------------------------------------------------------------------|
| 7         | Uygulama (Application) | Kullanıcıya en yakın katmandır. HTTP, FTP, SMTP gibi protokoller burada çalışır. |
| 6         | Sunum (Presentation)   | Veriyi şifreler, sıkıştırır, biçimlendirir. (JPEG, MPEG vb.)          |
| 5         | Oturum (Session)       | İki cihaz arasında oturum açar, yönetir, sonlandırır.                |
| 4         | Taşıma (Transport)     | Veriyi parçalara böler ve iletim güvenliğini sağlar. (TCP, UDP)      |
| 3         | Ağ (Network)           | IP adresleme ve yönlendirme yapılır. (IP, ICMP)                       |
| 2         | Veri Bağlantısı (Data Link) | MAC adresi ile veri çerçevelerini işler. (Ethernet, Switch)       |
| 1         | Fiziksel (Physical)    | Elektriksel sinyaller, kablolar, donanımlar. (Hub, kablo)            |

---

## TCP/IP Modeli

TCP/IP modeli, internetin gerçek işleyişini açıklayan 4 katmanlı bir modeldir.

| Katman No | Katman Adı              | OSI Karşılığı                              | Protokoller                        |
|-----------|--------------------------|--------------------------------------------|-----------------------------------|
| 4         | Uygulama (Application)   | OSI 5-6-7. katmanlar                        | HTTP, FTP, SMTP, DNS              |
| 3         | Taşıma (Transport)       | OSI 4. katman                               | TCP, UDP                          |
| 2         | İnternet (Internet)      | OSI 3. katman                               | IP, ICMP, ARP                     |
| 1         | Ağ Erişim (Network Access)| OSI 1-2. katmanlar                          | Ethernet, Wi-Fi, MAC             |

---

## 🔄 OSI ve TCP/IP Karşılaştırması

| Özellik           | OSI Modeli                     | TCP/IP Modeli                  |
|-------------------|--------------------------------|--------------------------------|
| Katman Sayısı     | 7                              | 4                              |
| Geliştiren        | ISO                             | DARPA                          |
| Kullanım          | Teorik ve öğretici model       | Gerçek dünyada kullanılan model |
| Katman Ayırımı    | Daha ayrıntılı                 | Daha sade                      |
| Protokol Bağımsız | Evet                            | Hayır, belirli protokollere dayanır |

---



