## Subnetting Nedir?

**Subnetting**, büyük bir IP ağını daha küçük alt ağlara (subnet) bölme işlemidir.

- Ağ trafiğini azaltır.  
- Ağ yönetimini kolaylaştırır.  
- Güvenliği artırır.  
- IP adreslerini daha etkin kullanmayı sağlar.

> **Not:** Subnetting, özellikle büyük ağlarda yönetim ve güvenlik açısından kritik bir işlemdir.

---

## Subnet Maskesi Nedir?

**Subnet Maskesi**, bir IP adresinde hangi kısmın ağ (network), hangi kısmın cihaz (host) adresi olduğunu belirleyen sayısal bir ifadedir.  
Subnetting işlemini uygulamak ve ağları tanımlamak için kullanılır.

- Örneğin, ilk 24 bit ağ adresini, kalan 8 bit cihaz adresini temsil eder.  
- Aynı ağda olup olmadığını anlamak için cihazlar bu maskeyi kullanır.

---

## CIDR Notasyonu Nedir?

**CIDR (Classless Inter-Domain Routing)**, IP adreslerini ve subnet maskelerini daha esnek ve verimli bir şekilde göstermek için kullanılan bir yöntemdir.

- IP adresinin sonuna `/` işaretiyle birlikte ağda kullanılan bit sayısı yazılır.  
- CIDR değeri ne kadar büyükse, ağ o kadar küçüktür (çünkü daha fazla bit ağ kısmına ayrılmış olur).

---

## CIDR Örneği

- IP adresi: `192.168.1.0/24`  
  - Buradaki `/24` ifadesi, subnet maskesinin ilk 24 bitinin ağ için ayrıldığını belirtir.  
  - Bu, `255.255.255.0` subnet maskesine eşdeğerdir.

---

## Maksimum Cihaz Sayısı Nasıl Hesaplanır?

- Toplam host sayısı = `2^(32 - subnet_mask_bits) - 2`  
  - Buradaki `-2`, bir IP adresinin ağ adresi, diğerinin ise broadcast adresi olarak ayrılmasından kaynaklanır.

---

## Örnek Hesaplama

- CIDR: `192.168.1.0/26`  
- Ağ bit sayısı: 26  
- Host bit sayısı: 32 - 26 = 6  
- Maksimum cihaz sayısı: `2^6 - 2 = 64 - 2 = 62`

Yani, bu subnet içinde **en fazla 62 cihaz** bulunabilir.

---

## CIDR ve Host Sayısı Tablosu

| CIDR    | Subnet Maskesi      | Maksimum Host Sayısı |
|---------|---------------------|-----------------------|
| /24     | 255.255.255.0       | 254                   |
| /25     | 255.255.255.128     | 126                   |
| /26     | 255.255.255.192     | 62                    |
| /27     | 255.255.255.224     | 30                    |
| /28     | 255.255.255.240     | 14                    |
| /29     | 255.255.255.248     | 6                     |

> **Not:** CIDR notasyonu, IP adreslerini ve subnetleri daha esnek ve verimli kullanmamıza olanak tanır.




