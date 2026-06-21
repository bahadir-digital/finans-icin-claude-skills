---
name: financial-summary
description: Yapıştırılan ham finansal tabloyu (mizan, gelir tablosu, bilanço, CSV) okur ve yönetici özeti, öne çıkan rakamlar, dikkat edilecek uyarılar ve önerilen sonraki analiz olarak özetler. "Şu tabloyu özetle", "mizanı yorumla", "gelir tablosundan ne çıkıyor", "hızlı finansal özet", "bu veriden ne anlamalıyım" gibi ifadelerde tetiklenir.
---

# Ham Veriden Hızlı Finansal Özet

Önüne konan finansal tabloyu hızlıca okunur bir özete çevirir: en önemli rakamlar, dikkat çeken noktalar ve hangi konuya derinlemesine bakman gerektiği. Diğer analiz skillerine giriş kapısıdır.

## Ne zaman tetiklenir
- "Bu mizanı/gelir tablosunu özetle"
- "Tabloyu yapıştırıyorum, bana özet çıkar"
- "Bu veriden yönetici özeti hazırla"
- "Rakamlarda dikkat çeken ne var?"
- "Hangi konuya daha yakından bakmalıyım?"

## Girdi
- Finansal tablo (mizan / gelir tablosu / bilanço / serbest CSV — tablo halinde yapıştırılmış)
- Dönem bilgisi
- Varsa karşılaştırma dönemi
- Özetin kime gideceği (yönetim, kendisi) — ton için, opsiyonel

## Çıktı yapısı
1. **Tek paragraf özet** — dönemin genel finansal görünümü
2. **Öne çıkan rakamlar** — ciro, brüt kâr, faaliyet kârı, net kâr, nakit (mevcut olanlar)
3. **Dikkat/uyarı** — olağandışı bakiyeler, ani değişimler, eksik görünen kalemler
4. **Önerilen sonraki analiz** — hangi skill'le derinleşilebilir (sapma, nakit, yaşlandırma vb.)
5. **Açık sorular** — özeti netleştirmek için kullanıcıya kısa sorular

## Kurallar
- Veride olmayan rakamı uydurma; "tabloda görünmüyor" de.
- Tek tek tüm satırları sayma; en önemli 5-7 noktaya odaklan.
- Yüzde ve büyüklük yorumunu birlikte ver (örn. "küçük bir kalemde büyük yüzde").
- Mizan ise borç/alacak bakiye mantığını koru; ters bakiyeyi (örn. alacak hesabında alacak kalanı) işaretle.
- Vergi/yorum gerektiren teknik konularda kesin hüküm verme, "doğrulanmalı" notu koy.

## Örnek
**Girdi:** Gelir tablosu yapıştırılıyor; ciro artmış, net kâr düşmüş.
**Çıktı:** "Ciro %18 büyümüş ama net kâr %6 gerilemiş; aradaki fark büyük olasılıkla artan faaliyet giderleri ve finansman maliyetinden geliyor." Öne çıkanlar listelenir, sonraki adım olarak gider analizi ve sapma analizi önerilir.
