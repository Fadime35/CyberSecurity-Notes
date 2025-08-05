# Linux Terminal Komutları 

## 1. `ls` – Listeleme
- Dizin içeriğini listeler.
- Sık Kullanım:
  - `ls` → Bulunduğun klasördeki dosyaları listeler.
  - `ls -l` → Detaylı listeleme (izinler, boyut, tarih).
  - `ls -a` → Gizli dosyalarla birlikte listeler.
  - `ls -lh` → Boyutları okunabilir formatta gösterir.

## 2. `cd` – Dizin Değiştirme
- Mevcut çalışma dizinini değiştirir.
- Sık Kullanım:
  - `cd /home/user` → Belirtilen dizine geçer.
  - `cd ..` → Bir üst dizine çıkar.
  - `cd` → Ana dizine gider.
  - `cd -` → Önceki dizine geri döner.

## 3. `pwd` – Mevcut Dizin Yolunu Gösterme
- Terminalde hangi dizinde olduğunu tam yoluyla gösterir.
- Sık Kullanım:
  - `pwd` → Örn: `/home/user/Desktop`

## 4. `mkdir` – Klasör Oluşturma
- Yeni bir klasör (dizin) oluşturur.
- Sık Kullanım:
  - `mkdir yeni_klasör` → Belirtilen isimde klasör oluşturur.
  - `mkdir -p a/b/c` → Alt klasörlerle birlikte oluşturur.

## 5. `rmdir` – Klasör Silme
- Boş klasörleri silmek için kullanılır.
- Sık Kullanım:
  - `rmdir klasör_adı`

## 6. `cat` – Dosya İçeriğini Gösterme
- Dosya içeriğini terminalde görüntüler.
- Sık Kullanım:
  - `cat dosya.txt` → Dosyanın içeriğini gösterir.
  - `cat dosya1 dosya2` → Birleştirip gösterir.
  - `cat > dosya.txt` → Yeni dosya oluşturur ve içine yazı yazılır (Ctrl+D ile çıkılır).

## 7. `grep` – Metin Arama
- Belirli bir ifadeyi dosyada veya çıktı içinde arar.
- Sık Kullanım:
  - `grep "kelime" dosya.txt` → Dosyada “kelime” geçen satırları gösterir.
  - `ps aux | grep firefox` → Bellekteki işlemler arasında “firefox” geçenleri arar.
  - `grep -i` → Büyük/küçük harf duyarsız arama.
  - `grep -r` → Dizin içinde ve alt dizinlerde arama.

## 8. `tail` – Dosyanın Son Satırlarını Görüntüleme
- Bir dosyanın son satırlarını gösterir.
- Sık Kullanım:
  - `tail dosya.txt` → Son 10 satırı gösterir.
  - `tail -n 20 dosya.txt` → Son 20 satırı gösterir.
  - `tail -f dosya.txt` → Dosya değiştikçe yeni satırları anlık gösterir (log takibi).

## 9. `ifconfig` – Ağ Arayüzü Bilgisi
- Ağ arabirimlerinin IP adresi, MAC adresi, durum gibi bilgilerini listeler.
- Sık Kullanım:
  - `ifconfig` → Tüm arayüzleri gösterir.
  - Alternatif: `ip addr`

## 10. `uptime` – Sistem Çalışma Süresi
- Bilgisayarın ne kadar süredir açık olduğunu ve yük ortalamasını gösterir.
- Sık Kullanım:
  - `uptime` → Örn: 3 saat 15 dakikadır açık, load average bilgisiyle birlikte.

## 11. `history` – Komut Geçmişi
- Terminalde daha önce yazılan komutları listeler.
- Sık Kullanım:
  - `history`  
  - `!145` → Geçmişteki 145 numaralı komutu tekrar çalıştırır.

## 12. `clear` – Terminal Ekranını Temizleme
- Ekrandaki tüm çıktıları siler.
- Sık Kullanım:
  - `clear`

## 13. `ping` – Ağ Bağlantısını Test Etme
- Belirtilen adrese ICMP paketleri göndererek ağ bağlantısını test eder.
- Sık Kullanım:
  - `ping google.com`  
  - `ping -c 4 8.8.8.8` → Sadece 4 ping atar.

## 14. `apt-get install` – Paket Yükleme (Debian/Ubuntu)
- Yazılım yüklemek için kullanılır.
- Sık Kullanım:
  - `sudo apt-get install paket_adi`  
  - `sudo apt update && sudo apt upgrade` → Sistem güncelleme

## 15. `sudo su` – Root Yetkisiyle Oturum Açma
- Superuser (yönetici) yetkisiyle terminale geçiş yapar.
- Sık Kullanım:
  - `sudo su` → Root kullanıcı olur.
  - `exit` → Normal kullanıcıya geri döner.

## 16. `echo` – Yazı Yazdırma
- Terminale veya dosyaya metin yazmak için kullanılır.

- `echo "Merhaba"` → Terminale yazar.  
- `echo $HOME` → Değişkenin değerini gösterir.  
- `echo "Deneme" > dosya.txt` → Dosyaya yazar, varsa içeriği siler.  
- `echo "Yeni satır" >> dosya.txt` → Dosyanın sonuna ekler.

## 17. `cp` – Dosya/Klasör Kopyalama
- Dosya veya klasörleri başka konuma kopyalar.

- `cp dosya.txt /hedef/` → Dosya kopyalar.  
- `cp dosya1.txt dosya2.txt` → Aynı dizinde kopya oluşturur.  
- `cp -r klasör/ /hedef/` → Klasörü içeriğiyle birlikte kopyalar.

**Parametreler:**
- `-r` → Klasör kopyalamak için gerekir.  
- `-i` → Üzerine yazmadan önce onay ister.  
- `-v` → Kopyalama işlemini terminalde gösterir.  
- `-u` → Sadece kaynak dosya hedeften daha yeniyse kopyalar.


---

## NOT:
- Kombinasyon:  
  - `cat dosya.txt | grep "hata"` → Dosyada "hata" geçen satırları bulur.  
  - `tail -f /var/log/syslog` → Canlı log izleme  
  - `grep -r "şifre" /etc` → Dizin genelinde anahtar kelime arama
- Log analizi ve sistem takibinde bu komutlar sık kullanılır.
- `man komut_adı` veya `komut --help` ile detaylı yardım alınabilir.





