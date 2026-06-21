---
name: cash-flow-tracker
description: Nakit giriş ve çıkışlarını dönem dönem takip eder, net nakit ve devreden bakiyeyi hesaplar, kasanın ne kadar dayanacağını (runway) gösterir ve düşük nakit uyarısı verir. "Nakit akışı çıkar", "kasa pozisyonu", "ne kadar nakit dayanır", "haftalık nakit projeksiyonu", "tahsilat ödeme planı" gibi ifadelerde tetiklenir.
---

# Nakit Akışı ve Pozisyon Takibi

Tahsilatlar ve ödemeler üzerinden dönemsel nakit pozisyonunu çıkarır. Kârlı görünüp nakitte zorlanan şirketlerde en sık ihtiyaç duyulan tablo budur. Haftalık veya aylık çalışır.

## Ne zaman tetiklenir
- "Önümüzdeki 13 haftanın nakit akışını çıkar"
- "Bu ayki tahsilat ve ödemelerle kasa nasıl gider?"
- "Nakitimiz kaç ay yeter?"
- "Hangi hafta nakit açığına düşeriz?"
- "Gelen-giden parayı tabloya dök"

## Girdi
- Açılış nakit bakiyesi
- Beklenen tahsilatlar (tarih/dönem, tutar, varsa olasılık)
- Planlanan ödemeler (maaş, kira, tedarikçi, vergi, kredi taksiti vb.)
- Dönem aralığı (haftalık / aylık) ve kaç dönem ileri
- Para birimi

## Çıktı yapısı
1. **Nakit akışı tablosu** — Dönem / Açılış / Toplam Giriş / Toplam Çıkış / Net Nakit / Kapanış bakiyesi
2. **Runway** — mevcut yakış hızıyla nakit kaç dönem/ay yeter
3. **Risk dönemleri** — bakiyenin kritik eşiğin altına düştüğü dönemler işaretli
4. **Kategori kırılımı** — girişleri ve çıkışları ana başlıklarda topla (opsiyonel)
5. **Kısa yorum** — likidite görünümü ve dikkat edilecek dönem

## Kurallar
- Kapanış bakiyesi = açılış + giriş − çıkış. Her dönemin kapanışı bir sonrakinin açılışıdır.
- Negatif veya kritik eşik altı bakiyeyi mutlaka işaretle.
- Tahsilatlara olasılık verildiyse hem brüt hem olasılıklı senaryoyu göster.
- Vergi ve SGK ödeme tarihlerini ayrı satırda tut; bunlar nakit planında sık atlanır.
- Tahmin olduğunu belirt; gerçekleşen ile karşılaştırma için yer bırak.

## Örnek
**Girdi:** Açılış 500.000 TL. 3. hafta 400.000 TL maaş + 150.000 TL vergi ödemesi, beklenen tahsilat 200.000 TL.
**Çıktı:** 3. hafta net −350.000 TL, kapanış 150.000 TL. Uyarı: bu hafta nakit en düşük seviyede; tahsilatın gecikmesi açığa yol açar, tedarikçi ödemesi 4. haftaya kaydırılabilir.
