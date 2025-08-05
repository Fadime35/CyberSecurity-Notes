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

## 3. `cat` – Dosya İçeriğini Gösterme
- Dosya içeriğini terminalde görüntüler.
- Sık Kullanım:
  - `cat dosya.txt` → Dosyanın içeriğini gösterir.
  - `cat dosya1 dosya2` → Birleştirip gösterir.
  - `cat > dosya.txt` → Yeni dosya oluşturur ve içine yazı yazılır (Ctrl+D ile çıkılır).

## 4. `grep` – Metin Arama
- Belirli bir ifadeyi dosyada veya çıktı içinde arar.
- Sık Kullanım:
  - `grep "kelime" dosya.txt` → Dosyada “kelime” geçen satırları gösterir.
  - `ps aux | grep firefox` → Bellekteki işlemler arasında “firefox” geçenleri arar.
  - `grep -i` → Büyük/küçük harf duyarsız arama.
  - `grep -r` → Dizin içinde ve alt dizinlerde arama.

## 5. `tail` – Dosyanın Son Satırlarını Görüntüleme
- Bir dosyanın son satırlarını gösterir.
- Sık Kullanım:
  - `tail dosya.txt` → Son 10 satırı gösterir.
  - `tail -n 20 dosya.txt` → Son 20 satırı gösterir.
  - `tail -f dosya.txt` → Dosya değiştikçe yeni satırları anlık gösterir (log takibi).

---

## Ekstra İpuçları:
- Kombinasyon: `cat dosya.txt | grep "hata"` → Dosyada "hata" içeren satırları bulur.
- Log analizi ve sistem takibinde bu komutlar sık kullanılır.
- `man komut_adı` ile her komutun detaylarına ulaşılabilir.

