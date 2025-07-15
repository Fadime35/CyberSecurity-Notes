# Subnetting ve Subnet Maskesi Nedir?

## Subnetting Nedir?

**Subnetting**, büyük bir IP ağını daha küçük alt ağlara (subnet) bölme işlemidir.  

## Subnetting’in Faydaları

- Ağ trafiğini azaltır.  
- Ağ yönetimini kolaylaştırır.  
- Güvenliği artırabilir.  
- IP adreslerini daha etkin kullanmayı sağlar.

---
> **Not:** Subnetting, özellikle büyük ağlarda yönetim ve güvenlik açısından kritik bir işlemdir.

## Subnet Maskesi Nedir?

**Subnet Maskesi**, IP adresinde hangi bölümün ağ (network), hangi bölümün cihaz (host) adresi olduğunu belirten sayısal bir maskedir.  
Subnetting işlemini göstermek ve uygulamak için kullanılır.

- Örneğin, ilk 24 bit ağ adresini, kalan 8 bit cihaz adresini gösterir.  
- Aynı ağda olup olmadığını anlamak için kullanılır.

---

**CIDR (Classless Inter-Domain Routing)**, IP adreslerini ve subnet maskelerini daha esnek ve verimli şekilde gösterme yöntemidir.  

- IP adresinin sonuna `/` işareti ve ağda kullanılan bit sayısı eklenir.  
- CIDR değeri ne kadar büyükse, ağ o kadar küçüktür. (Çünkü daha fazla bit ağ kısmına ayrılmış olur.)

---

## CIDR Örneği

- IP adresi: `192.168.1.0/24`  
  - Buradaki `/24` ifadesi, subnet maskesinin ilk 24 bitinin ağ (network) için ayrıldığını belirtir.  
  - Bu, `255.255.255.0` subnet maskesine eşdeğerdir.

---

## Maksimum Cihaz Sayısı Nasıl Hesaplanır?

- Toplam host sayısı = `2^(32 - subnet_mask_bits) - 2`  
  - Buradaki `-2`, ağ adresi ve broadcast adresi için ayrılan 2 IP'yi çıkarır.

---

## Örnek Hesaplama

- CIDR: `192.168.1.0/26`  
- Ağ bit sayısı: 26  
- Host bit sayısı: 32 - 26 = 6  
- Maksimum cihaz sayısı: `2^6 - 2 = 64 - 2 = 62`

Yani, bu subnet içinde **62 cihaz bağlanabilir**.

---

## CIDR ve Host Sayısı Tablosu

| CIDR    | Subnet Maskesi      | Maksimum Host Sayısı |
|---------|---------------------|---------------------|
| /24     | 255.255.255.0       | 254                 |
| /25     | 255.255.255.128     | 126                 |
| /26     | 255.255.255.192     | 62                  |
| /27     | 255.255.255.224     | 30                  |
| /28     | 255.255.255.240     | 14                  |
| /29     | 255.255.255.248     | 6                   |

---

> **Not:** CIDR notasyonu, IP adreslerini ve subnetleri daha esnek ve verimli kullanmamızı sağlar.



