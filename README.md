# Karakter Tabanlı Hayatta Kalma Simülatörü (C Project)

Bu proje, C programlama dili kullanılarak geliştirilmiş metin tabanlı bir hayatta kalma oyunudur. Oyuncu, sınırlı kaynaklarla (enerji, sağlık) hayatta kalmaya çalışırken çeşitli komutlar kullanarak stratejik kararlar verir.

## 🎮 Oyun Özellikleri ve Komutlar

Oyun `do-while` döngüsü içerisinde çalışır ve kullanıcıdan sürekli komut bekler. Kullanılabilir komutlar şunlardır:

* **[A]vlan:** Enerji harcayarak yemek bulmaya çalışır. (Şans faktörü ve sağlık durumu etkilidir).
* **[S]ığınak Ara:** Güvenli bir sığınak arar.
* **[E]nvanter:** Mevcut sağlık, enerji ve yemek durumunu listeler.
* **[R]Dinlen:** Yemek yiyerek enerji ve sağlık kazanılmasını sağlar.
* **[F]Tehlike:** `For` döngüsü ile simüle edilen bir tehlike dalgası (fırtına/saldırı) başlatır.
* **[P]Şifre:** `Do-while` döngüsü ile korunan şifreli bir engeli aşmaya çalışır.
* **[X]Çıkış:** Simülasyonu sonlandırır.

## 🛠 Teknik Detaylar ve Kod Yapısı

Bu projede C dilinin temel yapı taşları şu amaçlarla kullanılmıştır:

* **Switch-Case Yapısı:** Kullanıcının girdiği karakter komutlarını (A, S, R vb.) kontrol etmek ve ilgili işlemleri hızlıca yönlendirmek için kullanılmıştır.
* **Do-While Döngüsü (Oyun Motoru):** Oyunun en az bir kez çalışması ve kullanıcı 'X' komutunu verene kadar döngünün devam etmesi için ana blok `do-while` içine alınmıştır.
* **For Döngüsü (Tehlike Simülasyonu):** 'F' komutunda belirli sayıda (örneğin 3 dalga) hasar veya olay gerçekleşmesi gerektiği için `for` döngüsü tercih edilmiştir.
* **İç İçe Döngüler (Şifre Çözme):** 'P' komutunda kullanıcı doğru şifreyi bulana kadar tekrar tekrar giriş yapması gerektiği için, bu işlem ana döngüden bağımsız ikinci bir `do-while` ile yönetilmiştir.
* **Mantıksal ve Aritmetik Operatörler:** Can ve enerji hesaplamalarında aritmetik operatörler; avlanma başarısı gibi çoklu koşulların kontrolünde ise `&&` (VE) ve `||` (VEYA) mantıksal operatörleri kullanılmıştır.

## 🚀 Kurulum ve Çalıştırma

Kodu derlemek ve çalıştırmak için bir C derleyicisine (GCC gibi) ihtiyacınız vardır.

1.  Repoyu klonlayın veya `main.c` dosyasını indirin.
2.  Terminali açın ve dosyanın olduğu dizine gidin.
3.  Şu komutla derleyin:
    ```bash
    gcc main.c -o survival_game
    ```
4.  Çalıştırın:
    * Windows için: `survival_game.exe`
    * Linux/Mac için: `./survival_game`
