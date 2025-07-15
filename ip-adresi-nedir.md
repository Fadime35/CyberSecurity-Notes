# IP Adresi Nedir?

**Ip Adresi** ,bir cihazın internette veya yerel ağda tanımlanmasını sağlayan sayısal bir adrestir.Bu adres, cihazların birbirleriyle iletişim kurmasını sağlar. 
IP adresi bilgisayarların internette nerede olduğunu gösterir.
- **Örnek bir IP adresi**: 192.168.1.1
---

## IP Adresinin Temel Özellikleri

- Mantıksal bir adrestir.
- Kolayca değiştirilebilir.
- IP adresleri, **veri paketlerinin doğru hedefe ulaşmasını** sağlar.
- İnternette iletişim için zorunludur.

---

## IP Adresi Türleri


### IPv4 (Internet Protocol version 4)

- **32 bit** uzunluğundadır.  
- Adresler, **nokta ile ayrılmış dört sayı**dan oluşur. Her sayı **0 ile 255** arasında değişir.  
- Örnek bir IPv4 adresi: `172.16.254.1`  
- En yaygın kullanılan IP adresi türüdür.  
- Toplamda yaklaşık **4.3 milyar** benzersiz adres üretilebilir.

> **Not:** Cihaz sayısının hızla artması nedeniyle IPv4 adresleri zamanla yetersiz kalmaya başlamıştır.

### IPv6 (Internet Protocol version 6)

- **128 bit** uzunluğundadır.  
- IPv4’ün yetersiz kalmasıyla birlikte geliştirilmiştir.  
- Daha fazla cihazın internete bağlanabilmesini sağlar.  
- Adresler, **8 grup halinde yazılan 4 haneli hexadecimal (onaltılık)** sayı sisteminden oluşur.  
- Örnek bir IPv6 adresi: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`  

---

## IP Adresinin Görevleri

- Cihazları tanımlamak  
- İnternet üzerinden veri paketlerinin doğru adrese yönlendirilmesini sağlamak  
- Ağ içi ve dışı iletişimi mümkün kılmak  

---

> **Not:** IP adresleri dinamik (değişken) veya statik (sabit) olabilir. Dinamik IP adresleri, internete bağlandıkça değişirken, statik IP adresleri sabit kalır.

## Dinamik ve Statik IP Adresleri

- **Dinamik IP Adresi:**  
  - Geçici ve değişebilen IP adresidir.
  - Cihaza otomatik olarak atanır (modem/DHCP ile).  
  - İnternet Servis Sağlayıcısı (ISS) tarafından geçici olarak verilir.  
  - Ev kullanıcıları genellikle dinamik IP kullanır.
  - Yönetimi kolaydır, IP tasarrufu sağlar.

- **Statik IP Adresi:**  
  - Manuel olarak ayarlanır ve değişmez.  
  - Web sunucuları, güvenlik kameraları gibi sürekli erişim gereken sistemlerde kullanılır.  
  - Erişimi sabit tutmak için idealdir.

 ---   
 
  > **Not:** Statik IP'ler güvenlik açısından daha fazla dikkat ister, çünkü IP sabit kaldığı için dış tehditlere hedef olma ihtimali artabilir.


 ## İç IP ve Dış IP Nedir?

###  İç IP (Private IP)
- Cihazlara yerel ağ (LAN) içinde atanır.  
- Yalnızca aynı yerel ağdaki cihazlar arasında iletişim için kullanılır.  
- Modem, bilgisayar, yazıcı gibi cihazlar bu IP ile haberleşir.  
- İnternete doğrudan çıkış yapamaz.

 **Örnek iç IP adresi**: `192.168.0.12` 

###  Dış IP (Public IP)
- Cihazların veya ağların internet üzerindeki adresidir.  
- İnternet Servis Sağlayıcısı (ISS) tarafından atanır.  
- Diğer ağlar ve internet ile doğrudan iletişim kurmayı sağlar.  
- Herkese açık bir adrestir.

**Örnek dış IP adresi**: `85.110.245.13` 

---
> **NOT**:
- Eğer IP adresi `10.x.x.x`, `172.16.x.x – 172.31.x.x`, veya `192.168.x.x` ile başlıyorsa: **İç IP’dir.**
- Bu aralıkların dışında kalan her IP: **Dış IP’dir.**







