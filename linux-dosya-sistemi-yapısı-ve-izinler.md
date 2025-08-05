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
/
├── bin/ # Temel kullanıcı komutları (ls, cp, mv vb.)
├── boot/ # Önyükleme dosyaları (kernel vb.)
├── dev/ # Donanım cihaz dosyaları
├── etc/ # Sistem yapılandırma dosyaları
├── home/ # Kullanıcıların kişisel dizinleri
├── lib/ # Paylaşılan kütüphaneler
├── media/ # Çıkarılabilir medya için bağlama noktaları
├── mnt/ # Geçici bağlama noktaları
├── opt/ # Opsiyonel yazılımlar
├── proc/ # Çekirdek ve süreç bilgileri (sanal dosya sistemi)
├── root/ # Root kullanıcısının ev dizini
├── sbin/ # Sistem yöneticisi komutları
├── srv/ # Hizmetlere ait veri dosyaları
├── tmp/ # Geçici dosyalar
├── usr/ # Kullanıcı programları ve dosyaları
└── var/ # Değişken veri dosyaları (log, spool vb.)
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
