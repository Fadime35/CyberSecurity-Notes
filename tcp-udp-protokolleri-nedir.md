# TCP ve UDP Protokolleri Nedir?

## TCP (Transmission Control Protocol)
- **Bağlantı tabanlı** bir protokoldür.
- Verinin güvenli, sıralı ve eksiksiz iletilmesini sağlar.
- Alıcıdan her veri paketi için onay (ACK) bekler.
- Ağ trafiği daha fazladır ancak veri kaybı riski düşüktür.
- Yavaş ama **güvenilir** iletişim sağlar.

🧰 **TCP Kullanım Alanları:**
- Web tarayıcıları (HTTP/HTTPS)
- E-posta (SMTP, IMAP, POP3)
- Dosya transferi (FTP)

---

## UDP (User Datagram Protocol)
- **Bağlantısız** bir protokoldür.
- Veri paketi gönderilir, alıcıdan onay beklenmez.
- Hızlıdır ama veri kaybı yaşanabilir.
- Sıra garantisi yoktur, paketler kaybolabilir veya karışabilir.

⚡ **UDP Kullanım Alanları:**
- Gerçek zamanlı uygulamalar (video konferans, online oyunlar)
- DNS sorguları
- Canlı yayın servisleri

---

## TCP ve UDP Arasındaki Farklar

| Özellik            | TCP                                | UDP                               |
|--------------------|-------------------------------------|------------------------------------|
| Bağlantı           | Bağlantı tabanlı                    | Bağlantısız                        |
| Güvenilirlik       | Güvenilirdir                        | Güvenilir değildir                 |
| Hız                | Daha yavaştır                       | Daha hızlı                         |
| Sıralama           | Paket sıralaması sağlar             | Sıralama garantisi yoktur          |
| Hata kontrolü      | Hata kontrolü ve yeniden gönderim vardır   | Hata kontrolü yapılmaz             |
| Kullanım alanı     | Web, e-posta, dosya transferi       | Video, ses akışı, oyun, DNS        |




