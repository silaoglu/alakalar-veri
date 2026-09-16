# alakalar-veri

Alakalar kök çalışması için açık veri deposu. Yalnız ham kaynak metinler ve
kök paketleri — yorum, çeviri veya özet yok.

## Yapı

- `kaynak/` — Kur'an metni (Tanzil), morfoloji (Quranic Arabic Corpus),
  dokuz klasik sözlüğün ham metni, dördünün kök kök ayrıştırılmış çıktısı.
  Künye ve lisans bilgisi: `kaynak/README.md`.
- `paketler/<kok>/` — her kök için `sozluk.md` (sözlük girişleri),
  `ayetler.tsv` (Kur'an'daki geçişleri, morfolojik künyeyle), `sayim.md`
  (segment/ayet/sûre sayıları, lem ve kalıp dağılımı).

## Üretim

Bu depodaki dosyalar özel bir depoda (silaoglu/Alakalar) tutulan bir betikle
üretildi, elle düzenlenmedi.
