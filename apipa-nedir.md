# APIPA Nedir?

**APIPA (Automatic Private IP Addressing)**, bir cihazın **DHCP sunucusundan IP adresi alamadığı** durumlarda otomatik olarak kendine verdiği **geçici bir IP adresidir**.

---

##  Özellikleri:
- IP aralığı: **169.254.0.1 - 169.254.255.254**
- Subnet maskesi: **255.255.0.0**
- **DHCP sunucusu bulunamazsa** otomatik olarak devreye girer.
- **Yalnızca yerel ağ (LAN)** içinde cihazlar arasında iletişim sağlar.
- İnternete çıkış için **yeterli değildir**.

---

##  Ne Zaman Kullanılır?
- DHCP sunucusu devre dışı kaldığında,
- Ağ kablosu takılı ama DHCP yapılandırılamamışsa,
- Bilgisayar IP adresi alamazsa otomatik olarak APIPA alır.

---

## Neden Önemlidir?
- Ağ sorunlarını teşhis etmek için ipucu verir.
- DHCP problemlerinin anlaşılmasını sağlar.
- Cihazların aynı yerel ağda sınırlı da olsa iletişim kurmasına olanak tanır.

---

## 🧪 Örnek:
Bir bilgisayar DHCP’den IP alamadığında IP yapılandırması şu şekilde olabilir:

