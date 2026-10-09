# onuralptumer.com — Atölye

Onuralp Tümer'in kişisel sitesi. Bu dosya, sitenin konsept kararlarını taşır. Her değişiklikten önce oku; aşağıdaki kararlar tartışılarak verildi, sorulmadan bozma.

## Konsept

- **Site bir CV değil.** Kariyer, deneyim ve makaleler LinkedIn'in işi. Site LinkedIn'i kopyalamaz.
- **Konsept: Atölye.** Onuralp hep bir şeyler kuran, üreten biri. Fotoğraf, müzik, iOS uygulamaları ve fabrikada kurduğu sistemler aynı yaratım eyleminin farklı malzemelerdeki ürünleri; birbirlerini besliyorlar.
- **Ziyaretçide bırakılacak his:** "Bu adam çok yönlü, işinde iyi, işi dışında da kaliteli ve farklı işler yapıyor; farklı bir zihni var."
- **Hero cümlesi:** "Atölyede saat yok." (EN: "The workshop keeps no time."). Açıklanmaz; anlam katmanlı kalır.

## Kurallar

- **Minimum metin.** Her şeye yazı yazılmaz; işler kendini anlatır. Açıklama eklemeden önce sor.
- **"Atölye" kelimesi tekrarlanmaz.** Sadece hero'da geçer.
- **Tarih yok.** Hiçbir işte tarih gösterilmez. Tek katmanlı, tarihsiz bir koleksiyon.
- **Şirket bilgisi yok.** İnci GS Yuasa / İnci Akü projeleri, adları, verileri, ekran görüntüleri sitede yer almaz. İş tarafı tek bir "Sahadan" kutusuyla temsil edilir ve LinkedIn'e yönlendirir.
- **Makaleler:** Sadece son 3 LinkedIn makalesinin başlığı, LinkedIn'e bağlantıyla. Makale içeriği siteye taşınmaz.
- **İki dilli:** Türkçe varsayılan, İngilizce ikinci. Her yeni içerik iki dilde.
- **Rumuzlar:** Marcus Veld ve Veldra (müzik projeleri) koleksiyonda birer iş olarak yer alır ve kendi dünyalarına bağlanır.
- **Güncelleme temposu:** 1–2 ayda bir yeni iş eklenir. Yapı buna göre basit kalmalı.

## Görsel dil

- Gece çalışılan bir atölye: koyu, sıcak zemin; tek vurgu rengi bir lamba ışığı.
- Renkler: zemin `#14120F`, yüzey `#1D1A16`, çizgi `#2E2A24`, metin `#ECE6DB`, ikincil metin `#A39A8C`, lamba `#E8B04B`.
- Yazı tipleri: DM Serif Display (başlık ve iş adları), IBM Plex Sans (gövde), IBM Plex Mono (etiketler).
- Her iş bir malzemeye ait: **Fotoğraf** (EN Photography), **Müzik** (Music), **Yazılım** (Software; uygulamalar), **Profesyonel** (Professional; saha), **Blog** (Blog; seyahattarifleri.com). Koddaki anahtarlar eski adlarla kaldı: `isik`, `ses`, `kod`, `sistem`, `yol`. Malzeme süzgeci, "aynı tezgâh, farklı malzemeler" fikrini metin yerine etkileşimle anlatır.

## Mevcut durum

- `index.html`: Tek sayfa, bağımlılıksız (HTML + CSS + vanilla JS). TR/EN düğmesi ve malzeme süzgeci çalışıyor.
- Bağlantılar dolu: ThinkLighter ve Bunny Fence (App Store), Veldra ve Marcus Veld (Spotify), Seyahat Tarifleri, Sahadan → LinkedIn profili, son 3 makale, e-posta.
- Fotoğraf işleri iki "Galeri" kutusu (kapakları Prag ve Viyana; ilk galeride Prag + fener). Tıklanınca büyük görsel açılır (`.lightbox` dialog). Galeriye dönüştürmek için `data-gallery` içine görselleri virgülle ekle (`img/prag.webp,img/prag-2.webp`); ileri/geri okları, sayaç, klavye ve kaydırma birden fazla görselde kendiliğinden çıkar.
- Görseller `img/` klasöründe (webp). Kutular kare. Kapaklar kutuyu doldurur. Uygulamalar `.frame.combo`: zemin rengi (`--bg`) + ekran görüntüsü (`.shot`) + sol altta ikon (`.badge`). Seyahat Tarifleri: tam fotoğraf + logo rozeti. Sahadan: anonim gece fabrika görseli (şirkete ait değil). Galeri kutusunun kapağı `data-gallery` listesindeki ilk görseldir.
- Yayın: Vercel, statik (build adımı yok). `vercel.json` yalnızca temiz URL ve önbellek ayarı taşır.

## Sıradaki işler

1. Gerçek görselleri yerleştir: fotoğraflar, uygulama ekran görüntüleri, Veldra ve Marcus Veld kapakları (`.frame` içindeki svg yerine `<img>`).
2. Fotoğraf kutularını galeriye dönüştür (her kutuya yeni fotoğraflar).
3. Her iş için tıklanınca ne olacağına karar ver (kendi sayfası mı, dış bağlantı mı).
4. Yayına alma (ör. Vercel) ve onuralptumer.com alan adının bağlanması.
