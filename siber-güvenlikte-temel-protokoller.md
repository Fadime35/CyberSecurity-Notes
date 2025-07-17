# Siber Güvenlikte Temel Protokoller

Siber güvenlikte ağ trafiğini analiz etmek, zafiyetleri tespit etmek ve savunma mekanizmaları geliştirmek için kullanılan temel protokollerin görevleri, port numaraları ve güvenlik durumları aşağıda özetlenmiştir.

---

## 1. HTTP (HyperText Transfer Protocol)
- Web tarayıcıları ile sunucular arasında veri alışverişini sağlar.
- Web sitelerinden metin, resim, video gibi içerikleri almak için kullanılır.
- **Port:** 80 (TCP)
- **Güvenlik:** Şifreleme yoktur; veriler düz metin olarak iletilir.
- **Zafiyet:** Sniffing, Man-in-the-Middle (MitM)
- **Alternatif:** HTTPS (Port 443)

---

## 2. HTTPS (HTTP Secure)
- HTTP'nin TLS/SSL ile güvenli hale getirilmiş versiyonudur.
- Web iletimini şifreleyerek veri gizliliğini ve bütünlüğünü sağlar.
- **Port:** 443 (TCP)
- **Kullanım:** Bankacılık, formlar, giriş sayfaları, ödeme işlemleri

---

## 3. FTP (File Transfer Protocol)
- İstemci ile sunucu arasında dosya gönderme ve alma işlemi yapar.
- **Port:** 21 (komut, TCP), 20 (veri, TCP)
- **Güvenlik:** Şifreleme yoktur; kimlik bilgileri açık iletilir.
- **Zafiyet:** Sniffing ile parola çalınabilir.
- **Alternatif:** SFTP (Port 22)

---

## 4. SFTP (SSH File Transfer Protocol)
- FTP'nin güvenli versiyonudur, SSH üzerinden çalışır.
- **Port:** 22 (TCP)
- **Avantaj:** Tüm veri aktarımı şifrelenir, kimlik doğrulama zorunludur.

---

## 5. DNS (Domain Name System)
- Alan adlarını IP adresine çevirerek tarayıcıların web sitelerine erişmesini sağlar.
- **Port:** 53 (UDP/TCP)
- **Saldırılar:** DNS Spoofing, Cache Poisoning, DNS Hijacking
- **Savunma:** DNSSEC, DNS-over-HTTPS (DoH)

---

## 6. DHCP (Dynamic Host Configuration Protocol)
- Cihazlara IP adresi, subnet mask, DNS gibi ağ ayarlarını otomatik olarak atar.
- **Port:** 67 (Sunucu, UDP), 68 (İstemci, UDP)
- **Saldırılar:** Rogue DHCP, DHCP Starvation

---

## 7. SSH (Secure Shell)
- Uzak sistemlere şifreli bağlantı sağlar; genellikle sunucu yönetiminde kullanılır.
- **Port:** 22 (TCP)
- **Kullanım:** Dosya aktarımı, terminal bağlantısı, port yönlendirme
- **Avantaj:** Telnet'e göre tamamen şifreli ve güvenlidir.
- Remote login protocol

---

## 8. Telnet
- Uzak bağlantı sağlar, ancak trafiği şifrelemez.
- **Port:** 23 (TCP)
- **Güvenlik:** Çok zayıftır; veriler düz metin ile gider.
- **Alternatif:** SSH (Port 22)
- Remote login protocol

---

## 9. SMTP (Simple Mail Transfer Protocol)
- E-posta göndermek için istemci ile sunucu arasında çalışır.
- **Port:** 25 (güvensiz, TCP), 465 (SMTPS, SSL/TLS), 587 (Submission, TLS)
- **Zafiyet:** Kimlik doğrulama yapılmazsa spoofing, spam riski taşır.

---

## 10. POP3 (Post Office Protocol v3)
- E-postaları sunucudan indirip yerel cihaza kaydeder, genellikle sunucudan siler.
- **Port:** 110 (güvensiz, TCP), 995 (POP3S, SSL/TLS)
- **Fark:** Offline çalışmaya uygundur; e-posta bir kez indirilip silinir, başka cihazdan tekrar erişilemez.

---

## 11. IMAP (Internet Message Access Protocol)
- E-postaları sunucuda tutarak cihazlar arasında senkronize şekilde erişilmesini sağlar.
- **Port:** 143 (güvensiz, TCP), 993 (IMAPS, SSL/TLS)
- **Avantaj:** Çoklu cihaz desteği, klasör yapısı, sunucu senkronizasyonu

---

## 12. ICMP (Internet Control Message Protocol)
- Ağ durumu, erişim ve hata mesajları için kullanılır (Örneğin `ping` komutu).
- **Port:** Yok (IP katmanında çalışır.)
- **Saldırılar:** Ping of Death, ICMP Flood (DoS)

---

## 13. SNMP (Simple Network Management Protocol)
- Ağ cihazlarını izleme ve yönetme amacıyla kullanılır (Örneğin router/switch durumu).
- **Port:** 161 (sorgu, UDP), 162 (trap/tuzak, UDP)
- **Sürüm Farkları:**
  - **v1/v2:** Şifreleme yok
  - **v3:** Kimlik doğrulama + şifreleme (güvenli sürüm)

---

## 14. SSL/TLS (Secure Sockets Layer / Transport Layer Security)
- Verilerin şifrelenmesini sağlar; özellikle HTTPS, SMTP, IMAP gibi protokollerle birlikte kullanılır.
- **Port:** Protokole göre değişir (örneğin HTTPS için 443 TCP)
- **Fark:** SSL artık eskidir; modern sistemlerde TLS (1.2 ve üzeri) kullanılır.
- **Kullanım:** Web trafiği, e-posta, VPN, VoIP
- **Zafiyet:** Eski sürümler (SSL 2.0/3.0, TLS 1.0) güvenli değildir.

---

## 15. SMB (Server Message Block)
- Dosya, yazıcı ve kaynak paylaşımı için kullanılır (özellikle Windows sistemlerinde).
- **Port:** 445 (TCP, güncel), 139 (TCP, NetBIOS üzerinden)
- **Zafiyet:** WannaCry gibi zararlı yazılımlar SMB açığını kullanır.
- **Güvenlik:** SMBv1 kapatılmalıdır; SMBv3 kullanılmalıdır.

---

## 16. NetBIOS (Network Basic Input Output System)
- Yerel ağdaki (LAN) cihazların ad çözümlemesini ve kaynak paylaşımını sağlar.
- **Port:** 137 (UDP, Name Service), 138 (UDP, Datagram Service), 139 (TCP, Session Service)
- **Zafiyet:** Kimlik sızdırma, bilgi toplama (enumeration)
- **Güvenlik:** Geniş ağda kullanımı önerilmez, modern sistemlerde devre dışı bırakılmalıdır.

---

## 17. MySQL
- Veritabanı yönetim sistemidir. İstemci-sunucu arasında SQL tabanlı veri alışverişi sağlar.
- **Port:** 3306 (TCP)
- **Zafiyet:** Zayıf parolalar, uzaktan erişime açık konfigürasyonlar
- **Güvenlik:** Veritabanına erişim sınırlanmalıdır, SSL ve güçlü parola politikaları uygulanmalıdır.

---

## 18. RDP (Remote Desktop Protocol)
- Grafiksel arayüz üzerinden uzak masaüstü bağlantısı sağlar (Windows).
- **Port:** 3389 (TCP)
- **Zafiyet:** Brute force saldırıları, ransomware bulaştırma vektörü olabilir.
- **Güvenlik:** MFA, IP kısıtlama, RDP gateway, güçlü parola kullanımı önerilir.

---

## 19. ARP (Address Resolution Protocol)
- IP adreslerini MAC adreslerine çevirir (ağ katmanı ile veri bağlantı katmanı arasında köprü).
- **Port:** Yok (katman 2 protokolüdür)
- **Zafiyet:** ARP Spoofing, Man-in-the-Middle saldırıları
- **Güvenlik:** Dynamic ARP Inspection, statik ARP girişleri gibi önlemler alınabilir.

---

> **Güvenlik Notu:**  
> Protokollerin güvenli sürümleri tercih edilmelidir. Örneğin:  
> - HTTP (Port 80) ❌ → HTTPS (Port 443) ✅  
> - FTP (Port 21) ❌ → SFTP (Port 22) ✅  
> - Telnet (Port 23) ❌ → SSH (Port 22) ✅  
> - POP3 (Port 110) ❌ → POP3S (Port 995) ✅  
> - IMAP (Port 143) ❌ → IMAPS (Port 993) ✅  
> - SMTP (Port 25) ❌ → SMTP TLS/SSL (Port 465/587) ✅








