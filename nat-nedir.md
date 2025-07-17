# NAT Nedir? 

**NAT (Network Address Translation)**, **özel IP adreslerini** genel (public) IP adreslerine çeviren bir ağ teknolojisidir. 
Genellikle **router (yönlendirici)** cihazlar üzerinde çalışır.

---

## Amaç:
- Aynı anda birden fazla cihazın **tek bir genel IP adresi** üzerinden internete çıkmasını sağlar.
- IP tasarrufu sağlar.
- **IP adreslerini gizleyerek** güvenliği artırır.

---

## Nasıl Çalışır?
- Özel IP’ye sahip cihazdan gelen veri, NAT cihazı (örneğin modem) tarafından alınır.
- Bu veri paketi, NAT tarafından **genel IP adresiyle etiketlenir**.
- İnternete bu genel IP ile çıkar.
- Gelen yanıt, NAT tarafından doğru özel IP’ye yönlendirilir.

---

##  NAT Türleri

### 1. **Static NAT** (Statik NAT)
- Her özel IP, belirli bir genel IP'ye **sabit** olarak eşlenir.
- Küçük ağlarda kullanılır.

### 2. **Dynamic NAT** (Dinamik NAT)
- Özel IP'ler, mevcut olan genel IP havuzundan **rastgele bir IP** ile eşleştirilir.
- Genel IP sayısı kadar cihaz internete çıkabilir.

### 3. **PAT (Port Address Translation)** – *NAT Overload*
- Çok sayıda cihaz, **tek bir genel IP** ile internete çıkabilir.
- Port numaraları kullanılarak ayırt edilir.
- En yaygın kullanılan NAT türüdür.

---

## Neden Önemlidir?

- IPv4 adreslerinin yetersizliğine **çözüm sunar**.
- Yerel ağdaki cihazları dışarıdan gelen tehditlere karşı **korur**.
- Ev, okul ve iş yerlerinde **standart ağ güvenliği** sağlar.

----

>**NOT:** NAT, ağ içindeki cihazların internete **gizli ve kontrollü** şekilde çıkmasını sağlar.
