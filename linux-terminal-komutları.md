# Linux Terminal Temel Komutları - Mülakat Notları

## 1. `ls` – Listeleme
- Dizin içeriğini listeler.
- `ls -l` → Detaylı listeleme  
- `ls -a` → Gizli dosyaları da gösterir  
- `ls -lh` → Boyutları okunabilir formatta

## 2. `cd` – Dizin Değiştirme
- Çalışma dizinini değiştirir.
- `cd ..` → Üst dizine çıkar  
- `cd ~` → Ana dizine gider  
- `cd -` → Önceki dizine döner

## 3. `pwd` – Bulunduğun Dizin
- Mevcut dizinin tam yolunu gösterir.

## 4. `mkdir` – Klasör Oluşturma
- Yeni klasör/dizin oluşturur.
- `mkdir yeni_klasör`

## 5. `rmdir` – Klasör Silme
- Boş klasörleri siler.
- `rmdir klasör_adi`

## 6. `cat` – Dosya İçeriğini Görüntüleme
- `cat dosya.txt` → İçeriği gösterir  
- `cat > dosya.txt` → Dosya oluştur ve yaz (Ctrl+D ile bitir)

## 7. `grep` – Metin Arama
- `grep "aranan" dosya.txt` → Eşleşen satırları listeler  
- `grep -i` → Büyük/küçük harf duyarsız  
- `grep -r` → Dizin içinde yinelemeli arar

## 8. `tail` – Dosya Sonunu Görüntüleme
- `tail dosya.txt` → Son 10 satırı gösterir  
- `tail -n 20` → Son 20 satır  
- `tail -f` → Canlı log takibi

## 9. `ifconfig` – Ağ Arayüzü Bilgisi
- Ağ kartlarının IP adresi ve yapılandırmalarını gösterir.  
- Alternatifi: `ip addr`

## 10. `uptime` – Sistem Çalışma Süresi
- Sistem ne kadar süredir açık, yük ortalamalarıyla birlikte gösterir.

## 11. `history` – Komut Geçmişi
- Terminalde yazılan önceki komutları listeler.

## 12. `clear` – Terminali Temizleme
- Ekrandaki tüm çıktıları temizler.

## 13. `ping` – Ağ Bağlantısını Test Etme
- `ping google.com` → Hedefe paket gönderip yanıt süresini ölçer.

## 14. `apt-get install` – Paket Yükleme (Debian/Ubuntu)
- `sudo apt-get install paket_adi`  
- Yazılım kurmak için kullanılır.

## 15. `sudo su` – Root Kullanıcıya Geçiş
- Yetkili (superuser) oturumu başlatır.

## 16. `echo` – Terminale Yazı Yazdırma
- `echo "Merhaba"` → Ekrana "Merhaba" yazar  
- Değişkenlerle kullanılır: `echo $HOME`

## 17. `cp` – Dosya Kopyalama
- `cp kaynak hedef` → Dosya kopyalar  
- `cp dosya.txt /hedef/klasör/`

## 18. `cp -r` – Klasör Kopyalama
- `cp -r kaynak_klasör hedef_klasör`  
- Alt klasör ve dosyalarla birlikte kopyalar.

---

## Ekstra Bilgiler:
- `man komut_adı` → Komutun kılavuzunu açar  
- `komut --help` → Yardım sayfası gösterir  
- Komutlar log analizi, sistem yönetimi ve güvenlik takibi için temeldir.



