# Kaynak metinler

Bu klasördeki dosyalar değiştirilmeden, olduğu gibi taşınmıştır (ayrıştırılmış
`*-parsed.jsonl` dosyaları hariç — bkz. aşağıda).

## Kur'an metni

Kaynak: Tanzil.net, Eylül 2026 indirmesi.

- `quran-uthmani.txt` — Osmanî yazım, `sure|ayet|metin` biçiminde.
- `quran-simple-clean.txt` — harekesiz sade yazım, `sure|ayet|metin` biçiminde.

Tanzil telif şartı: metin değiştirilmeden kullanılmıştır, kaynak olarak
Tanzil Project (tanzil.net) belirtilir.

## Morfoloji

`quranic-corpus-morphology-0.4.txt` — Quranic Arabic Corpus (morphology,
version 0.4), Kais Dukes, 2011. Lisans: GNU General Public License. Dosyanın
kendi başlığındaki telif bloğu korunmuştur.

## Klasik sözlükler

OpenITI mARkdown biçiminde, ayrıştırılmadan (ayrıştırılan dört eser hariç,
aşağıya bkz.) taşınmış ham metinler. Künye:

| dosya | eser | neşir |
|---|---|---|
| ayn.txt | Kitâbü'l-Ayn | Mahzûmî / Sâmerrâî, Hilâl, 8 cilt |
| cemhere.txt | Cemheretü'l-Luga | Ba'lebekkî, Dâru'l-İlm, Beyrut 1987, 3 cilt |
| tehzib.txt | Tehzîbü'l-Lüga | Mur'ib, Dâru İhyâi't-Türâs, Beyrut 2001, 15 cilt |
| sihah.txt | es-Sıhâh | Attâr, Dâru'l-İlm, 1407/1987, 6 cilt |
| mekayis.txt | Mekâyîsü'l-Lüga | Hârûn, Dâru'l-Fikr, 1399/1979, 6 cilt |
| mucmel.txt | Mücmelü'l-Lüga | Sultân, Risâle, Beyrut |
| muhkem.txt | el-Muhkem | Hindâvî, DKİ, Beyrut 2000, 11 cilt |
| muhassas.txt | el-Muhassas | Ceffâl, Beyrut 1417/1996, 5 cilt |
| esas.txt | Esâsü'l-Belâga | Uyûnu's-Sûd, DKİ, 2 cilt |

Not: Mekâyîs'te Dâru'l-Fikr 1979 baskısı kullanılmıştır (Dâru'l-Cîl 1999
değil) — sayfa numaraları iki baskıda farklıdır.

## Ayrıştırılmış çıktılar

`ayn-parsed.jsonl`, `mucmel-parsed.jsonl`, `mekayis-parsed.jsonl`,
`cemhere-parsed.jsonl` — yukarıdaki dört ham metinden, kök kök ayrılmış
girişler. Her satır bir JSON kaydı: `kok`, `bab`, `metin`,
`sayfa_isaretleri` (`{konum, cilt, sayfa}` dizisi — `konum`, `metin`
alanı içindeki karakter konumu).

Ayrıştırma betikleri ana (özel) depoda tutuluyor, bu depoya dahil değil.
`ayn-parsed.jsonl` için bilinen bir durum: ayırıcıdaki bir normalizasyon
düzeltmesi (DIACRITICS_RE) sonrası dosya henüz yeniden üretilmedi; ölçülen
etki +4 kök, 0 kayıp (yalnız harekeli/şeddeli yazılmış birkaç kanonik kök
etkileniyor).

Kanonik kök listesi (2723 kök) editoryal bir başlangıç listesidir, nötr veri
değildir — bazı sık geçen kökler bu listede yer almayabilir (bkz.
`paketler/` altındaki ilgili köklerin `sozluk.md` dosyalarındaki notlar).

## Kapsam dışı bırakılanlar

Bu depoya şunlar dahil edilmedi: ayırıştırma/kazıma betikleri, deneme
metinleri, karar notları, proje dosyaları, .env/anahtar içeren dosyalar.
