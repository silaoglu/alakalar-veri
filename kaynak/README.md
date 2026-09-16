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

Kanonik kök listesi başlangıçta 2723 kök içeren editoryal bir liste
(Hawramani/Ayn kök dizini) idi; 2026-09-16'da morfoloji dosyasındaki
1.642 kökün tamamını (mudaaf kökler için 2 harfli katlama kuralıyla)
kapsayacak şekilde 3796 köke tamamlandı — bkz. `kaynak/README.md`
içindeki künye ve ana depodaki CLAUDE.md. Yine de nötr veri değildir:
Kur'an'da geçmeyen bazı klasik kökler listede yer almayabilir.

## Kapsam dışı bırakılanlar

Bu depoya şunlar dahil edilmedi: ayırıştırma/kazıma betikleri, deneme
metinleri, karar notları, proje dosyaları, .env/anahtar içeren dosyalar.
