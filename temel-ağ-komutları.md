# Temel Ağ Komutları

## 1. `ping`
Bir hedef sistemin (IP ya da domain) ağda erişilebilir olup olmadığını test etmek için kullanılır. ICMP Echo paketleri gönderir ve yanıt sürelerini ölçer. Paket kaybı veya ağ gecikmesi gibi sorunları analiz etmede kullanılır.

**Örnek:**
- `ping 192.168.1.157`  
- `ping www.google.com`

---

## 2. `tracert` / `traceroute`
Bir paketin hedefe ulaşana kadar geçtiği tüm yönlendirici (router) noktalarını listeler. Her atlamada oluşan gecikmeleri gösterir. Ağ üzerindeki kopma veya yavaşlamanın hangi noktada olduğunu tespit etmek için kullanılır.

**Örnek:**  
- `tracert google.com` *(Windows)*  
- `traceroute google.com` *(Linux/macOS)*

---

## 3. `netstat`
Ağ bağlantılarını, açık portları ve hangi uygulamanın hangi portu kullandığını gösterir. TCP/UDP bağlantıları analiz etmek, açık portları görmek ve şüpheli bağlantıları tespit etmek için kullanılır.

---

## 4. `nslookup`
Bir alan adının IP adresine veya IP adresinin alan adına çevrilmesini sağlar. DNS sunucusunun verdiği yanıtları gösterir. DNS sorunlarını tanılamak ve sorgulama testleri yapmak için kullanılır.

**Örnek:**  
- `nslookup google.com`

---

## 5. `ipconfig` / `ifconfig`
- `ipconfig` → Windows sistemlerde  
- `ifconfig` → Linux/macOS sistemlerde kullanılır.

Ağ arayüzlerine ait IP adresi, alt ağ maskesi, ağ geçidi gibi bilgileri görüntülemek için kullanılır. Ayrıca `ipconfig /release` ve `ipconfig /renew` gibi parametrelerle IP yenileme işlemleri de yapılabilir.

---
**NOT:**  *Bu komutlar, temel ağ yapılandırması ve sorun giderme işlemlerinde hızlı analiz imkânı sağlar. Mülakatlarda sıkça sorulan ve uygulamada da aktif olarak kullanılan komutlardır.*
