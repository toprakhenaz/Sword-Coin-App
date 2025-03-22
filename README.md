# Sword-Coin-App
**GitHub - Tap to Earn App: Sword Coin Uygulaması**  
Bu proje, kullanıcıların aktif katılım ve etkileşimle dijital ödüller kazandığı bir **Tap to Earn** uygulamasıdır. Uygulama, **Sword Coin** adlı sanal bir para birimi üzerinden çalışmaktadır. Kullanıcılar, belirli görevleri tamamlayarak ve belirli etkileşimlerde bulunarak **Sword Coin** kazanır. Uygulama, **React** ve **Next.js** teknolojileriyle geliştirilmiştir ve **Tailwind CSS** ile şık bir kullanıcı arayüzü sunmaktadır. Veri yönetimi için **Prisma** kullanarak veritabanı entegrasyonu sağlanmış, **Vercel** üzerinde barındırılmıştır. **GitHub** üzerinden açık kaynak kodlu olarak erişilemez, Uygulamanın hakları saklıdır.


## Main Page Overview

![Ana sayfa](https://github.com/toprakhenaz/Sword-Coin-App/blob/main/Images/Ana-sayfa.gif)


Tap to Earn uygulamasının ana sayfası, oyuncuların dokunarak para kazanabilecekleri basit ancak ilgi çekici bir arayüze sahiptir.

### Top Section
- **Crystals**: 65065 (kristal simgesi ile gösterilir) - Bunlar oyunun temel para birimidir ve oyun sonunda airdrop için kullanılır.
- **Coins to level up**: 2200 (yukarı ok simgesi ile gösterilir) - Bir sonraki seviyeye ulaşmak için gereken coin miktarını gösterir.
- **Earn per Tap**: +1 (coin yığını simgesi ile gösterilir) - Her tıklamada kazanılan coin miktarını belirtir.

### Center Section
- **Coin Display**: 1269 - Oyuncunun mevcut coin bakiyesini gösterir.
- **League Button**: "Lig 1 →" - Mevcut ligi gösterir ve lig sayfasına erişim sağlar.
- **Main Tap Button**: Liglerde ilerledikçe değişen bir kılıç görüntüsüne sahip büyük dairesel bir buton.
  - Bu butona tıklamak enerjiyi azaltır ve coinleri artırır.
  - Her tıklama, görünen ve kaybolan "+earn-per-tap" animasyonunu gösterir.

### Energy Section
- **Energy Bar**: "500 / 500" - Mevcut ve maksimum enerjiyi gösterir.
- **Rocket Button**: Enerjiyi tamamen doldurur, günde üç kez ve kullanımlar arasında 1 saat aralıklarla kullanılabilir.

### Bottom Navigation
Uygulama, alt menü aracılığıyla erişilebilen 4 ana sayfadan oluşur:
1. **Home**: Ana oyun arayüzü
2. **Friends**: Sosyal özellikler
3. **Mine**: Oyuncunun kaynakları/envanteri
4. **Earn**: Ek kazanç yöntemleri

Crystal tabanlı airdrop özelliği için gelecekte bir Airdrop sayfası eklenecektir.

### League System
League butonuna tıklandığında, şunları gösteren bir lig sayfası açılır:
- Liglere göre oyuncu sıralamaları
- Diğer mevcut ligler
- Bir sonraki lige yükselmek için gereken coin gereksinimler
![lig](https://github.com/toprakhenaz/Sword-Coin-App/blob/main/Images/lig.gif)



## Arkadaşlar Sayfası - Davet Sistemi

Arkadaşlar sayfası, kullanıcılara referans sistemi aracılığıyla arkadaşlarını uygulamaya davet etme ve bonus kazanma imkanı sunar.

### Davet Mekanizması
- **Arkadaşını Davet Et** butonuna tıklandığında kullanıcı doğrudan Telegram üzerinden arkadaşlarını davet edebilir
- **Kopyalama** butonuna tıklandığında davet linki panoya kopyalanır ve kullanıcı bu linki istediği platformda paylaşabilir

### Kazanç Sistemi
- Her başarılı davet sonucunda hem davet eden hem davet edilen kişi **2500 coin** bonus kazanır
- **Telegram Premium** üyeliği olan kullanıcılar ek olarak davet ettikleri kişinin kazandığı miktarın **%10'u** kadar ekstra kazanç elde eder

### Görünüm
- Sayfanın üst kısmında kullanıcının mevcut coin ve crystal miktarı görüntülenir
- Orta kısımda toplam arkadaş sayısı ve davet avantajları hakkında bilgiler yer alır
- Alt kısımda uygulama içi navigasyon menüsü bulunur

Bu referans sistemi, kullanıcıların oyun içi ekonomiye daha hızlı adapte olmalarını sağlarken, topluluk oluşturmayı ve uygulamanın büyümesini teşvik eder. 

![Friends Page](https://github.com/toprakhenaz/Sword-Coin-App/blob/main/Images/Friends-page.png)


## Mine Sayfası - Kartlar ve Günlük Kombo

Mine sayfası, kullanıcıların çeşitli kartları görüntüleyebildiği, yükseltebildiği ve günlük kombo etkinliğine katılabildiği alandır.

### Daily Combo Sistemi
- **Günlük Kombo**: Sayfanın üst kısmında görüntülenen, her 24 saatte bir otomatik olarak yenilenen özel bir etkinlik
- **Ödül**: Rastgele seçilmiş 3 kartı doğru şekilde bulunca **100,000 coin** kazanma fırsatı
- **Zaman Sayacı**: Bir sonraki yenilemeye kalan süreyi gösteren geri sayım sayacı (03:47:23)

### Kart Kategorileri
Kartlar farklı kategorilere ayrılmıştır:
- **Ekipman**
- **İşçiler**
- **İstekai**
- **Özel** (Premium kartlar, daha yüksek fiyatla satılır)

### Kart Özellikleri
- Her kartın kendine özgü görsel tasarımı vardır
- Örnekler: "Abyssal Hammer" ve "Celestial Shield"
- Kartların **Seviye** sistemi vardır (Seviye 0, Seviye 1, vb.)
- Her kart yükseltildiğinde **Crystal ** kazanılır

### Yükseltme Sistemi
- Kartları yükseltmek için coin gereklidir
- Yükseltme maliyeti kartın seviyesine göre değişir
- Örnek fiyatlar: 1100 coin, 1500 coin
- Kartlar yükseltildikçe daha değerli hale gelir

### Tasarım
- Görsel açıdan çekici, detaylı kart tasarımları
- Seviye, maliyet ve ödül bilgileri net bir şekilde gösterilir
- Alt kısımda uygulama içi navigasyon menüsü bulunur

Bu sayfa, oyun içi koleksiyon oluşturma ve ekonomi sisteminin önemli bir parçasıdır, kullanıcıları düzenli olarak uygulamaya dönmeye teşvik eden Daily Combo sistemi ile kullanıcı bağlılığını artırır.

![Mine Page](https://github.com/toprakhenaz/Sword-Coin-App/blob/main/Images/Mine.gif)
