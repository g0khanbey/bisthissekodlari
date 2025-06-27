# BIST Hisse Kodu Listesi (CSV)

Bu depo, **Borsa İstanbul (BIST)**'ta işlem gören şirketlerin güncel hisse kodlarını CSV formatında sunar. Veri seti 28 Haziran 2025 itibarıyla Kamuoyu Aydınlatma Platformu (KAP) üzerinden derlenmiştir.

## Veri Kaynağı

* **Kamuoyu Aydınlatma Platformu – BIST Şirketler Sayfası**
  [https://www.kap.org.tr/tr/bist-sirketler](https://www.kap.org.tr/tr/bist-sirketler)

## Dosyalar

| Dosya              | Açıklama                                                                    |
| ------------------ | --------------------------------------------------------------------------- |
| `bist_tickers.csv` | BIST’te işlem gören tüm şirketlerin hisse kodları (ve opsiyonel şirket adı) |

### `bist_tickers.csv` Sütunları

| Sütun  | Açıklama                   |
| ------ | -------------------------- |
| `code` | Hisse kodu (ör. **AKBNK**) |
| `name` | Şirket adı (opsiyonel)     |

## Hızlı Başlangıç

```bash
pip install pandas
```

```python
import pandas as pd

tickers = pd.read_csv("bist_tickers.csv")
print(tickers.head())
```

## Güncelleme

Veri, `scripts/scrape_kap_bist.py` betiğiyle otomatik güncellenebilir:

```bash
python scripts/scrape_kap_bist.py --output bist_tickers.csv
```

> **Uyarı:** KAP sitesi zaman zaman erişim kısıtlamaları uygulayabilir. Betiği çalıştırmadan önce **robots.txt** ve site kullanım koşullarını kontrol edin.

## Lisans

Bu proje **MIT Lisansı** ile lisanslanmıştır. Ayrıntılı bilgi için `LICENSE` dosyasına bakın.

## Katkı

Hata bildirmek veya katkıda bulunmak için lütfen [Issues](../../issues) bölümünü kullanın veya bir Pull Request oluşturun.
