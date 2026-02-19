# RET2LIBC-ASLR-BYPASS

## RET2LIBC ASLR BYPASS
HEDEF ASLR korumasını atlatmak

## Güvenlik Mekanizmaları / Security Mechanisms

| Mekanizma | Durum | Açıklama |
|-----------|-------|----------|
| **NX** |  ENABLED | Stack üzerinde kod çalıştırılamaz (No Shellcode) |
| **ASLR** |  Kısmi | PIE kapalı, LIBC ASLR aktif |
| **RELRO** |  Partial | Kısmi RELRO etkin |
| **PIE** |  DISABLED | Konum bağımsız kod üretilmemiş |

##  Özet / Summary
- **Zafiyet Türü:** Buffer Overflow → ret2libc
- **Bypass Edilen Koruma:** ASLR (LIBC adreslerini sızdırarak)
- **Kullanılan Teknik:** Information Leak + ret2libc
- **Hedef:** ASLR etkin bir sistemde libc fonksiyonlarını çalıştırmak
