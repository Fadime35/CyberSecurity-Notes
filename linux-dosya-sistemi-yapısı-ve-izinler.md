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

## 2. Dosya ve Dizin İzinleri

### İzin Türleri:
- `r` → okuma (read)
- `w` → yazma (write)
- `x` → çalıştırma (execute)

### Kimler İçin:
- **u** → user (dosya sahibi)
- **g** → group (dosya sahibinin grubu)
- **o** → others (diğer herkes)

### Örnek Listeleme:
```bash
ls -l
