# Temel Ağ  Komutları

## 1. `ping`
Bir hedef sistemin (IP ya da domain) ağda erişilebilir olup olmadığını test etmek için kullanılır. ICMP Echo paketleri gönderir ve cevap sürelerini ölçer. Paket kaybı ya da gecikme gibi durumları analiz etmede faydalıdır.

**Örnek:**
- ping 192.168.1.157 
- ping 'www.google.com'

---

## 2. `tracert` / `traceroute`
Bir paketin hedefe ulaşana kadar geçtiği tüm router (yönlendirici) noktalarını gösterir. Her bir atlama için gecikme süresi de listelenir. Ağdaki darboğaz veya kopmaların hangi noktada olduğunu anlamak için kullanılır.

**Örnek:** 
- tracert google.com      # Windows
- traceroute google.com   # Linux/macOS

  ---

## 3. `netstat`
Ağ bağlantıları, açık portlar ve hangi uygulamanın hangi portu kullandığı gibi bilgileri gösterir. Sistem üzerinde aktif olan TCP/UDP bağlantılarını analiz etmek için kullanılır. Şüpheli bağlantıları tespit etmekte de işe yarar.

---

## 4. `nslookup`
Alan adlarının IP adresine (veya tersine) çözümünü yapmak için kullanılan bir DNS sorgulama aracıdır. DNS sorunlarını tanımlamak veya hangi DNS kaynağından yanıt alındığını görmek için kullanılır.

---

## 5. `ipconfig` / `ifconfig`
`ipconfig` Windows’ta, `ifconfig` ise Linux/macOS’ta kullanılır. Ağ arayüzlerinin IP adresi, alt ağ maskesi ve varsayılan ağ geçidi gibi bilgilerini gösterir. 



