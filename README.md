# BIST Hisse Kodu Listesi (CSV)

Bu depo, **Borsa İstanbul (BIST)**'ta işlem gören şirketlerin güncel hisse kodlarını CSV formatında sunar. Veri seti 28 Haziran 2025 itibarıyla Kamuoyu Aydınlatma Platformu (KAP) üzerinden derlenmiştir.

## Veri Kaynağı

* **Kamuoyu Aydınlatma Platformu – BIST Şirketler Sayfası**
  [https://www.kap.org.tr/tr/bist-sirketler](https://www.kap.org.tr/tr/bist-sirketler)



### `bisthissekodlari.csv` Sütunları



## Hızlı Başlangıç

```bash
pip install pandas
```

```python
import pandas as pd

tickers = pd.read_csv("bist_tickers.csv")
print(tickers.head())
```




## Lisans

Bu proje **MIT Lisansı** ile lisanslanmıştır. Ayrıntılı bilgi için `LICENSE` dosyasına bakın.



