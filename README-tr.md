*Bunu diğer dillerde oku: [中国](README-cn.md), [한국어](README-ko.md), [日本](README-ja.md), [português](README-pt.md), [İngilizce](README.md)
## Marbles Hakkında..
- Bu uygulamanın altında yatan ağ, bir Linux vakıf projesi olan Hyperledger Fabric'dir. Hyperledger Fabric hakkında biraz bilgi edinmek için bu talimatları gözden geçirmek isteyebilirsiniz.[Hyperledger Fabric](https://github.com/hyperledger/fabric/tree/master/docs).
- **Bu demo, bir geliştiricinin bir Fabric network ile zincir kodu ve uygulama geliştirmenin temellerini öğrenmesine yardımcı olmaktır.**
- Bu çok basit 'bir varlık' transferi gösterimidir. Birden fazla kullanıcı birbiriyle Marble oluşturabilir ve aktarabilir.

![](/doc_images/marbles-peek.gif)

### Versiyon
Çok sayıda Marble çeşidi vardır. Bu sürüm ** Hyperledger Fabric v1.1x ** ile uyumludur.

# Uygulama Arkaplanı
 Bu uygulama Hyperledger'dan yararlanan birçok Marble sahibi arasında Marble transferini gösterecek.Bunu Node.js'de ve bir miktar GoLang'da yapacağız.Bu uygulamanın arka ucu, blockchain ağımızda çalışan GoLang kodu olacaktır. Bundan sonra GoLang kodu 'Blockchain' veya 'cc' olarak adlandırılacaktır. Blockchain kendisi, Blockchain durumuna depolayarak bir Marble yaratacaktır. Zincir kodun kendisi verileri bir anahtar / değer çifti ayarında bir dize olarak saklayabilir. Bu nedenle, daha karmaşık yapıları depolamak için JSON nesnelerini dizileyeceğiz.

 Marbles Özellikleri:

  1. ID (benzeri olmayan bir dize, anahtar olarak kullanılacak).
  2. Renk (dize, css renk adları).
  3. Boyut (mm olarak Boyut).
  4. Diziye sahip olmak.

Bu değerleri ayarlayabilecek ve blockchain defterinde saklayabilecek bir UI(arayüz) oluşturacağız.
Marble gerçekten önemli bir değer çifti.
“Anahtar” Marble kimliğidir ve “değer” Marble özelliklerini içeren bir JSON dizesidir (yukarıda listelenmiştir).
