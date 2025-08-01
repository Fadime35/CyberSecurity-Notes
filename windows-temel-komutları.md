# Windows Temel Komutları (CMD ve PowerShell)

## 1. `dir`
Klasör içeriğini listeler. Linux'taki `ls` komutuna benzer.

**Örnek:**
- `dir` → Bulunduğun dizindeki dosya ve klasörleri listeler.

---

## 2. `cd` (Change Directory)
Dizin (klasör) değiştirir.

**Örnek:**
- `cd Belgeler` → "Belgeler" klasörüne geçer.
- `cd ..` → Bir üst dizine çıkar.

---

## 3. `cls`
Ekranı temizler yani terminali sıfırlar.

**Örnek:**
- `cls` → Komut geçmişi temizlenir.

---

## 4. `mkdir` ve `rmdir`
Yeni klasör oluşturur veya klasörü siler.

**Örnek:**
- `mkdir test` → "test" adında klasör oluşturur.
- `rmdir test` → "test" klasörünü siler.

---

## 5. `del`
Dosya silmek için kullanılır.

**Örnek:**
- `del dosya.txt`

---

## 6. `echo`
Ekrana yazı yazdırır ya da değişken değerlerini gösterir.

**Örnek:**
- `echo Merhaba`
- `echo %USERNAME%` → Giriş yapan kullanıcı adını gösterir.

---

## 7. `tasklist` ve `taskkill`
Sistem üzerindeki çalışan işlemleri görüntüler ve sonlandırır.

**Örnek:**
- `tasklist` → Aktif görevleri listeler.
- `taskkill /IM notepad.exe /F` → Not Defteri'ni kapatır.

---

### 8. `ipconfig` (Internet Protocol Configuration)
Windows sistemlerde ağ arayüzlerine ait IP yapılandırmasını görüntülemek için kullanılır. Özellikle IP adresi, alt ağ maskesi, varsayılan ağ geçidi gibi bilgileri gösterir.

**Kullanım Örnekleri:**
- `ipconfig` → Temel ağ bilgilerini listeler.
- `ipconfig /all` → MAC adresi, DHCP durumu, DNS sunucuları gibi ayrıntılı bilgi verir.
- `ipconfig /release` → Mevcut IP adresini devre dışı bırakır (DHCP ile alınan adres).
- `ipconfig /renew` → Yeni bir IP adresi talep eder (DHCP’den).
- `ipconfig /flushdns` → DNS önbelleğini temizler, DNS çözümleme sorunlarını gidermek için kullanılır.

**Ne işe yarar?**
- IP adresi çakışmalarını kontrol etme
- DHCP yapılandırmasını test etme
- DNS önbelleğini sıfırlayarak çözümleme hatalarını giderme

---

### 9.`ping` (Packet Internet Groper)
Ağdaki başka bir cihazla iletişim kurmayı test etmek için ICMP (Internet Control Message Protocol) kullanır. Uzak bir IP adresine veya alan adına 
ICMP Echo Request paketi gönderir ve gelen yanıt süresini ölçer.

**Kullanım Örnekleri:**
- `ping 8.8.8.8` → Google DNS sunucusuna doğrudan ping atılır.
- `ping google.com` → DNS çözümlemesi de test edilmiş olur.
- `ping -t 192.168.1.1` → Ping işlemini sürekli tekrar eder (Ctrl+C ile durdurulur).
- `ping -n 10 google.com` → Belirtilen sayıda (örnekte 10) ping atar.

**Ne işe yarar?**
- Hedef sistemin erişilebilir olup olmadığını kontrol eder.
- Gecikme süresi (ms) ve paket kaybı bilgisi ile ağ performansını ölçer.
- DNS çözümleme sorunlarını test etmek için domain pinglenebilir.

---
**NOT:**

**ipconfig** genellikle yerel bilgisayarın IP yapılandırmasını görmek veya sıfırlamak için kullanılırken, **ping** ağı test etmek ve bağlantı kontrolü yapmak
için kullanılır.

İkisi birlikte kullanıldığında, bir sistemin hem yerel IP ayarları hem de dış ağla bağlantı durumu hakkında net bilgi verir.

---

## 10. `copy`, `xcopy`, `robocopy`

- Dosya ve klasör kopyalamada kullanılır.
- `copy`: Basit dosya kopyalama işlemleri içindir. Alt klasörleri kopyalayamaz.
- `xcopy`: Dosya ve klasörleri (alt klasörlerle birlikte) kopyalar. Daha esnektir.
- `robocopy`: Büyük klasörleri senkronize etmek (ayna gibi kopyalamak) için kullanılır. Hızlı ve güçlüdür.

---

**Örnekler:**

- `copy dosya.txt D:\yedek\`  
  → `dosya.txt` dosyası `D:\yedek\` klasörüne kopyalanır.

- `xcopy D:\veriler\*.* C:\backup\ /s /i`  
  → `D:\veriler\` içindeki tüm dosya ve alt klasörler `C:\backup\` konumuna kopyalanır.  
  - `/s`: Alt klasörleri de dahil eder (boş klasörler hariç).  
  - `/i`: Hedefin klasör olduğunu varsayar, kullanıcıya sormaz.

- `robocopy D:\veriler C:\backup /MIR`  
  → `D:\veriler` klasörü `C:\backup` ile **birebir aynı hale** getirilir.  
  - `/MIR`: "Mirror" (ayna) anlamındadır. Kaynak klasörün içeriğini hedefe tamamen yansıtır.  
  - Yeni dosyalar kopyalanır, ancak **hedefte olup kaynakta olmayan dosyalar silinir**.

---

 **Not:**
 
`/MIR` komutu yedekleme değil, **eşitleme** (senkronizasyon) amacı taşır. Hedef klasördeki bazı dosyalar silinebilir. Bu nedenle dikkatli kullanılmalıdır.

---

## 11. `whoami`

- Sistemde oturum açmış olan **kullanıcının adını** gösterir.
- Eğer bilgisayar bir **domain**’e bağlıysa, domain bilgisiyle birlikte gösterir.
- Hem **Windows CMD**, hem **PowerShell**, hem de **Linux terminali** içinde çalışır.

---

### 12. `date`
- Sistem tarihini gösterir veya değiştirir.
- Komutu yazdığınızda mevcut tarihi gösterir ve yeni tarih girmeniz istenir (boş geçerek değişiklik yapılmadan çıkılabilir).

---

## 13. `time`

- Bilgisayarın sistem saatini gösterir veya değiştirmenizi sağlar.
- Komutu yazdığınızda mevcut saat gösterilir ve yeni saat girme isteği çıkar.

---

## 14. `exit`

- Açık olan komut istemcisi (CMD veya PowerShell) penceresini kapatır.
- Scriptler içinde komutu bitirmek için de kullanılır.

---

## 15. `shutdown`

- Bilgisayarı kapatma, yeniden başlatma veya oturumu kapatma gibi işlemler için kullanılır.
- Genellikle zamanlı veya uzaktan yönetimli kapatmalarda kullanılır.

**Yaygın Parametreler:**

- /s → Bilgisayarı kapatır.

- /r → Bilgisayarı yeniden başlatır.

- /l → Oturumu kapatır.

- /t [saniye] → Belirtilen saniye sonra işlem yapılır.

- /f → Zorla kapat (uygulamaları kapatır).


