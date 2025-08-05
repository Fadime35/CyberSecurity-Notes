# Linux Dosya Sistemi Yapısı ve İzinler

## 1. Linux Dosya Sistemi Hiyerarşisi (FHS - File Hierarchy Standard)

- Linux'ta tüm dosyalar `/` kök dizininden başlar.
- Temel dizinler ve görevleri:

| Dizin       | Açıklama                                              |
|-------------|--------------------------------------------------------|
| `/`         | Kök dizin. Tüm dosyalar buradan türetilir.            |
| `/home`     | Kullanıcıların kişisel dizinleri. `/home/kullanici`   |
| `/root`     | Root (yönetici) kullanıcısının dizini.                |
| `/bin`      | Temel sistem komutları (ls, cp, mv, rm, vb.)          |
| `/sbin`     | Sistem yöneticisine özel komutlar.                    |
| `/etc`      | Yapılandırma (config) dosyaları.                      |
| `/var`      | Değişken dosyalar (log, mail, spool, vb.).            |
| `/usr`      | Kullanıcıya ait uygulamalar ve dosyalar.              |
| `/tmp`      | Geçici dosyalar. Yeniden başlatıldığında silinir.     |
| `/dev`      | Donanım aygıt dosyaları (disk, USB, vs.)              |
| `/proc`     | Çalışan işlemler ve sistem bilgisi (sanal dosyalar).  |
| `/mnt` `/media` | Harici diskler/aygıtlar için bağlama noktaları.  |

---


## 2. Dosya Türleri

- `-` Normal dosya
- `d` Dizin (directory)
- `l` Sembolik link (kısayol)
- `c` Karakter aygıt dosyası
- `b` Blok aygıt dosyası
- `s` Socket dosyası
- `p` Named pipe (FIFO)

## 3. Dosya İzinleri

Dosya izinleri 3 farklı kullanıcı grubu için belirlenir:

| Kullanıcı Grubu | Kısaltma | Açıklama             |
|-----------------|----------|----------------------|
| Owner (Sahip)   | User (u) | Dosyanın sahibi      |
| Group (g)       | Grup     | Dosyanın ait olduğu grup |
| Others (o)      | Diğerleri| Diğer tüm kullanıcılar |

Her kullanıcı grubu için 3 tip izin vardır:

| İzin  | Açıklama           |
|-------|--------------------|
| r     | Okuma izni (read)  |
| w     | Yazma izni (write) |
| x     | Çalıştırma izni (execute) |

### 3.1 İzinlerin Görünümü

`ls -l` komutu ile dosya izinleri şöyle görünür:

-rwxr-xr--

- İlk karakter dosya türünü belirtir (`-` normal dosya, `d` dizin vb.)
- Sonraki 3 karakter kullanıcı izinleri (rwx)
- Sonraki 3 karakter grup izinleri (r-x)
- Son 3 karakter diğer kullanıcı izinleri (r--)

### 3.2 Sayısal (Octal) İzin Gösterimi

İzinler 3 basamaklı sayılarla da gösterilir, her basamak 0-7 arasında olur:

| İzinler | Değer | Açıklama                  |
|---------|-------|---------------------------|
| ---     | 0     | İzin yok                  |
| --x     | 1     | Sadece çalıştırma          |
| -w-     | 2     | Sadece yazma              |
| -wx     | 3     | Yazma + çalıştırma        |
| r--     | 4     | Sadece okuma              |
| r-x     | 5     | Okuma + çalıştırma        |
| rw-     | 6     | Okuma + yazma             |
| rwx     | 7     | Okuma + yazma + çalıştırma|

Örnek: `chmod 755 dosya` komutu

- User: 7 (rwx)
- Group: 5 (r-x)
- Others: 5 (r-x)

## 4. İzinleri Değiştirme Komutları

- `chmod` : Dosya izinlerini değiştirir
  - Sayısal veya sembolik olarak kullanılır
  - Örnekler:
    - `chmod 644 file.txt`  (User: rw-, Group: r--, Others: r--)
    - `chmod u+x script.sh` (Sahibe çalıştırma izni ekle)

- `chown` : Dosya sahibi ve grubu değiştirir
  - Örnek: `chown fadime:users file.txt`

- `ls -l` : Dosya izinlerini ve sahip bilgilerini gösterir

## 5. Örnek

```bash
$ ls -l script.sh
-rwxr-xr-- 1 fadime users 1234 Aug 5 10:30 script.sh

| Bölüm | Açıklama                  |
|---------|---------------------------|
| -    |  İzin yok                  |
| rwx  | Sadece çalıştırma          |
|  r-x  | Sadece yazma              |
| r--   | Yazma + çalıştırma        |
|   1  | Sadece okuma              |
|  fadime   | Okuma + çalıştırma        |
| users    |Okuma + yazma             |
| 1234    |  Okuma + yazma + çalıştırma|
| Aug 5 10.30    |  Okuma + yazma + çalıştırma|
| script.sh   |  Okuma + yazma + çalıştırma|
