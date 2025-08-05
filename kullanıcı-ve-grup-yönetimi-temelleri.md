# Kullanıcı ve Grup Yönetimi Temelleri

## 1. Temel Tanımlar

### Kullanıcı (User)
- Sisteme giriş yapabilen kişi veya servis.
- Her kullanıcının:
  - Kullanıcı adı (username)
  - Kullanıcı kimlik numarası (UID)
  - Birincil grubu (GID)
  - Ev dizini (home directory)
  - Giriş kabuğu (login shell) vardır.

### Grup (Group)
- Kullanıcıların toplandığı birimdir.
- Ortak dosya erişim izinlerini yönetmekte kullanılır.
- Her grubun bir Grup ID'si (GID) vardır.

---

## 2. Önemli Dosyalar

| Dosya            | Açıklama                              |
|------------------|---------------------------------------|
| `/etc/passwd`    | Kullanıcı bilgileri                   |
| `/etc/shadow`    | Şifre bilgileri (şifreli ve gizli)     |
| `/etc/group`     | Grup bilgileri                        |
| `/etc/gshadow`   | Grup şifre bilgileri (gizli)          |

---

## 3. Kullanıcı İşlemleri

### Kullanıcı Ekleme

```bash
sudo adduser kullanıcı_adı
# veya
sudo useradd -m kullanıcı_adı
