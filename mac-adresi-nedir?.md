# MAC Adresi Nedir?

**MAC (Media Access Control) adresi**, bir cihazın ağ arayüzüne atanan **benzersiz fiziksel** bir kimlik numarasıdır.

- 48 bit (6 byte) uzunluğundadır.
- Hexadecimal (onaltılık) biçimde yazılır: `00:1A:2B:3C:4D:5E`
- İlk 3 byte: üretici kodu (OUI)  
- Son 3 byte: cihaz kimliği

---

## Ne İşe Yarar?

- Yerel ağda cihazları tanımlar.
- Veri paketlerinin doğru cihaza ulaşmasını sağlar.
- ARP protokolü ile IP adresi MAC adresine çevrilir.

---

## MAC - IP Farkı

| Özellik  | MAC Adresi       | IP Adresi         |
|----------|------------------|-------------------|
| Tür      | Fiziksel adres    | Mantıksal adres   |
| Sabitlik | Değiştirilemez (genelde) | Değişebilir       |
| Kullanım | Yerel ağ         | Ağlar arası iletişim |

---

> **Not:** MAC adresi, cihazların ağ içinde birbirini tanımasını sağlar.
