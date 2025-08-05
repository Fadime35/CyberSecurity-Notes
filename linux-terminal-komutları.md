ls         # Dizin içeriğini listeler
ls -l      # Uzun liste formatı (izinler, sahip, boyut vb.)
ls -a      # Gizli dosyaları da gösterir

cd /       # Root dizinine geçiş
cd ~       # Home dizinine geçiş
cd ..      # Bir üst dizine geçiş
cd /etc    # Belirli bir dizine geçiş

pwd        # Geçerli dizini gösterir

cat dosya.txt      # Dosyanın içeriğini terminalde gösterir
tac dosya.txt      # Dosyayı tersten gösterir
less dosya.txt     # Sayfa sayfa görüntüleme
head -n 10 dosya   # İlk 10 satırı gösterir
tail -n 10 dosya   # Son 10 satırı gösterir
tail -f dosya.log  # Log dosyasını canlı izler

grep "kelime" dosya.txt   # Belirli kelimeyi içeren satırları arar
grep -r "admin" /etc      # Belirli bir dizin içinde arama yapar

clear      # Terminal ekranını temizler
history    # Kullanılan komut geçmişini gösterir
